---
title: Идвритефонтфаллбаккбуилдер Аддмаппинг, метод
description: Добавляет одно сопоставление в список. Вызывайте его один раз для каждого дополнительного сопоставления.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Непосредственная запись метода Аддмаппинг
- Прямая запись метода Аддмаппинг, интерфейс Идвритефонтфаллбаккбуилдер
- Прямая запись интерфейса Идвритефонтфаллбаккбуилдер, метод Аддмаппинг
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415796"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a><span data-ttu-id="7b26d-107">Метод Идвритефонтфаллбаккбуилдер:: Аддмаппинг</span><span class="sxs-lookup"><span data-stu-id="7b26d-107">IDWriteFontFallbackBuilder::AddMapping method</span></span>

<span data-ttu-id="7b26d-108">Добавляет одно сопоставление в список.</span><span class="sxs-lookup"><span data-stu-id="7b26d-108">Appends a single mapping to the list.</span></span> <span data-ttu-id="7b26d-109">Вызывайте его один раз для каждого дополнительного сопоставления.</span><span class="sxs-lookup"><span data-stu-id="7b26d-109">Call this once for each additional mapping.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b26d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b26d-110">Syntax</span></span>


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a><span data-ttu-id="7b26d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b26d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b26d-112">*остаются*</span><span class="sxs-lookup"><span data-stu-id="7b26d-112">*ranges*</span></span> 
</dt> <dd>

<span data-ttu-id="7b26d-113">Тип: \**\* [**дврите \_ \_ диапазон Юникода**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)* _</span><span class="sxs-lookup"><span data-stu-id="7b26d-113">Type: \**[**DWRITE\_UNICODE\_RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\** _</span></span>

<span data-ttu-id="7b26d-114">Диапазоны Юникода, которые применяются к этому сопоставлению.</span><span class="sxs-lookup"><span data-stu-id="7b26d-114">Unicode ranges that apply to this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="7b26d-115">_rangesCount \*</span><span class="sxs-lookup"><span data-stu-id="7b26d-115">_rangesCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="7b26d-116">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="7b26d-116">Type: **UINT32**</span></span>

<span data-ttu-id="7b26d-117">Число диапазонов Юникода.</span><span class="sxs-lookup"><span data-stu-id="7b26d-117">Number of Unicode ranges.</span></span>

</dd> <dt>

<span data-ttu-id="7b26d-118">*таржетфамилинамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b26d-118">*targetFamilyNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b26d-119">Тип: **const WCHAR \* \***</span><span class="sxs-lookup"><span data-stu-id="7b26d-119">Type: **const WCHAR\*\***</span></span>

<span data-ttu-id="7b26d-120">Список строк имен целевых семейств.</span><span class="sxs-lookup"><span data-stu-id="7b26d-120">List of target family name strings.</span></span>

</dd> <dt>

<span data-ttu-id="7b26d-121">*таржетфамилинамескаунт*</span><span class="sxs-lookup"><span data-stu-id="7b26d-121">*targetFamilyNamesCount*</span></span> 
</dt> <dd>

<span data-ttu-id="7b26d-122">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="7b26d-122">Type: **UINT32**</span></span>

<span data-ttu-id="7b26d-123">Число имен целевых семейств.</span><span class="sxs-lookup"><span data-stu-id="7b26d-123">Number of target family names.</span></span>

</dd> <dt>

<span data-ttu-id="7b26d-124">*фонтколлектион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7b26d-124">*fontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b26d-125">Тип: **[ **идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span><span class="sxs-lookup"><span data-stu-id="7b26d-125">Type: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span></span>

<span data-ttu-id="7b26d-126">Необязательная коллекция явных шрифтов для этого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="7b26d-126">Optional explicit font collection for this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="7b26d-127">*localeName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7b26d-127">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b26d-128">Тип: \**const WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="7b26d-128">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="7b26d-129">Языковой стандарт контекста.</span><span class="sxs-lookup"><span data-stu-id="7b26d-129">Locale of the context.</span></span>

</dd> <dt>

<span data-ttu-id="7b26d-130">_baseFamilyName \* \[ в, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="7b26d-130">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b26d-131">Тип: \**const WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="7b26d-131">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="7b26d-132">Имя базового семейства для сопоставления, если применимо.</span><span class="sxs-lookup"><span data-stu-id="7b26d-132">Base family name to match against, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="7b26d-133">_scale \*</span><span class="sxs-lookup"><span data-stu-id="7b26d-133">_scale\*</span></span> 
</dt> <dd>

<span data-ttu-id="7b26d-134">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="7b26d-134">Type: **FLOAT**</span></span>

<span data-ttu-id="7b26d-135">Коэффициент масштабирования для умножения целевого шрифта результата на.</span><span class="sxs-lookup"><span data-stu-id="7b26d-135">Scale factor to multiply the result target font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b26d-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b26d-136">Return value</span></span>

<span data-ttu-id="7b26d-137">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7b26d-137">Type: **HRESULT**</span></span>

<span data-ttu-id="7b26d-138">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7b26d-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7b26d-139">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7b26d-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b26d-140">Требования</span><span class="sxs-lookup"><span data-stu-id="7b26d-140">Requirements</span></span>



| <span data-ttu-id="7b26d-141">Требование</span><span class="sxs-lookup"><span data-stu-id="7b26d-141">Requirement</span></span> | <span data-ttu-id="7b26d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="7b26d-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b26d-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b26d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7b26d-144">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="7b26d-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="7b26d-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b26d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7b26d-146">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="7b26d-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="7b26d-147">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="7b26d-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="7b26d-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b26d-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="7b26d-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7b26d-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b26d-150"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b26d-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7b26d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7b26d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b26d-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b26d-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b26d-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b26d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b26d-154">**идвритефонтфаллбаккбуилдер**</span><span class="sxs-lookup"><span data-stu-id="7b26d-154">**IDWriteFontFallbackBuilder**</span></span>](idwritefontfallbackbuilder.md)
</dt> </dl>

 

