# computational-biology
Hey! I am Greer Handley, and this is my hub for all of my classwork throughout my Computational Biology course at LA Tech.
All of the code below was created following step-by-step instructions as a way to become familiar with Python and its applications.


{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [],
   "source": [
    "%matplotlib inline\n",
    "import pandas as pd\n",
    "import matplotlib.pyplot as plt\n",
    "import seaborn as sns \n",
    "sns.set(style=\"darkgrid\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [],
   "source": [
    "df = pd.read_csv('/home/student/Desktop/classroom/myfiles/notebooks/fortune500.csv')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Year</th>\n",
       "      <th>Rank</th>\n",
       "      <th>Company</th>\n",
       "      <th>Revenue (in millions)</th>\n",
       "      <th>Profit (in millions)</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <td>0</td>\n",
       "      <td>1955</td>\n",
       "      <td>1</td>\n",
       "      <td>General Motors</td>\n",
       "      <td>9823.5</td>\n",
       "      <td>806</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>1</td>\n",
       "      <td>1955</td>\n",
       "      <td>2</td>\n",
       "      <td>Exxon Mobil</td>\n",
       "      <td>5661.4</td>\n",
       "      <td>584.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>2</td>\n",
       "      <td>1955</td>\n",
       "      <td>3</td>\n",
       "      <td>U.S. Steel</td>\n",
       "      <td>3250.4</td>\n",
       "      <td>195.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>3</td>\n",
       "      <td>1955</td>\n",
       "      <td>4</td>\n",
       "      <td>General Electric</td>\n",
       "      <td>2959.1</td>\n",
       "      <td>212.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>4</td>\n",
       "      <td>1955</td>\n",
       "      <td>5</td>\n",
       "      <td>Esmark</td>\n",
       "      <td>2510.8</td>\n",
       "      <td>19.1</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   Year  Rank           Company  Revenue (in millions) Profit (in millions)\n",
       "0  1955     1    General Motors                 9823.5                  806\n",
       "1  1955     2       Exxon Mobil                 5661.4                584.8\n",
       "2  1955     3        U.S. Steel                 3250.4                195.4\n",
       "3  1955     4  General Electric                 2959.1                212.6\n",
       "4  1955     5            Esmark                 2510.8                 19.1"
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Year</th>\n",
       "      <th>Rank</th>\n",
       "      <th>Company</th>\n",
       "      <th>Revenue (in millions)</th>\n",
       "      <th>Profit (in millions)</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <td>25495</td>\n",
       "      <td>2005</td>\n",
       "      <td>496</td>\n",
       "      <td>Wm. Wrigley Jr.</td>\n",
       "      <td>3648.6</td>\n",
       "      <td>493</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>25496</td>\n",
       "      <td>2005</td>\n",
       "      <td>497</td>\n",
       "      <td>Peabody Energy</td>\n",
       "      <td>3631.6</td>\n",
       "      <td>175.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>25497</td>\n",
       "      <td>2005</td>\n",
       "      <td>498</td>\n",
       "      <td>Wendy's International</td>\n",
       "      <td>3630.4</td>\n",
       "      <td>57.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>25498</td>\n",
       "      <td>2005</td>\n",
       "      <td>499</td>\n",
       "      <td>Kindred Healthcare</td>\n",
       "      <td>3616.6</td>\n",
       "      <td>70.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>25499</td>\n",
       "      <td>2005</td>\n",
       "      <td>500</td>\n",
       "      <td>Cincinnati Financial</td>\n",
       "      <td>3614.0</td>\n",
       "      <td>584</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       Year  Rank                Company  Revenue (in millions)  \\\n",
       "25495  2005   496        Wm. Wrigley Jr.                 3648.6   \n",
       "25496  2005   497         Peabody Energy                 3631.6   \n",
       "25497  2005   498  Wendy's International                 3630.4   \n",
       "25498  2005   499     Kindred Healthcare                 3616.6   \n",
       "25499  2005   500   Cincinnati Financial                 3614.0   \n",
       "\n",
       "      Profit (in millions)  \n",
       "25495                  493  \n",
       "25496                175.4  \n",
       "25497                 57.8  \n",
       "25498                 70.6  \n",
       "25499                  584  "
      ]
     },
     "execution_count": 5,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.tail()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [],
   "source": [
    "df.columns = ['year', 'rank', 'company', 'revenue', 'profit']"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "25500"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "len(df)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "year         int64\n",
       "rank         int64\n",
       "company     object\n",
       "revenue    float64\n",
       "profit      object\n",
       "dtype: object"
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.dtypes"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>year</th>\n",
       "      <th>rank</th>\n",
       "      <th>company</th>\n",
       "      <th>revenue</th>\n",
       "      <th>profit</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <td>228</td>\n",
       "      <td>1955</td>\n",
       "      <td>229</td>\n",
       "      <td>Norton</td>\n",
       "      <td>135.0</td>\n",
       "      <td>N.A.</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>290</td>\n",
       "      <td>1955</td>\n",
       "      <td>291</td>\n",
       "      <td>Schlitz Brewing</td>\n",
       "      <td>100.0</td>\n",
       "      <td>N.A.</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>294</td>\n",
       "      <td>1955</td>\n",
       "      <td>295</td>\n",
       "      <td>Pacific Vegetable Oil</td>\n",
       "      <td>97.9</td>\n",
       "      <td>N.A.</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>296</td>\n",
       "      <td>1955</td>\n",
       "      <td>297</td>\n",
       "      <td>Liebmann Breweries</td>\n",
       "      <td>96.0</td>\n",
       "      <td>N.A.</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <td>352</td>\n",
       "      <td>1955</td>\n",
       "      <td>353</td>\n",
       "      <td>Minneapolis-Moline</td>\n",
       "      <td>77.4</td>\n",
       "      <td>N.A.</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "     year  rank                company  revenue profit\n",
       "228  1955   229                 Norton    135.0   N.A.\n",
       "290  1955   291        Schlitz Brewing    100.0   N.A.\n",
       "294  1955   295  Pacific Vegetable Oil     97.9   N.A.\n",
       "296  1955   297     Liebmann Breweries     96.0   N.A.\n",
       "352  1955   353     Minneapolis-Moline     77.4   N.A."
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "non_numberic_profits = df.profit.str.contains('[^0-9.-]')\n",
    "df.loc[non_numberic_profits].head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "{'N.A.'}"
      ]
     },
     "execution_count": 10,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "set(df.profit[non_numberic_profits])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "369"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "len(df.profit[non_numberic_profits])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "bin_sizes, _, _ = plt.hist(df.year[non_numberic_profits], bins=range(1955, 2006))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "metadata": {},
   "outputs": [],
   "source": [
    "df = df.loc[~non_numberic_profits]\n",
    "df.profit = df.profit.apply(pd.to_numeric)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "25131"
      ]
     },
     "execution_count": 14,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "len(df)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "year         int64\n",
       "rank         int64\n",
       "company     object\n",
       "revenue    float64\n",
       "profit     float64\n",
       "dtype: object"
      ]
     },
     "execution_count": 15,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.dtypes"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "metadata": {},
   "outputs": [],
   "source": [
    "group_by_year = df.loc[:, ['year', 'revenue', 'profit']].groupby('year')\n",
    "avgs = group_by_year.mean()\n",
    "x = avgs.index\n",
    "y1 = avgs.profit\n",
    "def plot(x, y, ax, title, y_label):\n",
    "    ax.set_title(title)\n",
    "    ax.set_ylabel(y_label)\n",
    "    ax.plot(x, y)\n",
    "    ax.margins(x=0, y=0)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAbMAAAELCAYAAABTdGifAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4xLjEsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy8QZhcZAAAgAElEQVR4nO3deZhcVZn48W9V73vSnU46+0peIIGEHdlRQVQQXFFZXFEcR8YZZxzHcRsdHcefy4zACCoqyiIIisgOKkvYQUhIIG+27qSTdJLe966qrqrfH+dWd6XTS3V3dWrp9/M8/XR1nVu3Tp2+dd97lnuOLxqNYowxxmQyf6ozYIwxxkyWBTNjjDEZz4KZMcaYjGfBzBhjTMazYGaMMSbjWTAzxhiT8XJTnYFsJSIPAr9V1ZtTnRdjMpGInA78CpgLXA58miR9p0TkP4GrgX5VrZns/kzq+VJ5n5mI1AGfVNXHUpYJkzAReRw4FeiPe/o8VX12gvu6RVV/npzcjeu9PwrcBPTGPX2hqj7upS8BfgmcAuwC/j7+GBWRfwT+FSgC7gY+o6qBw5H36URE/gzcq6r/O0zaR3HnjjMmsN+FwBZgsaoemHRGx//++cBtwInAYuDc2LHnpc8A/hd4u/fU/6nqN+LS64A5QNh76hlVPd9L+yijHNtD8rEEqAXyVLV/aHoCn+NU4FvACV5eHgeuUdUGL90HfBf4pPeSm4B/VdWol77We+4o4A3gE6r6qpf2DeDfgfjv1bGqumOk/GRdzUxEcifyjzEJ+/vJBCDvAPclMT8T9ewoJ8LbgWeBd3g/d4nIEaraKCJvA74EvBnYC/wB+A/vOZOgBL+ni4FNU/D2i4HmkQLZYTqHrAP+B/jdMGk/AoqBJcBs4M8islNVfxm3zUWjVAJGO7aTaSbwU+Bh3AXudbiLwAu89E8BlwBrgCjwKLADuMEL6H/ElcH/4Wrdf/S+Z0Hv9Xeo6uWJZiZtglnsSgt4DvgE0Ab8nao+6KVXAj8A3oa7In5CVS8RkXOAW4BrgX/EFdgVInIh8J+4A+J14GpV3eDt60vAVbgDpR74d1X9g5e2Ane1sBYIAX9W1Uu9tCO99zkBaAS+qqp3jvB5HsereYz12YZ5bR1wPXAFsBz4LfBlXJPLGcDzwPtVtdXb/lTgh8DRwE7gH+JqGR8Dvggs8PL836p6o5cWK7sf4WoaYeDLQ740CRGR03BXkytxV73/oKrPxJXF08A5wPHA74EzgVNF5H+8z/V9hlwljqcMRaTCK4N3ABHcl+rrqhq7ek30c6z08ni+qvYCd4vI54H3AjcAHwFuUtVN3vbfAm5lhGAmImcA38P9bzpxx8yvvPxei7v67gF+BnxHVSPeZ70KeAH4GNCCa2ZbibsSLgD+JdbcJiK/Avpwx8qpwN+AK1V1p5f+v8B7gApgK/B5VX3KS/uGl7c+4N24muhHVPUlEfkX4FRVfW/c57kWCKvq54f5rHXAjbjjdi5wD67W2jfK9/Qq3LFXiTvBX62qe0VkO7AU+JOIhIEq3EnzFtyxdAOQJyJduKbCGSLyDtxxtBDoAH6kqt8fkse3An8CCrzX3gV8A3fsfRL4OlAHnCUi7wL+C5gPvOp9ljfiPmvC39F43sn6f7z9DHd8XgS8XVV7gDoRuQn4OO6YTqYnvd9tIgJwnpfvL+OOvyLgIeBzqto+zOc46PwlItcBT8Q99RHgB6q620v/gbffG3Dnglzgf7ya2o9F5J9xF4kPTeTDpNsAkFMABWbhTgA3eVfyAL/BXa2swgWhH8W9rgb3ZVgMfEpEjgd+gYv2Vbgv2L0iUuBtvx13Mq3AXVXfIiJzvbRvAY/grjoW4L58iEgJ7gt4m/f+HwL+T0RWJeGzDee9uINrJe7gfhB3kM3C/d+u8fI1H7gfF7grgX/GnYCrvf0cAC4EynEnxh955RNT45XDfFyQuF5EZib4mfDyUOnl4ce48v4hcL+IVMVtdgXuSq0M+CjwFK6WV6qqf5/gW41Whjfjrg5XAMcB5zPYvDGc40SkSUS2iMhXRSR2YbcK2KGqnXHbrveej6WvH5I2Z8hnBUBEFuH+b9cC1bgLpFe95Gtx5b4MOBu4Evf/if+sG3DleRvuZHmS9/kuB64TkdK47S/DHbuzvPe4NS7tRe+9K719/U5ECuPS3+XtfwZwL+4KG1zguMBr9sIro0tx38WRXIa74FyOO3a/Epc29Hv6Zlyw+AAu+O308oGqLscF1ou8Y2SguckLKFfjaiClqjrDS7oJ+LSqlgGrgb8MzZxXm3k7sNd77Ufjks/GNXm9zbuouR34PO5/9wAusObHbZ/Qd3SCfEMerx6SfquINIrIIyKyZkjaSMf2UGd5v2d4ZfEs7rv5UeBc3LFZyuDxMJazOLgmPdx3Jf57tCHW5OjZEJcOcJGItIjIJhH5zFhvnjY1M89OVf0ZgIjcjKt+zvFOWG8HquKudOKvACK4q/CA99qrgBtV9Xkv/WYR+TLuqvUJVY2v2t8hIv8GnIyr9oZwX7Z53hXFOm+7C4G6uFrL30TkbuB9JNYUMuxnA/aNsP21qrrf2/4p4ICqvuL9/QfgLd52lwMPqOoD3t+PishLuBrKzap6f9w+nxCRR3CB/G/ecyHgm15t6AHvalVwNaDh/FhEYle7O1T1eOCdwFZVjZ3kbheRa3Bf8F95z/0qVpvxPsMIux/VSMdHFHd8zPBqU90i8iNc8LxxmP08iTs57MR9ee7ABcL/wn15h16FtuOCPcOkxx6XAc1DXncZ8Jiq3u793Qw0i0gOLigc5wXNTu+q9QrcCRmgNnasicgduP6Db3rH+CMiEsQFtlhwvF9Vn/S2/3egXUQWqmq9qt4Sl6cfiMhXcP/j2IlmXez4EZHf4E7gqGqDiDwJvB9Xc7wAaFLVlw8p0UHXqWq9t69v44J2LKAN/Z5eBvxCVf/m/f1vQKuILFHVulHeYyQh4GgRWe+dJw6pFY3hG6ra7eXlUlyZPur9/X3gH4DTcH1DkPh3dLweAr4kIh/BnSM+jruQj7kM9/31eXl6WESOVNU2Rj+2E3EZ8MNY35T3P9koIh8brelVRI4FvgZcHPf0cN+VUu98PtL3rMx7fCeuCXM/7sLubhFpi/suHSLdgtnAiV1Ve7wTXinuaq5luCq7p1FV++L+Xgx8REQ+F/dcPjAPQESuBP4J1wQZe49Z3uMv4q5wXxCRVlw1+RfePk8Rkba4feYy+lVqIp9tJPvjHvcO83fstYuB94vIRXHpecBfAUTk7bimk5W4q8Vi4LW4bZuHHKQ9Y+TrmmH6zObhvjzxdjIYAMA1507WaMdHHtAQFyT9I73nkE7k10Tkm8C/4L7wXbhabLxyXBMhw6THHndyqIW4VoChZuGOx/gyG1peQ//fxE6ccc/F/58GPquqdolIC+7/Ui8iX8DVUufh+i7KGTze4eALqh6gUAb7jW4GPoMLZpcz9vEeX+Y7vfeMGfo9ncfgRVUs3824cqgb432G815c4PyuiGwAvqTjG5wUn/eDjmmv+bee0f9Ho/1/xuMa3EXAVtwF0O24lqBYXp6O2/a/vKB3JvCnMY7tRAz9Lu/EnefmAHuGe4G4rpkHcV0LT8UlDfdd6VLVqHfRPOL3TFVfj3v+Ga+p/H24shhWugWzkdQDlSIyw7v6GGrokMx64Nuq+u2hG4rIYtwX8y24ZoqwiLyKV61X1X24dt1Yf8dj3tVpPa5Wd16yPlSS1AO/UdWrhiZ4zap345qw/qiqIRG5h+QPwNiLC6rxFnFw2/fQ/9HQv7u938W4/g5wzVKJqMeNepo12tXjKKIMlskmYJmIlMU1Na7BNc/F0tfgrhxjaftVdWitLJavk4d5vonBFoDYl3YRI5wsErQw9sBrfqwE9orImbg+qbcAm7yTciuJHwP3AD8RkdW41okvJpoP3GfaG/f30P/5QceN15RfRWLlcMgwbFV9EbhYRPKAv8f9jxYO3S7Bfe4FjonLm8/b12T+RwlR1RZcDSn23t/B9Z+OJP74HW/aUEO/y4twNbv9w2wbO58+BnwrrmUmJvZdieV9DYOtWJuAL4iIL66p8VhcP+R4PweQIcHMa+54ENdH9VlcxH9TrFllGD8D/iAij+EKshjX4fgkUIIrmEYYGCAx0B4tIu/HBbnduGaKKG5gxH24K74r8Nr1cf0QXbFO4RS5BXhR3Ci7x3A1lFOBbbhqewHus/Z7tbTzgY1JzsMDwLUi8mHcCeS9uEEF943ymv24NnkA1I0U3ANcLiI34jqPlyfy5t7x8QiuCe2ruONjKbBAVZ8Yur1XDn9T1f3iBvV8FW9Umapu8S5uvu41x70d9yWLDYL4NfArEbkVaMDVBH41QtZuBb4sIh/ADXqpABaq6qsicifwba+VoBLXUvD9EfaTiHd4F18v4FoWnlfVehE5BncyagRyxQ1+GnpFPCJv8MZduGD+gqruGuMlnxWR+3A1vC/jmrlGchvwWxG5DTc0+ztevusSyNp+YIGI5Ktq0OvLej9wn6q2i0gHg0PXJ+JOXFPfW3DnjX/AXTA9M4l9DvAuNGMn53xxfZgBr9ayHDfAqQ33ff0Urj8v1g+7ENcP6gc+h6tlP+2lj3hsD6MR1/S7DDdoC1zN51+9820j7n9yx3AXieL66/8CXK+qNwyz/18D/yQiD+DOo1/AG4OAa6oNA9eIyA14FQhvf4jIxbhyb8P1FV+DO55GlG4DQEZzBe5qdjNuUMMho6liVPUlXOFchwtI23CdmrHq6w9wQ6/3466+4qvtJwHPe9Xge3FV51rvKv184IO4q5d9wH/jgkXKeP0TF+P+0Y242sC/AH4vz9fgvpitwIdxnynZeWjGXbV/Adcs8kXcvS1No7zsf4H3iUiriPzYe+4qL+/NuPb+8Zw4rsQ13b2O+6x34QYVDOctwAYR6cYF4t/jvrQxH8TdA9SKu0/mfara6H3Wh3CDT/6Ka4LZiWvGPYR34n8HrlxacP1bsc76z+Fqoztw/bK34QYtTdRtXj5acKNtY1f2D+OagLZ4ee1j/E2+N+O+J4k0qd+GG0C1w/v5z5E2VNU/4062d+MuDJbjyj4Rf8Fd3e8TkdhxdgVu9F8HboBIwsO6h8mbeq+/FleTvgg3GCU46gvH8Ra4psj5uP9RL4M1ohNwXQGduObBy+L6m8uAn+COzT24fsy3x7UMjHVsx3/GHuDbwNMi0iZuVPQvcP/nJ3EjPPtwx+pwPokLhF8Xka7YT1z6jbiRo6/hLqDv956Ljei8BPe9bcP1C14SV74fxJ23O3FB8b91jJvlU3rTtDFm8sQNzd+tql8Za9sJ7n8R7iKyRlU7RtmuDpsEwaRIJtXMjDGHmYj4cU2gvx0tkBmTahnRZ2aMOfy8ARn7cc2TF4yxuTEpZc2MxhhjMp41MxpjjMl407WZsQA3arGByQ3fNcaY6SQHN0r4RQ6e0T7lpmswOwk3N6AxxpjxO5PBqf7SwnQNZg0Ara3dRCKp6zOsqiqlublr7A2nASuLQVYWg6wsBqW6LG57bCtt3QG++vFTwTuHppPDEsy8STrfi5sL8RhV3eg9vxJ3Q2YV7kbZK1V162TSEhQGiESiKQ1msTwYx8pikJXFICuLQaksi5c37+e4lbNjf6Zd98zhGgByD255gKGT0d6AmwplJW5OrhuTkGaMMSaJWjr6aO4IsKSmbOyNU+Sw1MxUdR0cvOyHiMzGLYIYm7j3dtwaTdW4OcvGnRabcsgYY0zybNvjVmtZnMbBLJVD8xcCe9RbCdj7vdd7fqJpxhhjkmzr7nby8/zMm1U89sYpMl0HgACuQzXVqqvT90rncLOyGGRlMcjKYlCqyqJufydHLq5kdnXCCy4cdqkMZvXAfBHJ8dYUy8FbTBDXlDiRtHFpbu5KaYdqdXUZjY3Drek4/VhZDLKyGGRlMShVZdEX7Kd2TwfveNNimpu70qISMJyUNTOq6gHckhixFVQ/BLyiqo0TTTt8uTfGmOmhdm8HkWiUIxZUpDorozpcQ/N/DLwHt3LwYyLSrKqrcGsO3SwiX8Otz3Nl3MsmmmaMMSZJtu5pxwcsn2fBDFW9BrdI5NDnNwOnjPCaCaUZY4xJnm2725lfXUJxYXoPsbCJho0xxgwrEomyfW87K+and60MLJgZY4wZwZ6mbnoDYVakeX8ZWDAzxhgzgm272wBYsWBGinMyNgtmxhhjhrV1TzsVJflUVxSmOitjsmBmjDFmWNt2t7NiQQU+ny/VWRmTBTNjjDGHaO0M0NTexxEZMPgDLJgZY4wZxnZvcuFM6C8DC2bGGGOGsXV3O/m5fhbNSc/pq4ayYGaMMeYQ2/a0sXRuObk5mREmMiOXxhhjDptAKMyu/V0ZcX9ZjAUzY4wxB6nd20E4Es2ImT9iLJgZY4w5yFZv8MdyC2bGGGMy1bbd7cybVUJpUV6qs5IwC2bGGGMGRKJRtu/JjMmF41kwM8YYM2BvUzc9gf60X4xzKAtmxhhjBmwbuFnagpkxxpjDpLsvRCQSTdr+tu1up7w4j9kzipK2z8PBgpkxxmSolo4+/vn6Z3hyw96k7XPbnnaWz8+MyYXjWTAzxpgM9ciL9QRCYRrbepO2z5aOPmoqi5O2v8PFgpkxxmSgrt4QT7zqamQ9ff1J2Wc4EqE/HKUgPycp+zucLJgZY0wG+vPLuwmEwhTm59CdpGAWCEYAyM/NvGCWm+oMGGOMGZ9AMMxjL9WzdsUsOnuC9PSFkrLfYH8YwGpmxhhjpt4T6/fS3dfPO960mOLCvOTVzEJeMMvLvNCQeTk2xphprD8c4eEXdrFy4QxWzK+gpDA3aTWzQDAWzKxmZowxZgo9u2kfrZ0B3vmmxQAUF+YmbQBIMOT6zCyYGWOMmTKRSJQHn9vFotmlrF5aCUBxYR49ff1EopO/cTrWzJhvwcwYY8xU+duWRva19PCONy0euKm5pDCXKNAXmHztLBiyZkZjjDFTKBqN8sBzO5k9o4gTZfbA88WFblB6MgaBDNbMMi80ZF6OjTFmGlq/tZG6fZ1ccOoi/P7BqaZKCt2aY8noNwtYzcwYY8xU+t2ft1JRms/pq+ce9HzJQM1s8iMaA7EBIHafmTHGmGTbsbeDDduaOP+kheTlHnzaLraaGWDBzBhj0t6jL9VTUpTHOWvnH5KWzJpZMBTG7/OR48+sGfPBgpkxxqS9zbtaOemoORQVHDoDYWwASLJqZgX5/oxb/gUsmBljTFpr7QzQ3hXkiIUzhk0vyMshx+9LymjGYCickfeYQZpMNCwiFwLfAny4APsNVf29iKwEbgaqgGbgSlXd6r1mxDRjjMkWtQ0dAByxcOaw6T6fz5sFJDkDQDKxvwzSoGYmIj7gN8AVqroWuBy4WUT8wA3A9aq6ErgeuDHupaOlGWNMVqht6MDv87F0fvmI2yRrsuFAMGzBbJIiQIX3eAbQAMwCjgdu956/HTheRKpFZPZIaYcvy8YYM/XqGjqYX11CYf7IDWnJmmw4EApn5A3TkAbNjKoaFZEPAH8UkW6gDHgnsBDYo6phb7uwiOz1nveNktaY6HtXVZUm98NMQHV1WaqzkDasLAZZWQyazmURjUbZub+L046dB4xcFjPKC+noDk66rKJAWXFBRpZ5yoOZiOQC/wZcrKpPi8jpwB3AFVP93s3NXUQik5+cc6Kqq8tobOxM2funEyuLQVYWg6Z7Wexv7aGrN0TNzEKAEcsiz++jozMw6bLq6glRlJ8z4n78fl9aVAKGkw71ybXAPFV9GsD73Q30AfNFJAfA+z0PqPd+RkozxpisEBv8sbRm5P4ycMPzk3WfmfWZTdxuYIGICICIHAXUAFuBV4EPedt9CHhFVRtV9cBIaYc158YYM4XqGjrJy/Uzv7pk1O1KCnPpCUx+GZhABg/NT3kwU9V9wGeAu0RkPfBb4GOq2gJcDXxORLYAn/P+jhktzRhjMl5tQweL5pSSmzP6qbq4II9oFPoC4Um9nw0AmSRVvRW4dZjnNwOnjPCaEdOMMSbThSMRdu7v5Cxv8MdoSgZmAQkNzAgyXtFolKDdZ2aMMSaZGpp6CIYiLJ07en8ZDE42PJl7zfrDUSLRqAUzY4wxyRMb/LFk7tjD5ONrZhOVyTPmgwUzY4xJS7X7OikqyGFOZfGY2yZjtelgLJhl4FpmYMHMGGPSUm1DB0tqyvEnMIP9wGrTgYkHs1jNLFMHgGRmro0xJouF+iPsPtCVUBMjxNfMJt7MGIytMp1rNTNjjDFJUH+gi3AkOubN0jGF+Tn4fb5JrWk2UDOzZkZjjDHJMDDzRwIjGWFwGZjJ9JnZABBjjDFJVdfQQXlxHpXlBQm/ZrIz5weCFsyMMcYkUe2+TpbMLceXwOCPmMmuaTZYM8vMsJCZuTbGmCzVG+inoak74SbGmMnWzIIDoxmtZmaMMWaSdu3vJAosTXAkY8zk+8y80YwZGswSmsRLRBYCa3CrQLcB61XVllsxxpgkq21wa4ktGXfNLG9SoxmDGT4AZMRgJiJ5wKe9n2XANqATtxL0ChGpBW4AfqqqwcOQV2OMyXo7GjqoKi+kvDh/XK8rLsylp6+faDQ6rr62mEAoTG6OH79//K9NB6PVzNYDf8EFs+dVdWBtAW8xzJOBy4BXgFVTmUljjJku6ho6xt3ECK5mFolG6QuGKSoY/8z5gVA4Ywd/wOjB7BxvEcxDeIHtWeBZEamekpwZY8w009ETpKm9j3OPmz/u18bPAjLhYJahN0zDKANARgpkACJSJCL53na2urMxxiRB3QT7yyB+5vyJ9ZsFQxHyM3QqK0hwNKOIfF9ETvYevxNoAdpE5KKpzJwxxkwndQ0d+IAlNeNvZpzsmmaumTHLgxmub2yj9/hrwOXAu4DvTEWmjDFmOqpt6KCmqnhCzYSTXdMsmMV9ZvGKVbVHRKqAZap6N4CILJ66rBljzPQRjUap3dfJqiWVE3r9ZNc0C4TClBTlTei16SDRYLZFRC4DVgCPAojILKB3qjJmjDHTSWtngI7u4IRGMkLcmmYTDmYRKsszt5kx0WD2d8D/AkHgE95zbwMemYpMGWPMdLNhRzOQ+Ez5Q8WWgZnommbBUDijB4AkFMxU9UXgtCHP3QrcOhWZMsaY6aK7L8Sdf9nGUxsamDerhEVzJlYziy0DM/GaWWYPzU+4l1FEBDelVWn886r6i2Rnyhhjsl00GuVlbeTWR7fQ0RPkglMWcfEZS8nLnfggDDc/48RqZtl80/QAEfkybhTjeqAnLikKWDAzxphxaO0McMsjyitbm1g0u5TPv38NiycwHH+okgnWzCLRKMFQJKOH5idaM/s8cLKqbpjKzBhjTLZ7cv1e7vjLVvrDUd5/znLOO2khuTnJqRFNdE2zUIbPmA+JB7NeYPNUZsQYY7Ldc6/v41cPbubIRTP4yAVHMqeyOKn7LynMpalt/IPMAxm+lhkkHsy+ClwrIt8A9scnqGok2Zkyxphs09LRxy0Pb2H5vHK+8MG15PiT3z810ZrZ4MKcWd5nBvzK+/3JuOd8uD6zzA3lxhhzGESiUW66/w36IxE+edHRUxLIYLDPbLzLwAQyfC0zSDyYLZ3SXBhjTBb788u7eWNnK1deIMyZmdymxXjFhbkTWgYm01eZhsTvM9sJICJ+YA6w35oXjTFmbHuburnr8e0cu7yKs9fMm9L3ip8FZHzBLPNrZonOml8uIr8G+oA9QK+I3CwiFVOaO2OMyWD94Qg/+9PrFOTl8LG3HzmhFaDHo7hgcE2z8RgIZhl803SiDbc/BkqA1UARcAxQ7D1vjDFmGPc+XcfO/Z185AKhorRgyt9vomuaDQwAmcQN26mWaD30Atxs+bEbpreIyMeA7VOTLWOMyWzb97Rz/7N1nL66hhNk9mF5z4muaZYNzYyJBrM+oBrYGffcLCCQjEyISCHwI+Ct3ns9q6qfEpGVwM1AFdAMXKmqW73XjJhmjDGpFAiG+dl9r1NZVsiH3rrysL3vRNc0C3oDQPKnQTPjz4FHReRqEXm7iFwNPAz8NEn5+B4uiK1U1WNw97UB3ABcr6orgeuBG+NeM1qaMcakzF2Pb6extZdPXnjUwDpjh4PVzMb2bWAv8GFgnvf4eyRhXkYRKQWuBBaoahRAVfeLyGzgeOA8b9PbgetEpBp3j9uwaaraONk8GWPMRPWHI6zb2MBpq2uQRTMP63sXFuTg80FPYJwDQILTpM/MCzK/YGomFV6Oayb8uoicC3QBX8FNobVHVcNeHsIishdYiAtmI6UlHMyqqkrH3miKVVdPfnLRbGFlMcjKYlCmlcVr25oIBMOcc9KipOc9kf2VFuURwTeu987Jy6EgP4fZsye2llo6GDGYicgVqvob7/HHR9ouCUvA5ALLgFdU9V9E5BTgT8D7J7nfMTU3dxGJRKf6bUZUXV1GY2Nnyt4/nVhZDLKyGJSJZfHUK/Xk+H3Mm1GY1LwnWhZF+bk0t/WO673bOvrIz/WP+Rq/35cWlYDhjFYz+xDwG+/xFSNsk4wlYHYC/bimQlT1eRFpwtXM5otIjlfzysE1cdbjamYjpRljTMps3NHCEQsqxnXTcjJNZE2zQDCc0f1lMEowU9V3xD0+d6oyoKpNIvJXXP/XI94oxdnAFuBVXFC9xfv9SqxPTERGTDPGmFRo7QxQf6CL952zPGV5mMiaZsFQFgczb+qqMSVpWqurgV+IyA+AEHCFqrZ5oyZvFpGvAa24gSLxrxkpzRhjDrtNtS0ArF5ambI8FBfm0dQxvrumAqFwRi//AqM3M/bjmhFHkrRZ81V1B3DOMM9vBk4Z4TUjphljTCpsrG2moiSfhbNT16/kambjvc8sTEEGL/8CowczmynfGGMSFIlE2VTbwtojZk35HIyjKS7MG/cyMIFQhIrS/CnO2dQarc9s50hpxhhjDrajoYPuvn6OWVaV0nyUFOYSjkQJhMIU5ic2CCWQ5X1mv2H0ZkYAVNX6qowx097GHc34fHD0ktT1lwEDM4709PVbMPNsO2y5MMaYDPfajhaWzS2ntCgvpfkoiZvSqjLBe6CzejSjqv7H4cyIMcZkqs6eIHUNHbzrjNQPNSiewGTDgVCY/PwsHQAiImep6pPe4+F3ae4AACAASURBVDePtJ2q/mUqMmaMMZliU10LUWD1stQ2McLBNbNEhCMR+sNRCnKztGYG/B9uMU6Am0bYJoqbisoYY6atjTtaKC3KY2lN6uc2jNXMEp0FZGD5lyxuZlwd9zj1dWdjjElDkWiUjbUtrFpaid+fuiH5MeNdbXpg+ZcMXssMEl/PzBhjzDDq93fR0R1M6awf8QoLcvGReDPj4FpmmR0OEhq3KSJrcCtBrwVit7b7gKiqZvaddsYYMwkba5uB1E5hFc/v81E8jllAYmuZZe1oxiFuB+4GrsHNZm+MMQY3JH/RnFIqSgtSnZUBxeOYbDjYn+V9ZkPUAF+LrQRtjDHG9Utt39POBacsSnVWDlJcmDeBZsbMDmaJNpLeDHx4KjNijDGZ5o2drYQj0bRpYowZz2TDwWnWzPhd4FkR+TKwPz5BVUe8B80YY7LZxtpmCvNzWD6/ItVZOUhxYR4tCS4DE6uZ5U+HASDAXUAt8Aesz8wYY4hGo2zc0czRSyrJzUmvQDCemlm2NDMmGszWAlWqGpzKzBhjTKZoaO6huSPAO09LryZGcANAuhNcBiZ20/R0uc/sKeDoqcyIMcZkkle3NQHpMyQ/XklhHuFIdCBQjWagmTGLp7OKVws8IiJ/4NA+s68lPVfGGJPGegP9PPzCLmThDGZVFKU6O4eIn9JqrBpXIBTG7/ORm5P62UsmI9FgVgzcD+QDC+Oet6H6xphp5+EXdtHZE+L971uR6qwMKzbZcE8Cy8AEQmEK8v0pXR07GRIKZqr6sanOiDHGZIK2rgAPvbCLk46czbJ5qZ9YeDjjmWw4GApn/A3TMEqfmYjMTmQHIjInedkxxpj0du+6WsLhKO85O30XDBnPZMPBUCTjRzLC6DWzv4rIE8BvgOdVdaAnUUT8wMnAlcBZDC4VY4wxWauhuZsn1zdw7vHzmTOzONXZGVHxONY0C4TCGT/4A0YPZscBnwJ+CiwTkR1AJ1CGW8NsK3Aj8PmpzqQxxqSDux7fTn6en4tOX5LqrIyqZByrTcf6zDLdaOuZBYHrgOtEZCFwDDADaAU2qOqew5NFY4xJva2723hlaxPvPmsZ5cXpvVhI0TiWgQmEwlnfzDhAVeuB+inOizHGpKVoNMrv/rqditJ8zj9x4dgvSDG/z0dRQWIz5weCkbQPzonI/LqlMcZMsb9taWLbnnbefeayjJkpo7gwl+5AYqMZs6FmZsHMGGNGEY5EuPuJ7cytKub0Y2pSnZ2ElRTmJVYz68/yofnGGGPgqfUN7Gvp4X3nLCfHnzmnTDc/Y6L3mWXO5xpJQp9ARP55hOf/KbnZMcaY9BEIhrlnXS0rF1SwdsWsVGdnXEoSWG06Go0SCGbHfWaJhuOR5l/8SrIyYowx6aa2oYOO7iAXnLo446Z7SmS16f5wlEg0mhXBbNTRjCISW3gzR0TOBeL/m8tw950ZY0xWau1yC1zOmZl+kwmPJbam2WjLwGTLWmYw9tD8m7zfhcAv4p6PAvuAz01FpowxJh20ecFsRmlBinMyfsWFufSHowT7R25GDMaCWYaM0BzNqMFMVZcCiMivVfXKw5MlY4xJD62dAQrycygqSHSBkfQRP3P+SMFscC2zzB8AkuhN04clkInI14FvAMeo6kYRORU3ZVYRUAdcrqoHvG1HTDPGmGRo6woyMwNrZQClRS6YdfYEmVk2/GcYWGU6C5oZR5s1/424x/Uismu4n2RlRESOB04Fdnl/+4BbgM+q6krgSeC7Y6UZY0yytHUGmFGambNjxAJYa2dgxG0GamZZ3sx4Vdzjy6cyEyJSAFwPfBj4q/f0iUCfqq7z/r4BVwP7+BhpxhiTFG1dAY5YUJHqbExIZXkhAC0dfSNuM10GgHwfV1MCOEdV/2MK8/FN4BZVrRWR2HOLgJ2xP1S1SUT8IlI5WpqqtkxhPo0x00Q0GqWtK5CRgz8AKkryyfH7aBmlZhacJsFspYgUqmof8AVgSoKZiLwJOAn40lTsfzRVVaWH+y0PUV1dluospA0ri0FWFoNSVRbtXQH6w1EWzC1Pm//HePNRVVFIdyA84uvyd7YBUDOnjOpZqT8fTsZoweyPwBYRqQOKROTJ4TZS1bMmmYezgSOBWK1sAfAw8GNgcWwjEZkFRFW1xeurGzZtPG/c3NxFJBKdZPYnrrq6jMZGu1UPrCziWVkMSmVZ7Nrv3jcP0uL/MZGymFGSz97GrhFf19TSDUB3Zx+N0bHPhX6/Ly0qAcMZbT2zj4nIGcASXM3pppG2nQxV/S5xgze84Hkh8DrwKRE5w+sbuxq409vsZVyAHS7NGGMmra0rCMCMEUYCZoLK8kK27WkfMT0QnB7NjHiBYp2I5KvqzYcpT7H3jojIFcCNIlKIN/x+rDRjjEmGwRumM3M0I7hg1rr5AJFIFL//0FlApkuf2QBV/YU3ndUVwHxgD27Axl+SnSFVXRL3+BncCtfDbTdimjHGTFZbZ+bO/hFTWV5AOBKlvXv4e80CoTC5Of5hA12mSXTW/E8Cd+CmsPo90ADcJiJXjfpCY4zJUK1dAcqK88jNydzZMQaG53cOPzw/GIpQkAXLv0CCNTPgi8B5qro+9oSI3AHcDfxsKjJmjDGp1NYZyNjZP2IqvdpYS0eA5fMOTQ+EsmNhTkh8CZgq3ICMeApUJjc7xhiTHlq7Ahk9+APc0HwY+cbpQCicFf1lkHgwWwf8UESKAUSkBPh/wDNTlTFjjEmltq5gRveXARQX5FKQl0OzBbMBV+MGW7SLyH6gDVgDfHqqMmaMManSH47Q2R3M6JGMAD6fj8ryAlo7hp8FJBgKT58+M29S3yLgrUANMA/Yq6q7pzhvxhiTEh3dQaIw4mzzmaSyvHCUmlmEkqLMW95mOGN+ClWNishrQJkXwCyIGWOyWmsWDMuPqSovoP5A17BpwVB4YJBIpku0fvkKsHIqM2KMMekidsN0VtTMygrp6A4S6o8ckpZNoxkTrV8+DjwkIr8C6oGBSbxU9RfJz5YxxqRONtXMYveatXb2MXtm8UFpgVCYgixYywwSD2anA7W4SYHjRQELZsaYrNLWFSTH76O0OC/VWZm0ynIXkJs7AsMHs+kyAARAVc+d6owYY0y6aPVWmPb7Mn+ap6oRFumMRqPeDCDToGbm3Vf2FWA18Dfgv1R15JXejDEmC7RlwQ3TMbF+v6GLdAa9PrRsCWZj1S+vAy4CNgPvw60+bYwxWS2TV5geKj8vh7LivENqZgFvxvxsGQAyVjB7O3C+qn7Re3zh1GfJGGNSq60r8+dljFdZVkjLkBung8FYMMuOPrOxPkWJqjYAqGo9UDH1WTLGmNTpC/bTGwhnTTMjuEEgI9XMsqWZcawBILneOma+Ef5mKtY0M8aYVImtMJ1VNbPyQjbvaj3ouWzrMxsrmB3g4KH3zUP+jgLLkp0pY4xJlcF7zDJ7XsZ4VeWF9AbC9PT1U1zoTvuB4DSqmcWv+myMMdNBbPaPbGtmBLdIZ3FhKTD9BoAYY8y00pZFs3/EVA5zr9lgn1l2hIHs+BTGGJMkrV0BCvJzKCrIjtnk4eAVp2OybQCIBTNjjInT1pldw/LB1TL9Pt9BS8EEQ24ASH6WzM1owcwYY+K4FaazZ/AHgN/vY2ZZ/kE1s6DVzIwxJnu1dgayYumXoSrLC4ftM8vLzY4wkB2fwhhjkiAajWbVVFbxKssLaek8OJjl5/mzYjJlsGBmjDEDOntDhCPRrBqWH+NmAQkQibrlKANZNGM+WDAzxpgBsWH52TYABNz8jOFIlM5uN8NJIBi2YGaMMdkoG2+Yjomta9bsDQIJ9lswM8aYpGjvCvDQ87voDfSnOivA4LyM2TaaEeJmAfEGgbg+s+wJZtlzV6AxJuPc/JDy6rYm/vzybj7xzqM4cvHMlOanNQtn/4gZOgtIMBjOmtk/wGpmxpgUeXVbE69ua+KsNfPIzfHxvdtf4bd/3jpw/1MqtHUFKCvOIzcn+06NJYW55Of5B1acDoQiVjMzxpjJCPWHuf2xLcytKuby81cSDkf53ePbeOTFel7b0cxVFx3Nkpryw56v1iyc/SPG5/NRVV44MAtIIGR9ZsYYMykPPreLxrY+LjtvJbk5fgryc7j8fOGfLl1DXzDMt3/9Mveuq6U/HDms+WrrCmTl4I+YyrKCgVlAbACIMcZMwoG2Xu5/bicnHzWbo5dUHpS2emkV3/zEyZx01GzuWVfLl65fd8gKyVOprTM7b5iOiZ8FJNuG5qe8mVFEqoDfAMuBALAN+LSqNorIqcCNQBFQB1yuqge8142YZoxJX799bCt+n49L33zEsOklhXl86qJVrF0xi5sf2sw3f/Uin7lkNbJoageH9IcjdPSEsnIkY0xleSHt3UFC/RGvzyx76jPp8EmiwPdUVVT1WGA78F0R8QG3AJ9V1ZXAk8B3AUZLM8akr9igj3edsWTM+Q9PPmoOP/iHsykuzOP/3f4qj7xYT9SbvWIqtHvD8rNxXsaY+OH5/WGbASSpVLVFVR+Pe+o5YDFwItCnquu8528APuA9Hi3NGJOGgqEwtz3qBn2cd+LChF6zcE4ZX/3IiaxZUcVv/7yVn/3pdQLBqRntOHDDdJY3MwI0NPcA2bPKNKRBMIsnIn7gM8C9wCJgZyxNVZsAv4hUjpFmjElDDz6/i6b2Pi73Bn0kqqggl8++5xjec9Yynn99P9/+zcscaO1Jev5i95hldc3M+2wNLd0AFGTJWmaQBn1mQ1wLdAHXAe+e6jerqiqd6rcYU3V1WaqzkDasLAZlW1nsa+7mwed2cuba+Zx10uJxvTZWFh+7+BjWyBz+3y0v8a1fv8x/XHUqsjh516/9mxsBWL64Km1HNE72uCirKAKgrTsEwKzKkqw51tImmInI94EjgItUNSIiu3DNjbH0WUBUVVtGSxvPezY3dxGJTF0b/Fiqq8tobOxM2funEyuLQdlYFtfftQGfz8clpy8Z12cbWhYLq4r4ykdO5L9ueZlf/mkTX7h0bdLyWL+vnRy/j0BvgMa+YNL2myzJOi5Ki/Ko3dMOQKA3OK59+v2+tKgEDCctmhlF5NvACcAlqhpbCvVloEhEzvD+vhq4M4E0Y0wa2bA98UEfiZg9o4hz1s5nU20LjW29Scih09bpVpjOlvW9RlJZXkBDc/Y1M6Y8mInIKuDLwDzgGRF5VUT+oKoR4ArgJyKyFTgb+BLAaGnGmPTRH45w+2NbqalMfNBHIs48di4+Hzy5fm/S9pntN0zHVJYV0t3nJnbOptGMKW9mVNVNwLCXQqr6DHDMeNOMMRPX2NbLrY9u4W0nL+KoSU78++hL9exv7eUfP7AmqfMdVpYXcuyyKta91sDFZyxNyr7bugLMm1WShNylt9hSMJBdwSzlNTNjzPiF+sNs29POIy/s4oY/buRbN7/I3qbuSe+3syfID+9cz4btzfzP79zviWrrCnDv03WsWV7FMcuqJp23oc5aO4/2ruCk8hgvm+dljBe71wzIqpumU14zM8aMLhKJ0tDSw679ndTu7WD73g527e8k7A1eqiovoCfQz033v86XrziBHP/ETlDBUJgf372B5vY+PveeY/jj07Vce/cGrr54NSdI9bj3d/fj2+nvj/DBtww/08dkHbu8ihml+Tzx6l6OXzn+/MXrDfTTFwxPj2bGLK2ZWTAzJo2EIxG21reyfvN+du3vYtf+TuobuwiG3IS7+Xl+ltaUc/7JC1k2t4Jl88qZWVbAi5sP8JN7NvLAc7u46LQl437fSCTKjfduYseeDv7u3as5bmU1smgGP7pzPT+5ZyNXXXQ0pxw9J+H9bd/bztMb9/H2Uxcxp7J43PlJRI7fz5nHzuO+Z+poau9lljfsfCJiN0xPv5qZBTNjTJIFQmF+dOd6ttS3AVBUkMOi2WWcvWY+i+aUsnhOGXNnFQ9b8zrpyNm8fNRs7l1Xy5rlVSyak/i9Q9FolNse28IrW5v48FuP4ASZDUBxYR7/dOlafnzXBn567yaC/WHOPHbemPuLRKPc9ugWKkrzufBNSxLOx0ScuWYu9z1Tx7oNDVxy5rIJ7yebV5geKlv7zCyYGZMGQv0Rrvv9a2zd3cZVl6xm+ZxSZs0oGtcw8cvPFzbvauPn973B1z56YsKDIh56fhd/+dseLjh5EW8dMuKwqCCXz39gDdf9/jV++cBmQv0R3nz8glH398xr+6ht6OSTFx5FUcHUnmJmVRSxelkVT21o4KLTl0y4ibUttsL0NGhmrCjNx+cDHz5yc7LnNoTs6f0zJkOFIxF+eu8mNtW28NELjuRdZy5n9szicd/vVFqUx0cvOJLdjV3c+3RdQq95btM+fvf4dk4+ajbvO3f5sNsU5OVwzXuPZe2KWdzyyBbue6ZuxNWgewP93PXEdpbPK+fUVTXjyv9EnbVmHq2dAV7bPq45Ew4yHeZljMnx+5lZVkBBvh9fFt1TZ8HMmBSKRKP88oHNvLylkQ+95QjOXDN2M95o1h4xi9NX1/DAszupbegYddtNdS3cdP8bHLloBp9459GjBs+8XD9/9+7VnHzUbH7/5A7+8bp1/PKBN9BdrUTiZrL/09N1dHYH+fB5Kw/bzcdrVlRRUZLPE6/umfA+WjsDFObnTHlNMl1UlhVmVX8ZWDOjMSkTjUa5/dGtPLNxH5ecuZTzTkrOTcUfeusRvL6zlZ/f9zrf+NhJ5OUefNLa3djFfc/U8eIbB5hXXcLfv+cY8nLHvq7NzfHz6Xet4uw183hm0z5e2HyApzY0UFVeyJtWz2HF/Bk8+lI9px87l6Vzy5PyWRKRm+PnjGPn8sBzO2np6DtotF6i2rqye1HOoeZWFRPsn5rVB1LFgpkxKfL7J3fw57/t5oKTF01oBOJIigvz+Ng7juSHd6znD0/W8oE3rwBg1/5O/vR0HS9vaaQwP4d3vGkxbzt5EcWFeQnv2+fzcdSSSo5aUsnl54V5ZWsjz2zcx/3P7iQa3UlRQQ7vPXv45sqpdNaaedz/7E7WbWjgXWcsHffrW7sCWT1b/lCXvvkIC2bGmMm7/9k67n92J2evncf7z12e9L6L1UurOGftPB5+YRdzKotYv62ZV7c1UVSQy7tOX8JbT1xIaVHiQWw4Bfk5nLqqhlNX1dDWFeCFNw4wr6qYipLDPyKwekYRq5bM5MkNe7nwtCX4/eMrz7bOACsXzpii3KWf4sJcirPs9J9dn8aYNNfeFeDuJ3ewbkMDpxw9hyvOlynrhH//uSvYWNvCzQ8pJYW5vPvMpbzlhAXjqoklakZpAecnqZl0os5eO5//u2cjG2ubOXb5rIRf19EdpLljekxllc0smBlzGIT6Izz6Uj33PVNHqD/CBScv4j1nLxt3DWI8igpyueZ9x6K72jhtdU3WD25Ye8QsyovzeOLVveMKZrH7+mTR5OahNKmV3Ue3MSkWjUZ5ZWsTd/xlK41tfaxdMYtL37xiymbFGGpBdSkLqtNz/alky83xc/qxc3n4+fpxDejQ+jby8/wsqcmORSqnKwtmxkyBaDTKrv1d3PnXbbyxs5X5s0r4wqVrWbU0eSsjm0O96egaHnxuF69tb074Ngfd1cbyeRVJndXfHH4WzIxJgt5AP3UNbhLg7Xva2b63g67eECWFuVx23krOOW7ehGenMImbX11CRWk+G2tbEgpmXb0h9jR2cfGZ4x8BadKLBTNjJigSifLg8zt5/vUD7GnqInbv8NyqYtaumMWy+eWcKLMnPWrQJM7n87F6SSWvbmsiEomO2Se5dXcbUUCm0UjGbGXBzJgJaO0M8NN7N6H1baxcOIOLTlvC8vluFvuSKRgtaBK3amklT2/cx879nWPevL2lvo3cHB/L5h2+m7zN1LBgZgyuj6uxrZfK8sIx+042bG/i5/e9QbA/zCfeeRSnHzP3MOXSJOJor19y447mMYOZ7mpj2dzyQ2ZJMZnHgpmZtvrDEbbUt/HKliZe2dZIS0eA8uI8Tj56DqevnsuiOaUH3QPWH45w9xPbefiFehZUl/KZS1Yxt8ruTUo35cX5LJ5TxqbaFi46feS+sN5APzv3d/LOKV6mxhweFszMtBIIhnltRzOvbG1k/bZmegL95Of6WbW0kredvIgt9W08/soeHntpN/NmlXDa6hpOPXoO/ZEoN/5xI7UNnZx7/Hw++OYVdjWfxlYtreThF3bRG+gf8f66bXvaiUZBFll/WTawYGamjfXbmvjlg5vp6A5SWpTHcStncfwR1Ry9tHJgkcLzTlxId1+IF984wDMb93HX49u5+/Ht5OX6yc3x89l3rx5YvNKkr9VLK3nguZ1s3tnKcSurh91mS30bOX4fK+ZVHObcmalgwcxkvb5gP3f+ZRuPv7qXBdUlfOqio5FFM0YcKl9SmMc5x83nnOPms7+1h2c37qO5vY+Lz1jKrBlFhzn3ZiJWLKigIC+HjXUtIwYz3dXGkpoyCvKthp0NLJiZrLZ9Tzs/u+91Glt7ueCURbz7zGUJLXcSM2dmMZecuWwKc2imQm6OnyMXzWDTjuEX7AyEwtQ2dKR8PkmTPBbMTFbqD0e49+k67n+2jsqyAr744eNs7r1pZtXSStZvb+ZAaw+zZx48fdiOPe2EI1HrL8siFsxMVgmEwmze2co962rZua+T01fX8KG3rqS40A716SY2ddimutZDgpnWt+HzwYr5FsyyhX3DTUaLRqPsbermtR0tbKxtZkt9O/3hCKVFeTZYY5qrqSymqryQjTuaOfe4+QelbalvY9HsMrvIySL2nzRTprMnyO7GbnY3drGnsYt9Lb0EQ2FC4Qih/gj93u9Qf4TC/FxqKouYX13K/FklzK8uYf6skoG1t0L9EVq7ArR29NHc0UdLR4D9rT28XtdKa2cAgHmzSnjz8fM5ZlkVKxdW2ND5ac7n87FqaSUvbt5PfzgycDN8qD/C9r0dnLN2/hh7MJnEgpkZUag/QnNHH01tvTS29dLYHnvcR18oTEGen4K8nIGf/Lwc8vP8NLX3sbuxi/au4MC+SovyqKkqpqw4n7xcvzfU3Udebg55OX7w+9i+u411rzUQCA4u5z6jNJ9I1C2gOFRZcR4rF87gmGVVrF5aSWV54WEpF5M5Vi+t5Mn1e6lt6OCIBa5Jsbahg1B/xPrLsowFM0N/OML+1l72NHaxu7GbPY1d7GnqprG1l2jcdrk5PqoqiqieUcjs/CKCoTCBUJjuvn5aOwMEQmGCoTAzygpYtaTSraU1u4QF1aVUlOSPuqJydXUZjY2dRKJRWjr62NPYzd6mbvY0dZPj91FVXsjM8gKqygupLC9kZlnBwL1hxozkqCUz8flg446WgWAWW4xzpU0unFUsmE0jvYF+9rX0sK+5h4aWbu+3+zsccWHL53N9DYtml3Lq0XOonlE08FNRmo9/lICUDH6fj1kVRcyqKGLNisRXCzZmOCWFeSybW86muhbefZa7xULr25hfXWKrGWQZC2ZZIBgK09IZoLUzQGdPkI7uIB09oYHHnT0hGtt7D2r28/t8VM8opKaymGOXV7FgVinzq0uYW1VsfU0mq6xaWsmfnqmjqzdEUUEO23a3c/oxNanOlkkyC2aeiDdr+v6WXkL9EcKRCOFwlP7Y73CESCRKJApRokSjbj2raNQ9LivJp3pGIdUVRVRVDD/zeldviP0tPa521NJDKAKhYD85OT5yc/zk+Ad/j7QOUyQSpb0r6AZBdLqBEF29oUO28/mgrDifsuI8yovzWb2kkpqqYuZWlVBTWczsmUW2sq6ZFlYvreLep+t4Y2crVeWFBEJha2LMQtM6mD2zcR9bdrVSf8D1FQVC4bFflACfDyrLCphV4Zrmmjv62N/Se1DQyfH7KC/J9wJnlHA4Qn84SiQaHWXPTnFBLpXlBVSWF7JsXgWVZQVUlhcws6yQ8pJ8yovzKCnMG3NhQmOmg6XzyigqyGVTbTM1lW6VA1uMM/tM62B2z1M76O4NsXB2KWceO5eFs0uZW1VCfp6fnBw32m5obcnvcz8+nxv6G+tC6ugOuhF/bX00tfcOPK5t6KCqvJATpJqaymLmVBZTU1nMrIpC5tZU0NjYeVCeItEo4bCr8Q3H58OaAY0Zhxy/n6MXz2RjbQvtXUHmVBZTUVqQ6myZJMvoYCYiK4GbgSqgGbhSVbcm+vovX3ECZUV5o46yS1SlN8pOFk1uP36fD3+u1aiMSaZVSyt5eUsj7V1BW0w1S2V6p8kNwPWquhK4HrhxPC+eUVqQlEBmjElvsamtwpGoNTFmqYytmYnIbOB44DzvqduB60SkWlUbx3h5DpAWfUrpkId0YWUxyMpiUDLKYk5lMUcvmUlTex+rllVmbPmmOt9x7592fR2+kfpm0p2InAD8WlVXxT33OnC5qv5tjJefATw1lfkzxpgsdiawLtWZiJexNbNJehH3z2gAkjOE0Rhjsl8OMBd3Dk0rmRzM6oH5IpKjqmERyQHmec+PJUCaXVUYY0yG2J7qDAwnYweAqOoB4FXgQ95THwJeSaC/zBhjTJbJ2D4zABE5Ejc0fybQihuar6nNlTHGmMMto4OZMcYYAxnczGiMMcbEWDAzxhiT8SyYGWOMyXgWzIwxxmS8TL7PLK2IyPeB9wJLgGNUdaP3/DuBbwF5QAvwUVWt9dIKgR8BbwX6gGdV9VNe2qQmUU6l8ZaFiCwB7onbxQygXFUrvddNm7Lw0i700ny4C85vqOrvvbTpVhajpWVyWVQBvwGW4+573QZ8WlUbReRU3DyzRUAdblajA97rJpQ2HVjNLHnuAc4CdsaeEJGZuC/bB1X1GOBnwE/iXvM9XBBb6aV/NS5tUpMop9i4ykJV61R1bezHe/1tcfubNmUhIj7cSe4KrywuB24Wkdh3dTqVxVjfn0wuiyjwPVUVVT0WdyPyd73//y3AZ73P9STwXRg4NsadNl1YMEsSVV2nqkNnH1kB7FfVLd7fDwBvE5FZQ579KQAAAppJREFUIlIKXAl8VVWj3j72w0GTKN/uve524HgRqZ7qz5EM4y2L+I1EJB+4DPiF9/d0LIsIUOE9ngE0qGpkGpbFaN+fTC+LFlV9PO6p54DFwIlAn6rGZii6AfiA93iiadOCBbOptQWoEZGTvL8v834vwjUvNANfF5GXRORxETnDS18I7FHVMID3e6/3fKYarSzivQv32WOTRU+rsvAubD4A/FFEduJqMx/x0qdVWYyRljVl4dW6PwPci/tsAzVXVW0C/CJSOYm0acGC2RRS1XbgUuBHIvISMBtoA0K4/spluCm4TgT+Ffi9iJSnKr9TaYyyiPdxvFpZthqtLEQkF/g34GJVXQxcBNzh1eSzzmhlMY5jJtNdC3QB16U6I5nMgtkUU9XHVPUML2Bdh+uc3YG7iurHayZR1eeBJmAlcZMoA4xzEuW0NUpZACAi84CzgVvjXjbdymItME9Vn/a2exroBo5i+pXFaGlZURbeoJgjgEtVNQLswjU3xtJnAVFVbZlE2rRgwWyKiUiN99sPfAe4QVW7vWaAv+ItLuqNzJoNbMvWSZRHKou4TT4K3K+qzbEnpmFZ7AYWiIh46UcBNcD2aVgWo31/Mr4sROTbwAnAJaoa8J5+GSiK63K4GrhzkmnTgs3NmCQi8mPgPbgTTxPQrKqrROTnwOlAPvAI8I+q2ue9ZhmuSa0K13Ty76r6oJeWsZMoT6QsvNdtAa5R1YeG7G9alYWIXAZ8CTcQBODrqnqPlzbdymK0tEwui1XARly/YK/3dK2qvltETsONzCxkcIh9bHDYhNKmAwtmxhhjMp41MxpjjMl4FsyMMcZkPAtmxhhjMp4FM2OMMRnPgpkxxpiMZ8HMGGNMxrNgZowxJuNZMDPGGJPx/j/mwlW6PGp/4gAAAABJRU5ErkJggg==\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "fig, ax = plt.subplots()\n",
    "plot(x, y1, ax, 'Increase in mean Fortune 500 company profits from 1955 to 2005', 'Profit (millions)')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "y2 = avgs.revenue\n",
    "fig, ax = plt.subplots()\n",
    "plot(x, y2, ax, 'Increase in mean Fortune 500 company revenues from 1955 to 2005', 'Revenue (millions)')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 1008x288 with 2 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "def plot_with_std(x, y, stds, ax, title, y_label):\n",
    "    ax.fill_between(x, y - stds, y + stds, alpha=0.2)\n",
    "    plot(x, y, ax, title, y_label)\n",
    "fig, (ax1, ax2) = plt.subplots(ncols=2)\n",
    "title = 'Increase in mean and std Fortune 500 company %s from 1955 to 2005'\n",
    "stds1 = group_by_year.std().profit.values\n",
    "stds2 = group_by_year.std().revenue.values\n",
    "plot_with_std(x, y1.values, stds1, ax1, title % 'profits', 'Profit (millions)')\n",
    "plot_with_std(x, y2.values, stds2, ax2, title % 'revenues', 'Revenue (millions)')\n",
    "fig.set_size_inches(14, 4)\n",
    "fig.tight_layout()"
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
   "version": "3.7.4"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
