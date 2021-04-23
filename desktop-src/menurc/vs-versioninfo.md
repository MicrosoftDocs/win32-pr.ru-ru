---
title: Структура VS_VERSIONINFO
description: Представляет организацию данных в ресурсе версии файла. Это корневая структура, которая содержит все остальные структуры сведений о версии файла.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- Меню структуры VS_VERSIONINFO и другие ресурсы
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137554"
---
# <a name="vs_versioninfo-structure"></a><span data-ttu-id="cdfa1-105">\_Структура VS versionInfo</span><span class="sxs-lookup"><span data-stu-id="cdfa1-105">VS\_VERSIONINFO structure</span></span>

<span data-ttu-id="cdfa1-106">Представляет организацию данных в ресурсе версии файла.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="cdfa1-107">Это корневая структура, которая содержит все остальные структуры сведений о версии файла.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-107">It is the root structure that contains all other file-version information structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdfa1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdfa1-108">Syntax</span></span>


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="cdfa1-109">Члены</span><span class="sxs-lookup"><span data-stu-id="cdfa1-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="cdfa1-110">**вленгс**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="cdfa1-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdfa1-112">Длина в байтах структуры **VS \_ versionInfo** .</span><span class="sxs-lookup"><span data-stu-id="cdfa1-112">The length, in bytes, of the **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="cdfa1-113">Эта длина не включает в себя заполнение, которое обеспечивает соответствие всех последующих данных ресурсов версии на 32-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-113">This length does not include any padding that aligns any subsequent version resource data on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="cdfa1-114">**ввалуеленгс**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-114">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="cdfa1-115">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdfa1-116">Длина (в байтах) элемента **value** .</span><span class="sxs-lookup"><span data-stu-id="cdfa1-116">The length, in bytes, of the **Value** member.</span></span> <span data-ttu-id="cdfa1-117">Это значение равно нулю, если нет элемента **значения** , связанного с текущей структурой версии.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-117">This value is zero if there is no **Value** member associated with the current version structure.</span></span>

</dd> <dt>

<span data-ttu-id="cdfa1-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="cdfa1-119">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdfa1-120">Тип данных в ресурсе версии.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-120">The type of data in the version resource.</span></span> <span data-ttu-id="cdfa1-121">Этот элемент равен 1, если ресурс версии содержит текстовые данные, и 0, если ресурс версии содержит двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="cdfa1-122">**сзкэй**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="cdfa1-123">Тип: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="cdfa1-124">Строка Юникода L " \_ \_ сведения о версии VS".</span><span class="sxs-lookup"><span data-stu-id="cdfa1-124">The Unicode string L"VS\_VERSION\_INFO".</span></span>

</dd> <dt>

<span data-ttu-id="cdfa1-125">**Padding1**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-125">**Padding1**</span></span>
</dt> <dd>

<span data-ttu-id="cdfa1-126">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdfa1-127">Содержит столько нуль слов, сколько необходимо для выровняйте **значение** элемента на 32-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-127">Contains as many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="cdfa1-128">**Значение**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-128">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="cdfa1-129">Тип: **[ **VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-129">Type: **[**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span></span>

</dd> <dd>

<span data-ttu-id="cdfa1-130">Произвольные данные, связанные с этой структурой **VS \_ versionInfo** .</span><span class="sxs-lookup"><span data-stu-id="cdfa1-130">Arbitrary data associated with this **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="cdfa1-131">Член **ввалуеленгс** указывает длину этого элемента; Если **ввалуеленгс** равен нулю, этот элемент не существует.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-131">The **wValueLength** member specifies the length of this member; if **wValueLength** is zero, this member does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="cdfa1-132">**Padding2**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-132">**Padding2**</span></span>
</dt> <dd>

<span data-ttu-id="cdfa1-133">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdfa1-134">Столько нуля слов, сколько необходимо для выровняйте **дочернего** элемента на 32-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-134">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span> <span data-ttu-id="cdfa1-135">Эти байты не включены в **ввалуеленгс**.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-135">These bytes are not included in **wValueLength**.</span></span> <span data-ttu-id="cdfa1-136">Этот член является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-136">This member is optional.</span></span>

</dd> <dt>

<span data-ttu-id="cdfa1-137">**Children**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-137">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="cdfa1-138">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdfa1-139">Массив с нулевой или одной структурой [**стрингфилеинфо**](stringfileinfo.md) и нулевой или одной структурой [**варфилеинфо**](varfileinfo.md) , являющихся дочерними по отношению к текущей структуре **VS \_ versionInfo** .</span><span class="sxs-lookup"><span data-stu-id="cdfa1-139">An array of zero or one [**StringFileInfo**](stringfileinfo.md) structures, and zero or one [**VarFileInfo**](varfileinfo.md) structures that are children of the current **VS\_VERSIONINFO** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdfa1-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdfa1-140">Remarks</span></span>

<span data-ttu-id="cdfa1-141">Эта структура не является истинной структурой языка C, так как она содержит члены переменной длины.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-141">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="cdfa1-142">Эта структура была создана только для описания организации данных в ресурсе версии и не отображается ни в одном из файлов заголовков, поставляемых вместе с пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="cdfa1-142">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdfa1-143">Требования</span><span class="sxs-lookup"><span data-stu-id="cdfa1-143">Requirements</span></span>



| <span data-ttu-id="cdfa1-144">Требование</span><span class="sxs-lookup"><span data-stu-id="cdfa1-144">Requirement</span></span> | <span data-ttu-id="cdfa1-145">Значение</span><span class="sxs-lookup"><span data-stu-id="cdfa1-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="cdfa1-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdfa1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cdfa1-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdfa1-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cdfa1-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdfa1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cdfa1-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdfa1-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cdfa1-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdfa1-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="cdfa1-151">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cdfa1-152">**стрингфилеинфо**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-152">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="cdfa1-153">**VerQueryValue**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-153">**VerQueryValue**</span></span>](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[<span data-ttu-id="cdfa1-154">**варфилеинфо**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-154">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="cdfa1-155">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-155">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

<span data-ttu-id="cdfa1-156">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="cdfa1-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cdfa1-157">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="cdfa1-157">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





