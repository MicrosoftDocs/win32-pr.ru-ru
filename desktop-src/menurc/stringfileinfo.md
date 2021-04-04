---
title: Структура Стрингфилеинфо
description: Представляет организацию данных в ресурсе версии файла. Он содержит сведения о версии, которые могут отображаться для определенного языка и кодовой страницы.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Меню структуры Стрингфилеинфо и другие ресурсы
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988328"
---
# <a name="stringfileinfo-structure"></a><span data-ttu-id="bfd7b-105">Структура Стрингфилеинфо</span><span class="sxs-lookup"><span data-stu-id="bfd7b-105">StringFileInfo structure</span></span>

<span data-ttu-id="bfd7b-106">Представляет организацию данных в ресурсе версии файла.</span><span class="sxs-lookup"><span data-stu-id="bfd7b-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="bfd7b-107">Он содержит сведения о версии, которые могут отображаться для определенного языка и кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="bfd7b-107">It contains version information that can be displayed for a particular language and code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd7b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfd7b-108">Syntax</span></span>


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a><span data-ttu-id="bfd7b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="bfd7b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="bfd7b-110">**вленгс**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="bfd7b-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bfd7b-112">Длина всего блока **стрингфилеинфо** в байтах, включая все структуры, указанные **дочерним** элементом.</span><span class="sxs-lookup"><span data-stu-id="bfd7b-112">The length, in bytes, of the entire **StringFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="bfd7b-113">**ввалуеленгс**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="bfd7b-114">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bfd7b-115">Этот элемент всегда равен нулю.</span><span class="sxs-lookup"><span data-stu-id="bfd7b-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="bfd7b-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="bfd7b-117">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bfd7b-118">Тип данных в ресурсе версии.</span><span class="sxs-lookup"><span data-stu-id="bfd7b-118">The type of data in the version resource.</span></span> <span data-ttu-id="bfd7b-119">Этот элемент равен 1, если ресурс версии содержит текстовые данные, и 0, если ресурс версии содержит двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="bfd7b-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="bfd7b-120">**сзкэй**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="bfd7b-121">Тип: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="bfd7b-122">Строка Юникода L "Стрингфилеинфо".</span><span class="sxs-lookup"><span data-stu-id="bfd7b-122">The Unicode string L"StringFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="bfd7b-123">**Заполнение**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="bfd7b-124">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bfd7b-125">Столько нуля слов, сколько необходимо для выровняйте **дочернего** элемента на 32-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="bfd7b-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="bfd7b-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="bfd7b-127">Тип: **[ **STRINGTABLE**](stringtable.md)**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-127">Type: **[**StringTable**](stringtable.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfd7b-128">Массив из одной или нескольких структур [**STRINGTABLE**](stringtable.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd7b-128">An array of one or more [**StringTable**](stringtable.md) structures.</span></span> <span data-ttu-id="bfd7b-129">Каждый элемент **сзкэй** структуры **STRINGTABLE** указывает соответствующий язык и кодовую страницу для отображения текста в этой структуре **STRINGTABLE** .</span><span class="sxs-lookup"><span data-stu-id="bfd7b-129">Each **StringTable** structure's **szKey** member indicates the appropriate language and code page for displaying the text in that **StringTable** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfd7b-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfd7b-130">Remarks</span></span>

<span data-ttu-id="bfd7b-131">Эта структура не является истинной структурой языка C, так как она содержит члены переменной длины.</span><span class="sxs-lookup"><span data-stu-id="bfd7b-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="bfd7b-132">Эта структура была создана только для описания организации данных в ресурсе версии и не отображается ни в одном из файлов заголовков, поставляемых вместе с пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="bfd7b-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="bfd7b-133">**Дочерние элементы** структуры [**VS \_ versionInfo**](vs-versioninfo.md) могут содержать ноль или более структур **стрингфилеинфо** .</span><span class="sxs-lookup"><span data-stu-id="bfd7b-133">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or more **StringFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfd7b-134">Требования</span><span class="sxs-lookup"><span data-stu-id="bfd7b-134">Requirements</span></span>



| <span data-ttu-id="bfd7b-135">Требование</span><span class="sxs-lookup"><span data-stu-id="bfd7b-135">Requirement</span></span> | <span data-ttu-id="bfd7b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="bfd7b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bfd7b-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfd7b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd7b-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bfd7b-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bfd7b-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfd7b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd7b-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bfd7b-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bfd7b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfd7b-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="bfd7b-142">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bfd7b-143">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-143">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="bfd7b-144">**Строка**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-144">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="bfd7b-145">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-145">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="bfd7b-146">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="bfd7b-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bfd7b-147">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="bfd7b-147">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





