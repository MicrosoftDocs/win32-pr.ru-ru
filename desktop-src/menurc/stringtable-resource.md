---
title: Ресурс STRINGTABLE
description: Определяет один или несколько строковых ресурсов для приложения. Строковые ресурсы — это просто заканчивающиеся нулем строки в Юникоде или ASCII, которые можно загрузить при необходимости из исполняемого файла с помощью функции Лоадстринг.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Меню ресурсов STRINGTABLE и другие ресурсы
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133862"
---
# <a name="stringtable-resource"></a><span data-ttu-id="90e4a-105">Ресурс STRINGTABLE</span><span class="sxs-lookup"><span data-stu-id="90e4a-105">STRINGTABLE resource</span></span>

<span data-ttu-id="90e4a-106">Определяет один или несколько строковых ресурсов для приложения.</span><span class="sxs-lookup"><span data-stu-id="90e4a-106">Defines one or more string resources for an application.</span></span> <span data-ttu-id="90e4a-107">Строковые ресурсы — это просто заканчивающиеся нулем строки в Юникоде или ASCII, которые можно загрузить при необходимости из исполняемого файла с помощью функции [**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa) .</span><span class="sxs-lookup"><span data-stu-id="90e4a-107">String resources are simply null-terminated Unicode or ASCII strings that can be loaded when needed from the executable file, using the [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) function.</span></span>

<span data-ttu-id="90e4a-108">Существует два способа форматирования оператора **STRINGTABLE** :</span><span class="sxs-lookup"><span data-stu-id="90e4a-108">There are two ways to format a **STRINGTABLE** statement:</span></span>

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

<span data-ttu-id="90e4a-109">\- или -</span><span class="sxs-lookup"><span data-stu-id="90e4a-109">\- or -</span></span>

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="90e4a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="90e4a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90e4a-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*Необязательные операторы*</span><span class="sxs-lookup"><span data-stu-id="90e4a-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="90e4a-112">Этот параметр может быть равен нулю или нескольким следующим операторам.</span><span class="sxs-lookup"><span data-stu-id="90e4a-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="90e4a-113">Инструкция</span><span class="sxs-lookup"><span data-stu-id="90e4a-113">Statement</span></span>                                                        | <span data-ttu-id="90e4a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="90e4a-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90e4a-115">[**Параметры**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="90e4a-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="90e4a-116">Определяемая пользователем информация о ресурсе, который может использоваться средствами чтения и записи файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90e4a-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="90e4a-117">Дополнительные сведения см. в разделе [**характеристики**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="90e4a-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="90e4a-118">[](language-statement.md) *Язык* языка, *подязык*</span><span class="sxs-lookup"><span data-stu-id="90e4a-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="90e4a-119">Указывает язык ресурса.</span><span class="sxs-lookup"><span data-stu-id="90e4a-119">Specifies the language for the resource.</span></span> <span data-ttu-id="90e4a-120">Дополнительные сведения см. в разделе [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="90e4a-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="90e4a-121">[**Версия**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="90e4a-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="90e4a-122">Определяемый пользователем номер версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90e4a-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="90e4a-123">Дополнительные сведения см. в разделе [**версия**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="90e4a-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="90e4a-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span><span class="sxs-lookup"><span data-stu-id="90e4a-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span></span>
</dt> <dd>

<span data-ttu-id="90e4a-125">16-разрядное целое число без знака, идентифицирующее ресурс.</span><span class="sxs-lookup"><span data-stu-id="90e4a-125">Unsigned 16-bit integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="90e4a-126"><span id="string"></span><span id="STRING"></span>*Строка*</span><span class="sxs-lookup"><span data-stu-id="90e4a-126"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="90e4a-127">Одна или несколько строк, заключенных в кавычки.</span><span class="sxs-lookup"><span data-stu-id="90e4a-127">One or more strings, enclosed in quotation marks.</span></span> <span data-ttu-id="90e4a-128">Длина строки не должна превышать 4097 символов и должна занимать одну строку в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="90e4a-128">The string must be no longer than 4097 characters and must occupy a single line in the source file.</span></span> <span data-ttu-id="90e4a-129">Чтобы добавить в строку символ возврата каретки, используйте следующую последовательность символов: \\ 012.</span><span class="sxs-lookup"><span data-stu-id="90e4a-129">To add a carriage return to the string, use this character sequence: \\012.</span></span> <span data-ttu-id="90e4a-130">Например, строка «одна \\ 012Line две» определяет строку, которая отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="90e4a-130">For example, "Line one\\012Line two" defines a string that is displayed as follows:</span></span>

``` syntax
Line one
Line two
```

<span data-ttu-id="90e4a-131">Чтобы внедрить кавычки в строку, используйте следующую последовательность: "".</span><span class="sxs-lookup"><span data-stu-id="90e4a-131">To embed quotes in the string, use the following sequence: "".</span></span> <span data-ttu-id="90e4a-132">Например, строка "" "третьего типа" "" определяет строку, которая отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="90e4a-132">For example, """Line three""" defines a string that is displayed as follows:</span></span>

``` syntax
"Line three"
```

<span data-ttu-id="90e4a-133">Для кодирования символов Юникода используется символ "L", за которым следуют символы Юникода, заключенные в кавычки.</span><span class="sxs-lookup"><span data-stu-id="90e4a-133">To encode Unicode characters, use an "L" followed by the Unicode characters enclosed by quotes.</span></span> <span data-ttu-id="90e4a-134">Пример см. в разделе "примеры".</span><span class="sxs-lookup"><span data-stu-id="90e4a-134">See the Examples section for an example.</span></span>

<span data-ttu-id="90e4a-135">Компилятор ресурсов также поддерживает продолжение строк в *строке*.</span><span class="sxs-lookup"><span data-stu-id="90e4a-135">The resource compiler also supports line continuations in *string*.</span></span> <span data-ttu-id="90e4a-136">Пример см. в разделе "примеры".</span><span class="sxs-lookup"><span data-stu-id="90e4a-136">See the Examples section for an example.</span></span>

</dd> </dl>

<span data-ttu-id="90e4a-137">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="90e4a-137">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="90e4a-138">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="90e4a-138">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="90e4a-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90e4a-139">Remarks</span></span>

<span data-ttu-id="90e4a-140">Версия-кандидат выделяет 16 строк на раздел и использует значение идентификатора, чтобы определить, какой раздел должен содержать строку.</span><span class="sxs-lookup"><span data-stu-id="90e4a-140">RC allocates 16 strings per section and uses the identifier value to determine which section is to contain the string.</span></span> <span data-ttu-id="90e4a-141">Строки, идентификаторы которых отличаются только нижними 4 битами, помещаются в один раздел.</span><span class="sxs-lookup"><span data-stu-id="90e4a-141">Strings whose identifiers differ only in the bottom 4 bits are placed in the same section.</span></span> <span data-ttu-id="90e4a-142">Дополнительные сведения см. в разделе [Q196774](https://support.microsoft.com/kb/196774).</span><span class="sxs-lookup"><span data-stu-id="90e4a-142">For more information, see [Q196774](https://support.microsoft.com/kb/196774).</span></span>

## <a name="examples"></a><span data-ttu-id="90e4a-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="90e4a-143">Examples</span></span>

<span data-ttu-id="90e4a-144">В следующем примере показано использование оператора **STRINGTABLE** для вывода строк ASCII:</span><span class="sxs-lookup"><span data-stu-id="90e4a-144">The following example demonstrates the use of the **STRINGTABLE** statement to display ASCII strings:</span></span>

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

<span data-ttu-id="90e4a-145">В следующем примере показано, как кодировать символы Юникода:</span><span class="sxs-lookup"><span data-stu-id="90e4a-145">The following example shows how to encode Unicode characters:</span></span>

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

<span data-ttu-id="90e4a-146">В следующем примере показаны строки с кодировкой ASCII и Юникод.</span><span class="sxs-lookup"><span data-stu-id="90e4a-146">The following example shows strings with both ASCII and Unicode.</span></span> <span data-ttu-id="90e4a-147">Обратите внимание, что строки без начального символа "L" используют формат escape-последовательности из двух цифр:</span><span class="sxs-lookup"><span data-stu-id="90e4a-147">Note that strings without the initial "L" use the 2-digit escape format:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

<span data-ttu-id="90e4a-148">В следующем примере показано, как можно использовать продолжения строки:</span><span class="sxs-lookup"><span data-stu-id="90e4a-148">The following example shows how line continuations can be used:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a><span data-ttu-id="90e4a-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90e4a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e4a-150">**лоадстринг**</span><span class="sxs-lookup"><span data-stu-id="90e4a-150">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[<span data-ttu-id="90e4a-151">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="90e4a-151">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="90e4a-152">**ПОКАЗАТЕЛИ**</span><span class="sxs-lookup"><span data-stu-id="90e4a-152">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="90e4a-153">**ЯЗЫКЕ**</span><span class="sxs-lookup"><span data-stu-id="90e4a-153">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="90e4a-154">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="90e4a-154">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="90e4a-155">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="90e4a-155">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="90e4a-156">**Версия**</span><span class="sxs-lookup"><span data-stu-id="90e4a-156">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 