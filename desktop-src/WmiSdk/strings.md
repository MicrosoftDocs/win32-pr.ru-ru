---
title: Строки MOF
description: Строка — это тип данных, который содержит строку символов, обычно предназначенную для читаемого текста.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898562"
---
# <a name="mof-strings"></a><span data-ttu-id="44360-103">Строки MOF</span><span class="sxs-lookup"><span data-stu-id="44360-103">MOF strings</span></span>

<span data-ttu-id="44360-104">Строка — это тип данных, который содержит строку символов, обычно предназначенную для читаемого текста.</span><span class="sxs-lookup"><span data-stu-id="44360-104">A string is a data type that contains a string of characters usually intended as human-readable text.</span></span> <span data-ttu-id="44360-105">MOF описывает два типа строк, которые используются для хранения одного или нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="44360-105">MOF describes two types of strings, which use to hold single or multiple characters.</span></span> <span data-ttu-id="44360-106">MOF также имеет ряд правил, описывающих использование кавычек в строке.</span><span class="sxs-lookup"><span data-stu-id="44360-106">MOF also has a series of rules describing the use of quotes within a string.</span></span>

<span data-ttu-id="44360-107">В следующей таблице перечислены типы строковых данных для MOF.</span><span class="sxs-lookup"><span data-stu-id="44360-107">The following table lists the string data types for MOF.</span></span>



| <span data-ttu-id="44360-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="44360-108">Data type</span></span>  | <span data-ttu-id="44360-109">Тип автоматизации</span><span class="sxs-lookup"><span data-stu-id="44360-109">Automation type</span></span> | <span data-ttu-id="44360-110">Описание</span><span class="sxs-lookup"><span data-stu-id="44360-110">Description</span></span>                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44360-111">**char16**</span><span class="sxs-lookup"><span data-stu-id="44360-111">**char16**</span></span> | <span data-ttu-id="44360-112">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="44360-112">**VT\_I2**</span></span>      | <span data-ttu-id="44360-113">Один 16-разрядный символ Юникода в формате универсального набора символов 2 (UCS-2)</span><span class="sxs-lookup"><span data-stu-id="44360-113">Single 16-bit Unicode character in Universal Character Set 2 (UCS-2) format</span></span><br/> |
| <span data-ttu-id="44360-114">**string**</span><span class="sxs-lookup"><span data-stu-id="44360-114">**string**</span></span> | <span data-ttu-id="44360-115">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="44360-115">**VT\_BSTR**</span></span>    | <span data-ttu-id="44360-116">Строка символов Юникод</span><span class="sxs-lookup"><span data-stu-id="44360-116">Unicode character string</span></span><br/>                                                    |



 

<span data-ttu-id="44360-117">При записи строк для MOF используйте следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="44360-117">Use the following guidelines when writing strings for MOF:</span></span>

-   <span data-ttu-id="44360-118">Заключите односимвольные константы в одинарные кавычки.</span><span class="sxs-lookup"><span data-stu-id="44360-118">Surround single-character constants with single quotes.</span></span>

    <span data-ttu-id="44360-119">Если вы не используете одинарные кавычки с одиночными символьными константами, необходимо использовать целочисленное представление значения символа Юникода.</span><span class="sxs-lookup"><span data-stu-id="44360-119">If you do not use single quotes with single character constants, you must use the integer representation of the Unicode character value.</span></span> <span data-ttu-id="44360-120">При необходимости можно указать символ буквально с \\ escape-последовательностью x из стандарта американский национальный институт стандартов (ANSI) (ANSI) C, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="44360-120">Optionally, you could specify the character literally with the \\x escape sequence from the American National Standards Institute (ANSI) C standard, as shown:</span></span>

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    <span data-ttu-id="44360-121">Так как MOF основана на Юникоде, можно также указать 16-разрядные значения.</span><span class="sxs-lookup"><span data-stu-id="44360-121">Because MOF is based on Unicode, you can also specify 16-bit values.</span></span>

    <span data-ttu-id="44360-122">Имейте в виду, что константы одного символа в формате ANSI C заключены в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="44360-122">Be aware that single-character constants in ANSI C format are surrounded by double quotes.</span></span>

-   <span data-ttu-id="44360-123">Заключите в строки символов двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="44360-123">Surround character strings with double quotes.</span></span>

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   <span data-ttu-id="44360-124">Объедините последующие строки кавычек с одним или несколькими пробелами.</span><span class="sxs-lookup"><span data-stu-id="44360-124">Concatenate successive quote strings with one or more white spaces.</span></span>

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   <span data-ttu-id="44360-125">Чтобы внедрить кавычки в строку, используйте escape-последовательность, начинающуюся с обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="44360-125">Use an escape sequence beginning with a backslash to embed quotes into a string.</span></span>

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

<span data-ttu-id="44360-126">В следующем примере описывается инициализация строковых свойств и строкового параметра.</span><span class="sxs-lookup"><span data-stu-id="44360-126">The following example describes how to initialize string properties and a string parameter:</span></span>

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




