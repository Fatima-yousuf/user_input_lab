{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyOu+PDIfHoRvgTinBuF0gVy",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/Fatima-yousuf/user_input_lab/blob/main/tuples_practice_lab.md\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Tuples in Python – Practice Lab**\n",
        "1. Exercising Tuples\n",
        "\n",
        "      1a. Take five inputs from the user and save in a tuple\n",
        "      \n",
        "      Example input/output:"
      ],
      "metadata": {
        "id": "G4l5i4Uh3XCT"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# 1a. Take five inputs from the user and save in a tuple\n",
        "my_tuple = tuple(input(f\"Enter element {i+1}: \") for i in range(5))\n",
        "print(\"Your tuple:\", my_tuple)\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "DwB6adCp4DSs",
        "outputId": "2646d1c3-2128-40c1-dbf3-41922ac54e6c"
      },
      "execution_count": 2,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Enter element 1: apple\n",
            "Enter element 2: banana\n",
            "Enter element 3: cherry\n",
            "Enter element 4: mango\n",
            "Enter element 5: blueberry\n",
            "Your tuple: ('apple', 'banana', 'cherry', 'mango', 'blueberry')\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 1b. Single element tuple\n",
        "single_element_tuple = (5,)\n",
        "print(single_element_tuple, type(single_element_tuple))\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "0NlKAZ2L4U6R",
        "outputId": "204a7137-c457-40ef-818d-60d9f830578a"
      },
      "execution_count": 3,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "(5,) <class 'tuple'>\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 1c. Count repeated integers\n",
        "my_tuple = (1,2,3,4,3,2,1,2,3,5,4,3,2,1)\n",
        "counts = {x: my_tuple.count(x) for x in set(my_tuple)}\n",
        "print(\"Count of each integer:\", counts)\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "_8cgem0N4bN4",
        "outputId": "923d07c4-20fc-4f7f-dc0d-c347fe6d5a42"
      },
      "execution_count": 4,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Count of each integer: {1: 3, 2: 4, 3: 4, 4: 2, 5: 1}\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 1d. Concatenate tuple with itself\n",
        "my_tuple_d = my_tuple + my_tuple\n",
        "print(\"Original tuple:\", my_tuple)\n",
        "print(\"Concatenated tuple:\", my_tuple_d)\n",
        "print(\"Are the objects the same?\", my_tuple is my_tuple_d)\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "g1MLazuV4hXK",
        "outputId": "2acef1f2-15ad-4580-f9cc-aacd1ed7384f"
      },
      "execution_count": 5,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Original tuple: (1, 2, 3, 4, 3, 2, 1, 2, 3, 5, 4, 3, 2, 1)\n",
            "Concatenated tuple: (1, 2, 3, 4, 3, 2, 1, 2, 3, 5, 4, 3, 2, 1, 1, 2, 3, 4, 3, 2, 1, 2, 3, 5, 4, 3, 2, 1)\n",
            "Are the objects the same? False\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "### 1e. Why these operations aren’t legal\n",
        "\n",
        "x = (1,2,3,4)\n",
        "\n",
        "x.append(1)      # ❌ Not allowed: tuples are immutable\n",
        "\n",
        "x[1] = \"hello\"   # ❌ Not allowed: cannot change elements\n",
        "\n",
        "del x[2]         # ❌ Not allowed: cannot delete elements\n",
        "\n",
        "**Explanation:**  \n",
        "Tuples are **immutable**, which means you cannot add, modify, or delete elements.  \n",
        "Trying to run any of these operations in code will cause an error.\n"
      ],
      "metadata": {
        "id": "o6Ku39Dt4qq1"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "### 2a. Simple tuple unpacking\n"
      ],
      "metadata": {
        "id": "k1PTe3JY5XNi"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# 2a. Simple tuple unpacking\n",
        "(one, two, three, four) = (1, 2, 3, 4)\n",
        "print(\"one:\", one, type(one))\n",
        "print(\"two:\", two, type(two))\n",
        "print(\"three:\", three, type(three))\n",
        "print(\"four:\", four, type(four))\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "ol0CffAR5ZBh",
        "outputId": "c9ad25ae-380d-47e0-f697-5857e44629a8"
      },
      "execution_count": 6,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "one: 1 <class 'int'>\n",
            "two: 2 <class 'int'>\n",
            "three: 3 <class 'int'>\n",
            "four: 4 <class 'int'>\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "### 2b. Extended unpacking with\n"
      ],
      "metadata": {
        "id": "_Bse4OUR5diD"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "x = (1, 2, 3, 4)\n",
        "a, b, *c = x\n",
        "print(\"a:\", a)\n",
        "print(\"b:\", b)\n",
        "print(\"c:\", c)\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "qzKbrmft5u-u",
        "outputId": "c35f07b1-7bdd-49fd-cb03-3970f24afad7"
      },
      "execution_count": 7,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "a: 1\n",
            "b: 2\n",
            "c: [3, 4]\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "### 2c. Extended unpacking with\n"
      ],
      "metadata": {
        "id": "3GK5P36K6YdY"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "a, *b, c = x\n",
        "print(\"a:\", a)\n",
        "print(\"b:\", b)\n",
        "print(\"c:\", c)\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "WIstsmdE6bqw",
        "outputId": "46f7073e-e855-436f-bd1c-4d1a5e3dea9d"
      },
      "execution_count": 8,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "a: 1\n",
            "b: [2, 3]\n",
            "c: 4\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "## 3. Memory Management\n"
      ],
      "metadata": {
        "id": "WOfmD1P66f-6"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# 3. Memory Management\n",
        "my_x = [100, 200, 300, 400]\n",
        "my_y = (200, 300, 400, 500)\n",
        "\n",
        "print(\"Memory addresses of my_x elements (list):\")\n",
        "for i in range(len(my_x)):\n",
        "    print(f\"Index {i}: {id(my_x[i])}\")\n",
        "\n",
        "print(\"\\nMemory addresses of my_y elements (tuple):\")\n",
        "for i in range(len(my_y)):\n",
        "    print(f\"Index {i}: {id(my_y[i])}\")\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "fUidAF0b6hJX",
        "outputId": "4bdb9847-6bc7-4fe2-8cb4-b4ce7b46b425"
      },
      "execution_count": 9,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Memory addresses of my_x elements (list):\n",
            "Index 0: 11645256\n",
            "Index 1: 11648456\n",
            "Index 2: 133791938027536\n",
            "Index 3: 133791938028944\n",
            "\n",
            "Memory addresses of my_y elements (tuple):\n",
            "Index 0: 11648456\n",
            "Index 1: 133791938020464\n",
            "Index 2: 133791938027280\n",
            "Index 3: 133791938019408\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "###Challenges:\n",
        "- A challenge I faced was understanding how the fractional part of a number works.  \n",
        "- I also learned the importance of separating headings from code sections to keep the assignment organized and readable.  \n",
        "- Generally speaking, practicing using tuples helped me understand when it is best to use immutable data versus mutable data."
      ],
      "metadata": {
        "id": "Gn3D9gIt8tKC"
      }
    }
  ]
}