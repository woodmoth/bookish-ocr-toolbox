# bookish-ocr-toolbox
Bash script for quick pdf splitting and ocr scan

# What is it?
in-Terminal (though it requires DE because of dmenu) toolbox that uses:
- poppler - for cutting books on slices
- tesseract and tesseract-data.* - for ocr analysing these slices
- dmenu - for selecting options
- whiptail - for selecting options and messages
- ranger - for manual intervention in *books's folders* which are created in cut/scan process

# How does it work?
1) **Bookish** seeks `.pdf` in the current directory, you choose a $book that you want to Split/Scan.
2) If you haven't yet *splitted* a $book, you cut it, choosing fragment size through dmenu's little dialog.
3) Every $book has its own ./bookish/subfolder where cutted `.pdf` fragments are stored. There could be many split regions of one $book. They are threated separately, even if they are: 3-6_page and 4-7_page e.g. and they are kept together in one $book subfolder.
4) If you splitted a $book anytime previously, you can *scan* it. The program asks which fragment you want to scan. You choose a DPI, wait for convertation `.pdf` to `.jpg` process, then `.jpg` scan process.
5) All OCR results are stored in a $book fragment subfolders, separate for each page and there is also Full Text, which possibly stores every scan of a fragment, if you did scan many times, the pages marked.
6) You can purge all subfolders of a $book. If there are no subfolders in ./bookish, then program deletes it. For a precious removal use ranger, which is an option in the menu.

# More
Though my bash may be somewhat ugly (at first bookish was planned to be 5 lines code), I tried to foresee obvious bugs and misprompts, so you *should not get errors* if prompted something out of plan, by mistake. Still bugshooting is welcome, though bookish worked well in intended patterns.
I myself use it in my digital book library so I can return to my already done splits everytime.

I used dmenu because it can easily search and tab. You can flavour it with dmenu patch.

- It could be updated soon as I use it and understand what's needed.

# Demo
![image](https://github.com/user-attachments/assets/783d9e7e-8996-44eb-9e02-a6b96830dc03)

---

The book already had some splits so we can see them while choosing what to scan, but no splits of other books.

![image](https://github.com/user-attachments/assets/a519e01a-9dd8-4e42-8f8a-9e62f88da78d)

![image](https://github.com/user-attachments/assets/a4334926-7b9e-4dcf-ba5c-1c86100eb73f)

![image](https://github.com/user-attachments/assets/d06e138a-c39b-4991-b215-63d6a9d5d417)

![image](https://github.com/user-attachments/assets/afd7e1a1-7f58-4f95-a517-5121cb4f52d1)

---
