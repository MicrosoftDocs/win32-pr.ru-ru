---
title: Ресурс RCDATA
description: Определяет ресурс необработанных данных для приложения. Ресурсы необработанных данных допускают включение двоичных данных непосредственно в исполняемый файл.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Меню ресурсов RCDATA и другие ресурсы
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103987010"
---
# <a name="rcdata-resource"></a><span data-ttu-id="72e30-105">Ресурс RCDATA</span><span class="sxs-lookup"><span data-stu-id="72e30-105">RCDATA resource</span></span>

<span data-ttu-id="72e30-106">Определяет ресурс необработанных данных для приложения.</span><span class="sxs-lookup"><span data-stu-id="72e30-106">Defines a raw data resource for an application.</span></span> <span data-ttu-id="72e30-107">Ресурсы необработанных данных допускают включение двоичных данных непосредственно в исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="72e30-107">Raw data resources permit the inclusion of binary data directly in the executable file.</span></span>

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a><span data-ttu-id="72e30-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="72e30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72e30-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="72e30-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="72e30-110">Уникальное имя или 16-битовое целочисленное значение без знака, идентифицирующее ресурс.</span><span class="sxs-lookup"><span data-stu-id="72e30-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="72e30-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*Необязательные операторы*</span><span class="sxs-lookup"><span data-stu-id="72e30-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="72e30-112">Этот параметр может быть равен нулю или нескольким следующим операторам.</span><span class="sxs-lookup"><span data-stu-id="72e30-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="72e30-113">Инструкция</span><span class="sxs-lookup"><span data-stu-id="72e30-113">Statement</span></span>                                                        | <span data-ttu-id="72e30-114">Описание</span><span class="sxs-lookup"><span data-stu-id="72e30-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72e30-115">[**Параметры**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="72e30-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="72e30-116">Определяемая пользователем информация о ресурсе, который может использоваться средствами чтения и записи файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72e30-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="72e30-117">Дополнительные сведения см. в разделе [**характеристики**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="72e30-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="72e30-118">[](language-statement.md) *Язык* языка, *подязык*</span><span class="sxs-lookup"><span data-stu-id="72e30-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="72e30-119">Язык для ресурса.</span><span class="sxs-lookup"><span data-stu-id="72e30-119">Language for the resource.</span></span> <span data-ttu-id="72e30-120">Дополнительные сведения см. в разделе [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="72e30-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="72e30-121">[**Версия**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="72e30-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="72e30-122">Определяемый пользователем номер версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72e30-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="72e30-123">Дополнительные сведения см. в разделе [**версия**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="72e30-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="72e30-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*необработанные данные*</span><span class="sxs-lookup"><span data-stu-id="72e30-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="72e30-125">Необработанные данные, состоящие из одного или нескольких целых чисел или строк символов.</span><span class="sxs-lookup"><span data-stu-id="72e30-125">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="72e30-126">Целые числа могут быть заданы в десятичном, восьмеричном или шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="72e30-126">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="72e30-127">Чтобы обеспечить совместимость с 16-разрядными Windows, целые числа хранятся в виде значений **Word** .</span><span class="sxs-lookup"><span data-stu-id="72e30-127">To be compatible with 16-bit Windows, integers are stored as **WORD** values.</span></span> <span data-ttu-id="72e30-128">Целое число можно сохранить как значение **типа DWORD** , указав для целого числа суффикс "L".</span><span class="sxs-lookup"><span data-stu-id="72e30-128">You can store an integer as a **DWORD** value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="72e30-129">Строки заключаются в кавычки.</span><span class="sxs-lookup"><span data-stu-id="72e30-129">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="72e30-130">RC не добавляет автоматически завершающий нуль-символ к строке.</span><span class="sxs-lookup"><span data-stu-id="72e30-130">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="72e30-131">Каждая строка является последовательностью указанных символов ANSI, если она не определена как строка расширенных символов с префиксом L.</span><span class="sxs-lookup"><span data-stu-id="72e30-131">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the L prefix.</span></span>

<span data-ttu-id="72e30-132">Блок данных начинается с границы **DWORD** , а RC не выполняет заполнение или выравнивание данных в блоке *необработанных данных* .</span><span class="sxs-lookup"><span data-stu-id="72e30-132">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="72e30-133">Необходимо обеспечить правильное выравнивание данных в блоке.</span><span class="sxs-lookup"><span data-stu-id="72e30-133">It is your responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

<span data-ttu-id="72e30-134">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="72e30-134">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="72e30-135">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="72e30-135">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="72e30-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="72e30-136">Examples</span></span>

<span data-ttu-id="72e30-137">В следующем примере демонстрируется использование инструкции **RCDATA** :</span><span class="sxs-lookup"><span data-stu-id="72e30-137">The following example demonstrates the use of the **RCDATA** statement:</span></span>

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a><span data-ttu-id="72e30-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72e30-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e30-139">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="72e30-139">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="72e30-140">**ПОКАЗАТЕЛИ**</span><span class="sxs-lookup"><span data-stu-id="72e30-140">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="72e30-141">**ЯЗЫКЕ**</span><span class="sxs-lookup"><span data-stu-id="72e30-141">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="72e30-142">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="72e30-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="72e30-143">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="72e30-143">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="72e30-144">**Версия**</span><span class="sxs-lookup"><span data-stu-id="72e30-144">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 




