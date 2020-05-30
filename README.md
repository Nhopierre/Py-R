{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Titre"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "440\n",
      "440\n",
      "469.86328125\n",
      "466.1637615180899\n",
      "495.0\n",
      "493.8833012561241\n",
      "528.59619140625\n",
      "523.2511306011974\n",
      "556.875\n",
      "554.3652619537443\n",
      "594.6707153320312\n",
      "587.3295358348153\n",
      "626.484375\n",
      "622.253967444162\n",
      "660.0\n",
      "659.2551138257401\n",
      "704.794921875\n",
      "698.456462866008\n",
      "742.5\n",
      "739.988845423269\n",
      "792.894287109375\n",
      "783.9908719634989\n",
      "835.3125\n",
      "830.6093951598906\n",
      "892.0060729980469\n",
      "880\n"
     ]
    }
   ],
   "source": [
    "note_1 = 440\n",
    "\n",
    "\n",
    "\n",
    "def gamme_pythagore(freq_initial):\n",
    "    gamme = []\n",
    "    gamme.append(freq_initial)\n",
    "    frequence = freq_initial\n",
    "    \n",
    "    for i in range(1,12):\n",
    "        frequence = frequence * 3/2\n",
    "        if frequence > freq_initial*2:\n",
    "            frequence = frequence/2\n",
    "        gamme.append(frequence)\n",
    "    #gamme.append(freq_initial*2)\n",
    "    gamme.sort()\n",
    "    gamme.append(frequence*3/2)\n",
    "    return gamme\n",
    "\n",
    "def gamme_temperee(freq_initial) :\n",
    "    gamme = []\n",
    "    demiton = 2**(1/12)\n",
    "    gamme.append(freq_initial)\n",
    "    frequence = freq_initial\n",
    "    for i in range(1,12):\n",
    "        frequence = frequence * demiton\n",
    "        gamme.append(frequence)\n",
    "    gamme.append(freq_initial*2)\n",
    "    gamme.sort()\n",
    "    return gamme\n",
    "\n",
    "gamme_p = gamme_pythagore(note_1)\n",
    "gamme_t = gamme_temperee(note_1)\n",
    "\n",
    "for j in range(0,len(gamme_t)) : \n",
    "    print(gamme_p[j])\n",
    "    \n",
    "    print(gamme_t[j])\n",
    "\n",
    "    "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
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
   "version": "3.7.6"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
