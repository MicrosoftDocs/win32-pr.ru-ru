---
title: Var, структура
description: Представляет организацию данных в ресурсе версии файла. Обычно он содержит список пар языков и идентификаторов кодовых страниц, поддерживаемых версией приложения или библиотеки DLL.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Меню структуры var и другие ресурсы
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892650"
---
# <a name="var-structure"></a><span data-ttu-id="5a86c-105">Var, структура</span><span class="sxs-lookup"><span data-stu-id="5a86c-105">Var structure</span></span>

<span data-ttu-id="5a86c-106">Представляет организацию данных в ресурсе версии файла.</span><span class="sxs-lookup"><span data-stu-id="5a86c-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="5a86c-107">Обычно он содержит список пар языков и идентификаторов кодовых страниц, поддерживаемых версией приложения или библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="5a86c-107">It typically contains a list of language and code page identifier pairs that the version of the application or DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a86c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a86c-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a><span data-ttu-id="5a86c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="5a86c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a86c-110">**вленгс**</span><span class="sxs-lookup"><span data-stu-id="5a86c-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="5a86c-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="5a86c-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="5a86c-112">Длина в байтах структуры **var** .</span><span class="sxs-lookup"><span data-stu-id="5a86c-112">The length, in bytes, of the **Var** structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a86c-113">**ввалуеленгс**</span><span class="sxs-lookup"><span data-stu-id="5a86c-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="5a86c-114">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="5a86c-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="5a86c-115">Длина (в байтах) элемента **value** .</span><span class="sxs-lookup"><span data-stu-id="5a86c-115">The length, in bytes, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="5a86c-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="5a86c-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="5a86c-117">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="5a86c-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="5a86c-118">Тип данных в ресурсе версии.</span><span class="sxs-lookup"><span data-stu-id="5a86c-118">The type of data in the version resource.</span></span> <span data-ttu-id="5a86c-119">Этот элемент равен 1, если ресурс версии содержит текстовые данные, и 0, если ресурс версии содержит двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="5a86c-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="5a86c-120">**сзкэй**</span><span class="sxs-lookup"><span data-stu-id="5a86c-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="5a86c-121">Тип: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="5a86c-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="5a86c-122">Строка в Юникоде L "Translation".</span><span class="sxs-lookup"><span data-stu-id="5a86c-122">The Unicode string L"Translation".</span></span>

</dd> <dt>

<span data-ttu-id="5a86c-123">**Заполнение**</span><span class="sxs-lookup"><span data-stu-id="5a86c-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="5a86c-124">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="5a86c-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="5a86c-125">Столько нуля слов, сколько необходимо, чтобы вычислить **значение** элемента на 32-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="5a86c-125">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="5a86c-126">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5a86c-126">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="5a86c-127">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5a86c-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="5a86c-128">Массив из одного или нескольких значений, которые являются парами идентификаторов кодовых страниц.</span><span class="sxs-lookup"><span data-stu-id="5a86c-128">An array of one or more values that are language and code page identifier pairs.</span></span> <span data-ttu-id="5a86c-129">Дополнительные сведения см. в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="5a86c-129">For additional information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a86c-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a86c-130">Remarks</span></span>

<span data-ttu-id="5a86c-131">Эта структура не является истинной структурой языка C, так как она содержит члены переменной длины.</span><span class="sxs-lookup"><span data-stu-id="5a86c-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="5a86c-132">Эта структура была создана только для описания организации данных в ресурсе версии и не отображается ни в одном из файлов заголовков, поставляемых вместе с пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="5a86c-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="5a86c-133">Если вы используете структуру **var** для перечисления языков, поддерживаемых приложением или библиотекой DLL, вместо использования нескольких ресурсов версий, используйте элемент **value** для хранения массива значений **типа DWORD** , указывающих на язык и кодовую страницу, поддерживаемые этим файлом.</span><span class="sxs-lookup"><span data-stu-id="5a86c-133">If you use the **Var** structure to list the languages your application or DLL supports instead of using multiple version resources, use the **Value** member to contain an array of **DWORD** values indicating the language and code page combinations supported by this file.</span></span> <span data-ttu-id="5a86c-134">Слово нижнего порядка для каждого **DWORD** должно содержать идентификатор языка Майкрософт, а в высоком порядке слово должно содержать номер кодовой страницы IBM.</span><span class="sxs-lookup"><span data-stu-id="5a86c-134">The low-order word of each **DWORD** must contain a Microsoft language identifier, and the high-order word must contain the IBM code page number.</span></span> <span data-ttu-id="5a86c-135">Слово в высоком или низком порядке может быть равно нулю, что означает, что файл не зависит от языка или кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="5a86c-135">Either high-order or low-order word can be zero, indicating that the file is language or code page independent.</span></span> <span data-ttu-id="5a86c-136">Если структура **var** пропущена, файл будет интерпретирован как независимо от языка и кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="5a86c-136">If the **Var** structure is omitted, the file will be interpreted as both language and code page independent.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a86c-137">Требования</span><span class="sxs-lookup"><span data-stu-id="5a86c-137">Requirements</span></span>



| <span data-ttu-id="5a86c-138">Требование</span><span class="sxs-lookup"><span data-stu-id="5a86c-138">Requirement</span></span> | <span data-ttu-id="5a86c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="5a86c-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5a86c-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a86c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5a86c-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a86c-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5a86c-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a86c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5a86c-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a86c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5a86c-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a86c-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a86c-145">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5a86c-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5a86c-146">**варфилеинфо**</span><span class="sxs-lookup"><span data-stu-id="5a86c-146">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="5a86c-147">**стрингфилеинфо**</span><span class="sxs-lookup"><span data-stu-id="5a86c-147">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="5a86c-148">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="5a86c-148">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="5a86c-149">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="5a86c-149">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="5a86c-150">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5a86c-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5a86c-151">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="5a86c-151">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





