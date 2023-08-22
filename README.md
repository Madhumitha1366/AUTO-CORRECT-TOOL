{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 27,
   "id": "fac56cca",
   "metadata": {},
   "outputs": [],
   "source": [
    "\n",
    "from textblob import TextBlob\n",
    "\n",
    "from tkinter import *\n",
    "\n",
    "def Auto_correct():\n",
    "    corrected_words = []\n",
    "    text = Input_text.get(1.0, END).split(\" \")\n",
    "    for i in text:\n",
    "        corrected_words.append(TextBlob(i).correct())\n",
    "    Output_text.delete(1.0, END)\n",
    "    for i in corrected_words:\n",
    "        Output_text.insert(END, i + \" \")\n",
    "\n",
    "\n",
    "def Clear():\n",
    "    Input_text.delete(1.0, END)\n",
    "    Output_text.delete(1.0, END)\n",
    "\n",
    "\n",
    "mainwin = Tk()\n",
    "mainwin.geometry('1400x520')\n",
    "mainwin.resizable(False, False)\n",
    "\n",
    "mainwin.title(\"Auto Correct By Ravi Kiran\")\n",
    "mainwin.config(bg='#c09999')\n",
    "\n",
    "Label(mainwin, text=\"Auto-Correction Tool\", font='arial 30 bold', bg= '#c09999').place(x=540, y=30)\n",
    "\n",
    "Label(mainwin, text=\"Enter Text\", font='arial 18 bold', bg= '#c09999').place(x=280, y=90)\n",
    "\n",
    "Input_text = Text(mainwin, font='arial 13', bg='white', height=13, wrap=WORD, padx=5, pady=5, width=60, insertbackground='black')\n",
    "\n",
    "Input_text.place(x=80, y=130)\n",
    "\n",
    "Label(mainwin, text=\"Corrected Text\", font='arial 18 bold', bg= '#c09999').place(x=980, y=90)\n",
    "\n",
    "Output_text = Text(mainwin, font='arial 13', bg='white', height=13, wrap=WORD, padx=5, pady=5, width=60, insertbackground='black')\n",
    "\n",
    "Output_text.place(x=770, y=130)\n",
    "\n",
    "auto_correct_btn = Button(mainwin, text=\"Correct\", bg='lavender blush', width=30, font='arial 18 bold', pady=3, command=Auto_correct)\n",
    "\n",
    "auto_correct_btn.place(x=240, y=420)\n",
    "\n",
    "c1 = Button(mainwin, text=\"Clear\", width=30, pady=3, bg='lavender blush', font='arial 18 bold', command=Clear)\n",
    "\n",
    "c1.place(x=710, y=419)\n",
    "\n",
    "mainwin.mainloop()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "d361146d",
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "99cdb71c",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.11.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
