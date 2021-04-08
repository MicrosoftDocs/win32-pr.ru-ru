---
title: Свойство эскиза Ивмдисплай (Впккоминтерфацес. h)
description: Извлекает массив пикселей, представляющий эскиз изображения экрана виртуальной машины. | Свойство эскиза Ивмдисплай (Впккоминтерфацес. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Свойство эскиза Virtual PC
- Свойство эскиза Virtual PC, интерфейс Ивмдисплай
- Ивмдисплай интерфейс Virtual PC, свойство эскиза
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000045"
---
# <a name="ivmdisplaythumbnail-property"></a><span data-ttu-id="f0c2a-107">Свойство Ивмдисплай:: thumbnail</span><span class="sxs-lookup"><span data-stu-id="f0c2a-107">IVMDisplay::Thumbnail property</span></span>

<span data-ttu-id="f0c2a-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f0c2a-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f0c2a-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f0c2a-110">Извлекает массив пикселей, представляющий эскиз изображения экрана виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

<span data-ttu-id="f0c2a-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c2a-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0c2a-112">Syntax</span></span>


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a><span data-ttu-id="f0c2a-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f0c2a-113">Property value</span></span>

<span data-ttu-id="f0c2a-114">Вариант типа VT \_ array \| VT \_ , СОДЕРЖАЩИЙ записи типа VT \_ UI4, по одному для каждого пикселя эскиза.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-114">A variant of type VT\_ARRAY \| VT\_VARIANT containing entries of type VT\_UI4, one for each pixel in the thumbnail.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0c2a-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f0c2a-115">Error codes</span></span>



| <span data-ttu-id="f0c2a-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="f0c2a-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f0c2a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f0c2a-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f0c2a-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f0c2a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f0c2a-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f0c2a-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="f0c2a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f0c2a-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f0c2a-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f0c2a-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f0c2a-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-123">An unexpected error has occurred.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f0c2a-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0c2a-124">Remarks</span></span>

<span data-ttu-id="f0c2a-125">Этот интерфейс возвращает эскиз менее эффективно, чем метод [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md) , но может использоваться из сценариев клиентов.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-125">This interface returns the thumbnail less efficiently than the [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) method, but is usable from scripting clients.</span></span> <span data-ttu-id="f0c2a-126">Размер эскиза всегда составляет 64 пикселей в ширину на 48 пикселей в высоком масштабе.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-126">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="f0c2a-127">Каждый пиксель имеет 32 бит.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-127">Each pixel is 32 bits.</span></span> <span data-ttu-id="f0c2a-128">Первые 64 элементов в массиве — это первая строка пикселей эскиза, следующие элементы 64 — вторая строка и т. д.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-128">The first 64 elements in the array is the first row of pixels in the thumbnail, the next 64 elements is the second row, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c2a-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f0c2a-129">Requirements</span></span>



| <span data-ttu-id="f0c2a-130">Требование</span><span class="sxs-lookup"><span data-stu-id="f0c2a-130">Requirement</span></span> | <span data-ttu-id="f0c2a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f0c2a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c2a-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0c2a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c2a-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f0c2a-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0c2a-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0c2a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c2a-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0c2a-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f0c2a-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f0c2a-136">End of client support</span></span><br/>    | <span data-ttu-id="f0c2a-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0c2a-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f0c2a-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="f0c2a-138">Product</span></span><br/>                  | <span data-ttu-id="f0c2a-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f0c2a-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f0c2a-140">Header</span><span class="sxs-lookup"><span data-stu-id="f0c2a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0c2a-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c2a-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f0c2a-142">IID</span><span class="sxs-lookup"><span data-stu-id="f0c2a-142">IID</span></span><br/>                      | <span data-ttu-id="f0c2a-143">IID \_ ивмдисплай определен как 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="f0c2a-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f0c2a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0c2a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c2a-145">**ивмдисплай**</span><span class="sxs-lookup"><span data-stu-id="f0c2a-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

