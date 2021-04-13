---
title: Командные строки
description: Командные строки
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Строки команд MCI, сведения
- Строки команд MCI, синтаксис
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412797"
---
# <a name="command-strings"></a><span data-ttu-id="eccd3-105">Командные строки</span><span class="sxs-lookup"><span data-stu-id="eccd3-105">Command Strings</span></span>

<span data-ttu-id="eccd3-106">Чтобы отправить командную строку на устройство MCI, используйте функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , которая включает параметры для команды String и буфер для любых возвращаемых сведений.</span><span class="sxs-lookup"><span data-stu-id="eccd3-106">To send a string command to an MCI device, use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, which includes parameters for the string command and a buffer for any returned information.</span></span>

<span data-ttu-id="eccd3-107">Функция **mciSendString** возвращает нуль в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="eccd3-107">The **mciSendString** function returns zero if successful.</span></span> <span data-ttu-id="eccd3-108">Если функция завершается ошибкой, в слове с низким порядком возвращаемого значения содержится код ошибки.</span><span class="sxs-lookup"><span data-stu-id="eccd3-108">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="eccd3-109">Этот код ошибки можно передать функции [**мЦижетеррорстринг**](/previous-versions//dd757158(v=vs.85)) , чтобы получить текстовое описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="eccd3-109">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-strings"></a><span data-ttu-id="eccd3-110">Синтаксис командных строк</span><span class="sxs-lookup"><span data-stu-id="eccd3-110">Syntax of Command Strings</span></span>

<span data-ttu-id="eccd3-111">В строках команд MCI используется единообразный синтаксис модификатора глагола-Object.</span><span class="sxs-lookup"><span data-stu-id="eccd3-111">MCI command strings use a consistent verb-object-modifier syntax.</span></span> <span data-ttu-id="eccd3-112">Каждая Командная строка содержит команду, идентификатор устройства и аргументы команды.</span><span class="sxs-lookup"><span data-stu-id="eccd3-112">Each command string includes a command, a device identifier, and command arguments.</span></span> <span data-ttu-id="eccd3-113">Аргументы являются необязательными для некоторых команд и являются обязательными для других.</span><span class="sxs-lookup"><span data-stu-id="eccd3-113">Arguments are optional for some commands and required for others.</span></span>

<span data-ttu-id="eccd3-114">Командная строка имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="eccd3-114">A command string has the following form:</span></span>

<span data-ttu-id="eccd3-115">*аргументы идентификатора устройства командной строки \_*</span><span class="sxs-lookup"><span data-stu-id="eccd3-115">*command device\_id arguments*</span></span>

<span data-ttu-id="eccd3-116">Эти компоненты содержат следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="eccd3-116">These components contain the following information:</span></span>

-   <span data-ttu-id="eccd3-117">*Команда* ОТОБРАЖАЕТ команду MCI, например [**Open**](open.md), [**Close**](close.md)или [**Play**](play.md).</span><span class="sxs-lookup"><span data-stu-id="eccd3-117">The *command* specifies an MCI command, such as [**open**](open.md), [**close**](close.md), or [**play**](play.md).</span></span>
-   <span data-ttu-id="eccd3-118">*\_ Идентификатор устройства* определяет экземпляр драйвера MCI.</span><span class="sxs-lookup"><span data-stu-id="eccd3-118">The *device\_id* identifies an instance of an MCI driver.</span></span> <span data-ttu-id="eccd3-119">*\_ Идентификатор устройства* создается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="eccd3-119">The *device\_id* is created when the device is opened.</span></span>
-   <span data-ttu-id="eccd3-120">*Аргументы* задают флаги и переменные, используемые командой.</span><span class="sxs-lookup"><span data-stu-id="eccd3-120">The *arguments* specify the flags and variables used by the command.</span></span> <span data-ttu-id="eccd3-121">Флаги — это ключевые слова, распознаваемые командой MCI.</span><span class="sxs-lookup"><span data-stu-id="eccd3-121">Flags are keywords recognized with the MCI command.</span></span> <span data-ttu-id="eccd3-122">Переменные — это числа или строки, которые применяются к команде или флагу MCI.</span><span class="sxs-lookup"><span data-stu-id="eccd3-122">Variables are numbers or strings that apply to the MCI command or flag.</span></span>

    <span data-ttu-id="eccd3-123">Например, команда **Play** использует аргументы «от *позиции* » и «to *position* » для указания позиций, с которых начинается и заканчивается воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="eccd3-123">For example, the **play** command uses the arguments "from *position* " and "to *position* " to indicate the positions at which to start and end play.</span></span> <span data-ttu-id="eccd3-124">Вы можете перечислить флаги, используемые командой, в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="eccd3-124">You can list the flags used with a command in any order.</span></span> <span data-ttu-id="eccd3-125">При использовании флага, связанного с переменной, необходимо указать значение для переменной.</span><span class="sxs-lookup"><span data-stu-id="eccd3-125">When you use a flag that has a variable associated with it, you must supply a value for the variable.</span></span>

    <span data-ttu-id="eccd3-126">Неуказанные (и необязательные) аргументы команды предполагают значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eccd3-126">Unspecified (and optional) command arguments assume a default value.</span></span>

<span data-ttu-id="eccd3-127">Следующий пример функции отправляет команду [**Play**](play.md) с флагами "from" и "to".</span><span class="sxs-lookup"><span data-stu-id="eccd3-127">The following example function sends the [**play**](play.md) command with the "from" and "to" flags.</span></span>


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a><span data-ttu-id="eccd3-128">Типы данных для переменных команд</span><span class="sxs-lookup"><span data-stu-id="eccd3-128">Data Types for Command Variables</span></span>

<span data-ttu-id="eccd3-129">В командной строке можно использовать следующие типы данных для переменных.</span><span class="sxs-lookup"><span data-stu-id="eccd3-129">You can use the following data types for the variables in a command string.</span></span>



| <span data-ttu-id="eccd3-130">**Data type**</span><span class="sxs-lookup"><span data-stu-id="eccd3-130">**Data type**</span></span>        | <span data-ttu-id="eccd3-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eccd3-131">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eccd3-132">Строки</span><span class="sxs-lookup"><span data-stu-id="eccd3-132">Strings</span></span>              | <span data-ttu-id="eccd3-133">Типы строковых данных разделяются начальными и конечными пробелами и кавычками.</span><span class="sxs-lookup"><span data-stu-id="eccd3-133">String data types are delimited by leading and trailing white spaces and quotation marks.</span></span> <span data-ttu-id="eccd3-134">MCI удаляет одинарные кавычки из строки.</span><span class="sxs-lookup"><span data-stu-id="eccd3-134">MCI removes single quotation marks from a string.</span></span> <span data-ttu-id="eccd3-135">Чтобы вставить кавычки в строку, используйте набор из двух кавычек, где нужно внедрить кавычки.</span><span class="sxs-lookup"><span data-stu-id="eccd3-135">To put a quotation mark in a string, use a set of two quotation marks where you want to embed your quotation mark.</span></span> <span data-ttu-id="eccd3-136">Чтобы использовать пустую строку, используйте двойные кавычки, разделенные начальными и конечными пробелами.</span><span class="sxs-lookup"><span data-stu-id="eccd3-136">To use an empty string, use two quotation marks delimited by leading and trailing white spaces.</span></span> |
| <span data-ttu-id="eccd3-137">Длинные целые числа со знаком</span><span class="sxs-lookup"><span data-stu-id="eccd3-137">Signed long integers</span></span> | <span data-ttu-id="eccd3-138">Типы данных, подписанные длинными целыми числами, разделяются начальными и конечными пробелами.</span><span class="sxs-lookup"><span data-stu-id="eccd3-138">Signed long integer data types are delimited by leading and trailing white spaces.</span></span> <span data-ttu-id="eccd3-139">Если не указано иное, целые числа могут быть положительными или отрицательными.</span><span class="sxs-lookup"><span data-stu-id="eccd3-139">Unless otherwise specified, integers can be positive or negative.</span></span> <span data-ttu-id="eccd3-140">Если используются отрицательные целые числа, не следует разделять знак "минус" и первую цифру пробелом.</span><span class="sxs-lookup"><span data-stu-id="eccd3-140">If you use negative integers, you should not separate the minus sign and the first digit with a space.</span></span>                                                                                                    |
| <span data-ttu-id="eccd3-141">Прямоугольники</span><span class="sxs-lookup"><span data-stu-id="eccd3-141">Rectangles</span></span>           | <span data-ttu-id="eccd3-142">Типы данных Rectangle представляют собой упорядоченный список из четырех коротких значений со знаком.</span><span class="sxs-lookup"><span data-stu-id="eccd3-142">Rectangle data types are an ordered list of four signed short values.</span></span> <span data-ttu-id="eccd3-143">Пробел отделяет этот тип данных и разделяет каждое целое число в списке.</span><span class="sxs-lookup"><span data-stu-id="eccd3-143">White space delimits this data type and separates each integer in the list.</span></span>                                                                                                                                                                                                              |



 

 

 