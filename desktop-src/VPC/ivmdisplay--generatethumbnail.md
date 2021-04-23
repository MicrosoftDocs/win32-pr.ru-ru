---
title: Метод _GenerateThumbnail Ивмдисплай (Впккоминтерфацес. h)
description: Извлекает массив пикселей, представляющий эскиз изображения экрана виртуальной машины. | Метод _GenerateThumbnail Ивмдисплай (Впккоминтерфацес. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail метод Virtual PC
- _GenerateThumbnail метод Virtual PC, интерфейс Ивмдисплай
- Ивмдисплай интерфейс Virtual PC, метод _GenerateThumbnail
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105651475"
---
# <a name="ivmdisplay_generatethumbnail-method"></a><span data-ttu-id="36df4-107">Метод Ивмдисплай:: \_ GenerateThumbnail</span><span class="sxs-lookup"><span data-stu-id="36df4-107">IVMDisplay::\_GenerateThumbnail method</span></span>

<span data-ttu-id="36df4-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="36df4-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="36df4-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="36df4-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="36df4-110">Извлекает массив пикселей, представляющий эскиз изображения экрана виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="36df4-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="36df4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36df4-111">Syntax</span></span>


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a><span data-ttu-id="36df4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="36df4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36df4-113">*сумбнаилимаже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="36df4-113">*thumbnailImage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36df4-114">Массив пикселей, представляющий эскиз изображения экрана виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="36df4-114">The array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36df4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36df4-115">Return value</span></span>

<span data-ttu-id="36df4-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="36df4-116">This method can return one of these values.</span></span>



| <span data-ttu-id="36df4-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="36df4-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="36df4-118">Описание</span><span class="sxs-lookup"><span data-stu-id="36df4-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="36df4-119"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="36df4-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="36df4-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="36df4-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="36df4-121"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="36df4-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="36df4-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="36df4-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="36df4-123"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="36df4-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="36df4-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="36df4-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36df4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36df4-125">Remarks</span></span>

<span data-ttu-id="36df4-126">Этот интерфейс возвращает эскиз более эффективно, чем свойство [**эскиза**](ivmdisplay-thumbnail.md) , но не может использоваться из скриптов клиентов.</span><span class="sxs-lookup"><span data-stu-id="36df4-126">This interface returns the thumbnail more efficiently than the [**Thumbnail**](ivmdisplay-thumbnail.md) property, but is not usable from scripting clients.</span></span> <span data-ttu-id="36df4-127">Размер эскиза всегда составляет 64 пикселей в ширину на 48 пикселей в высоком масштабе.</span><span class="sxs-lookup"><span data-stu-id="36df4-127">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="36df4-128">Каждый пиксель имеет 32 бит, где верхние 8 бит представляют синее значение пикселя, а следующие 8 бит представляют зеленое значение пикселя, а следующие 8 бит представляют красную величину пикселя.</span><span class="sxs-lookup"><span data-stu-id="36df4-128">Each pixel is 32 bits, where the upper 8 bits represent the blue value of the pixel, the next 8 bits represent the green value of the pixel, and the next 8 bits represent the red value of the pixel.</span></span> <span data-ttu-id="36df4-129">Первые 64 элементов в массиве — это первая строка эскиза, следующие элементы 64 — вторая строка и т. д.</span><span class="sxs-lookup"><span data-stu-id="36df4-129">The first 64 elements in the array is the first row of the thumbnail, the next 64 elements is the second row, and so on.</span></span> <span data-ttu-id="36df4-130">Этот метод возвращает статический массив пикселей, который более эффективен, чем возврат **SAFEARRAY** значений **типа Variant** , но несовместим с клиентами скриптов.</span><span class="sxs-lookup"><span data-stu-id="36df4-130">This method returns a static array of pixels, which is more efficient than returning a **SAFEARRAY** of **VARIANT** values, but is not compatible with scripting clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="36df4-131">Требования</span><span class="sxs-lookup"><span data-stu-id="36df4-131">Requirements</span></span>



| <span data-ttu-id="36df4-132">Требование</span><span class="sxs-lookup"><span data-stu-id="36df4-132">Requirement</span></span> | <span data-ttu-id="36df4-133">Значение</span><span class="sxs-lookup"><span data-stu-id="36df4-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="36df4-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36df4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="36df4-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="36df4-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36df4-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36df4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="36df4-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="36df4-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="36df4-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="36df4-138">End of client support</span></span><br/>    | <span data-ttu-id="36df4-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="36df4-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="36df4-140">Продукт</span><span class="sxs-lookup"><span data-stu-id="36df4-140">Product</span></span><br/>                  | <span data-ttu-id="36df4-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="36df4-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="36df4-142">Header</span><span class="sxs-lookup"><span data-stu-id="36df4-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="36df4-143"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="36df4-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="36df4-144">IID</span><span class="sxs-lookup"><span data-stu-id="36df4-144">IID</span></span><br/>                      | <span data-ttu-id="36df4-145">IID \_ ивмдисплай определен как 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="36df4-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="36df4-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36df4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36df4-147">**ивмдисплай**</span><span class="sxs-lookup"><span data-stu-id="36df4-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

