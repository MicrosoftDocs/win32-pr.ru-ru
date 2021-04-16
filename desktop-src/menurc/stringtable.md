---
title: Структура StringTable
description: Представляет организацию данных в ресурсе версии файла. Он содержит сведения о языке и форматировании кодовой страницы для строк, указанных дочерним элементом. Кодовая страница — это упорядоченная кодировка.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Меню структуры StringTable и другие ресурсы
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415016"
---
# <a name="stringtable-structure"></a><span data-ttu-id="29bcb-106">Структура StringTable</span><span class="sxs-lookup"><span data-stu-id="29bcb-106">StringTable structure</span></span>

<span data-ttu-id="29bcb-107">Представляет организацию данных в ресурсе версии файла.</span><span class="sxs-lookup"><span data-stu-id="29bcb-107">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="29bcb-108">Он содержит сведения о языке и форматировании кодовой страницы для строк, указанных **дочерним** элементом.</span><span class="sxs-lookup"><span data-stu-id="29bcb-108">It contains language and code page formatting information for the strings specified by the **Children** member.</span></span> <span data-ttu-id="29bcb-109">Кодовая страница — это упорядоченная кодировка.</span><span class="sxs-lookup"><span data-stu-id="29bcb-109">A code page is an ordered character set.</span></span>

## <a name="syntax"></a><span data-ttu-id="29bcb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29bcb-110">Syntax</span></span>


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a><span data-ttu-id="29bcb-111">Члены</span><span class="sxs-lookup"><span data-stu-id="29bcb-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="29bcb-112">**вленгс**</span><span class="sxs-lookup"><span data-stu-id="29bcb-112">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="29bcb-113">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="29bcb-113">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="29bcb-114">Длина в байтах данной структуры **STRINGTABLE** , включая все структуры, указанные **дочерним** элементом.</span><span class="sxs-lookup"><span data-stu-id="29bcb-114">The length, in bytes, of this **StringTable** structure, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="29bcb-115">**ввалуеленгс**</span><span class="sxs-lookup"><span data-stu-id="29bcb-115">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="29bcb-116">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="29bcb-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="29bcb-117">Этот элемент всегда равен нулю.</span><span class="sxs-lookup"><span data-stu-id="29bcb-117">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="29bcb-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="29bcb-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="29bcb-119">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="29bcb-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="29bcb-120">Тип данных в ресурсе версии.</span><span class="sxs-lookup"><span data-stu-id="29bcb-120">The type of data in the version resource.</span></span> <span data-ttu-id="29bcb-121">Этот элемент равен 1, если ресурс версии содержит текстовые данные, и 0, если ресурс версии содержит двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="29bcb-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="29bcb-122">**сзкэй**</span><span class="sxs-lookup"><span data-stu-id="29bcb-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="29bcb-123">Тип: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="29bcb-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="29bcb-124">8-разрядное шестнадцатеричное число, хранящееся в виде строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="29bcb-124">An 8-digit hexadecimal number stored as a Unicode string.</span></span> <span data-ttu-id="29bcb-125">Четыре наиболее значимых цифры представляют идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="29bcb-125">The four most significant digits represent the language identifier.</span></span> <span data-ttu-id="29bcb-126">Четыре наиболее значимых цифры представляют кодовую страницу, для которой отформатированы данные.</span><span class="sxs-lookup"><span data-stu-id="29bcb-126">The four least significant digits represent the code page for which the data is formatted.</span></span> <span data-ttu-id="29bcb-127">Каждый идентификатор языка Microsoft Standard содержит две части: младшие 10 битов указывают основной язык, а старшие биты с высоким порядковым номером содержат сведения о подязыке.</span><span class="sxs-lookup"><span data-stu-id="29bcb-127">Each Microsoft Standard Language identifier contains two parts: the low-order 10 bits specify the major language, and the high-order 6 bits specify the sublanguage.</span></span> <span data-ttu-id="29bcb-128">Таблицу допустимых идентификаторов см. в разделе.</span><span class="sxs-lookup"><span data-stu-id="29bcb-128">For a table of valid identifiers see .</span></span>

</dd> <dt>

<span data-ttu-id="29bcb-129">**Заполнение**</span><span class="sxs-lookup"><span data-stu-id="29bcb-129">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="29bcb-130">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="29bcb-130">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="29bcb-131">Столько нуля слов, сколько необходимо для выровняйте **дочернего** элемента на 32-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="29bcb-131">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="29bcb-132">**Children**</span><span class="sxs-lookup"><span data-stu-id="29bcb-132">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="29bcb-133">Тип: **[ **строка**](string-str.md)**</span><span class="sxs-lookup"><span data-stu-id="29bcb-133">Type: **[**String**](string-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="29bcb-134">Массив из одной или нескольких [**строковых**](string-str.md) структур.</span><span class="sxs-lookup"><span data-stu-id="29bcb-134">An array of one or more [**String**](string-str.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29bcb-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29bcb-135">Remarks</span></span>

<span data-ttu-id="29bcb-136">Эта структура не является истинной структурой языка C, так как она содержит члены переменной длины.</span><span class="sxs-lookup"><span data-stu-id="29bcb-136">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="29bcb-137">Эта структура была создана только для описания организации данных в ресурсе версии и не отображается ни в одном из файлов заголовков, поставляемых вместе с пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="29bcb-137">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="29bcb-138">**Дочерний** элемент структуры [**стрингфилеинфо**](stringfileinfo.md) содержит по крайней мере одну структуру **STRINGTABLE** .</span><span class="sxs-lookup"><span data-stu-id="29bcb-138">The **Children** member of the [**StringFileInfo**](stringfileinfo.md) structure contains at least one **StringTable** structure.</span></span>

<span data-ttu-id="29bcb-139">Задайте в качестве части кодовой страницы элемента **сзкэй** шестнадцатеричное значение 0x04b0, чтобы указать кодовую страницу Юникода, или шестнадцатеричное значение кодовой страницы, подходящую для компонента языка.</span><span class="sxs-lookup"><span data-stu-id="29bcb-139">Set the code page portion of the **szKey** member to the hexadecimal value 0x04b0 to indicate the Unicode code page, or to the hexadecimal value of the code page that is appropriate for the language component.</span></span> <span data-ttu-id="29bcb-140">После выбора значения для кодовой страницы следует продолжать использовать то же значение в последующих редакциях файла.</span><span class="sxs-lookup"><span data-stu-id="29bcb-140">After you choose the value for the code page you should continue to use the same value in later revisions to the file.</span></span>

<span data-ttu-id="29bcb-141">Исполняемый файл или библиотека DLL, поддерживающие несколько языков, должны иметь ресурс версии для каждого языка, а не единственный ресурс версии, содержащий строки на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="29bcb-141">An executable file or DLL that supports multiple languages should have a version resource for each language, rather than a single version resource that contains strings in several languages.</span></span> <span data-ttu-id="29bcb-142">Однако при использовании структуры [**var**](var-str.md) для перечисления языков, поддерживаемых приложением, число структур **STRINGTABLE** в ресурсе версии напрямую связано с числом пар идентификаторов кодовых страниц в элементе **value** структуры **var** .</span><span class="sxs-lookup"><span data-stu-id="29bcb-142">However, if you use the [**Var**](var-str.md) structure to list the languages that your application supports, the number of **StringTable** structures in the version resource is directly related to the number of language/code page identifier pairs in the **Value** member of the **Var** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="29bcb-143">Требования</span><span class="sxs-lookup"><span data-stu-id="29bcb-143">Requirements</span></span>



| <span data-ttu-id="29bcb-144">Требование</span><span class="sxs-lookup"><span data-stu-id="29bcb-144">Requirement</span></span> | <span data-ttu-id="29bcb-145">Значение</span><span class="sxs-lookup"><span data-stu-id="29bcb-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="29bcb-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29bcb-146">Minimum supported client</span></span><br/> | <span data-ttu-id="29bcb-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29bcb-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="29bcb-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29bcb-148">Minimum supported server</span></span><br/> | <span data-ttu-id="29bcb-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29bcb-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="29bcb-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29bcb-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="29bcb-151">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="29bcb-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29bcb-152">**Строка**</span><span class="sxs-lookup"><span data-stu-id="29bcb-152">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="29bcb-153">**стрингфилеинфо**</span><span class="sxs-lookup"><span data-stu-id="29bcb-153">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="29bcb-154">**Var**</span><span class="sxs-lookup"><span data-stu-id="29bcb-154">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="29bcb-155">**варфилеинфо**</span><span class="sxs-lookup"><span data-stu-id="29bcb-155">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="29bcb-156">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="29bcb-156">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="29bcb-157">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="29bcb-157">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29bcb-158">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="29bcb-158">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





