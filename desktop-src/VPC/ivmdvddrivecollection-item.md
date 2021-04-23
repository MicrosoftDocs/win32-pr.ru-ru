---
title: Свойство Item Ивмдвддривеколлектион (Впккоминтерфацес. h)
description: Извлекает объект CD или DVD-дисковода, соответствующий указанному индексу.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмдвддривеколлектион
- Интерфейс Ивмдвддривеколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc631ab6d4de3ab65071bf2b8692236f3ae03ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071584"
---
# <a name="ivmdvddrivecollectionitem-property"></a><span data-ttu-id="22f9a-106">Свойство Ивмдвддривеколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="22f9a-106">IVMDVDDriveCollection::Item property</span></span>

<span data-ttu-id="22f9a-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="22f9a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="22f9a-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="22f9a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="22f9a-109">Извлекает объект CD или DVD-дисковода, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="22f9a-109">Retrieves the CD or DVD drive object that corresponds to the specified index.</span></span>

<span data-ttu-id="22f9a-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="22f9a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="22f9a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22f9a-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a><span data-ttu-id="22f9a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="22f9a-112">Property value</span></span>

<span data-ttu-id="22f9a-113">Объект [**ивмдвддриве**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="22f9a-113">The [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="22f9a-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="22f9a-114">Error codes</span></span>



| <span data-ttu-id="22f9a-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="22f9a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="22f9a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="22f9a-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22f9a-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="22f9a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="22f9a-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="22f9a-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="22f9a-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="22f9a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="22f9a-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="22f9a-120">The parameter is **NULL**.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="22f9a-121"><dt>Д \_ Сбой</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="22f9a-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="22f9a-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="22f9a-122">An unexpected error has occurred.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="22f9a-123"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="22f9a-123"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="22f9a-124">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="22f9a-124">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="22f9a-125"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="22f9a-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="22f9a-126">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="22f9a-126">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="22f9a-127"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="22f9a-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="22f9a-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="22f9a-128">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="22f9a-129">Требования</span><span class="sxs-lookup"><span data-stu-id="22f9a-129">Requirements</span></span>



| <span data-ttu-id="22f9a-130">Требование</span><span class="sxs-lookup"><span data-stu-id="22f9a-130">Requirement</span></span> | <span data-ttu-id="22f9a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="22f9a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="22f9a-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22f9a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="22f9a-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="22f9a-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22f9a-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22f9a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="22f9a-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="22f9a-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="22f9a-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="22f9a-136">End of client support</span></span><br/>    | <span data-ttu-id="22f9a-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="22f9a-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="22f9a-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="22f9a-138">Product</span></span><br/>                  | <span data-ttu-id="22f9a-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="22f9a-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="22f9a-140">Header</span><span class="sxs-lookup"><span data-stu-id="22f9a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="22f9a-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="22f9a-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="22f9a-142">IID</span><span class="sxs-lookup"><span data-stu-id="22f9a-142">IID</span></span><br/>                      | <span data-ttu-id="22f9a-143">IID \_ ивмдвддривеколлектион определен как bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="22f9a-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="22f9a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22f9a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22f9a-145">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="22f9a-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="22f9a-146">**ивмдвддривеколлектион**</span><span class="sxs-lookup"><span data-stu-id="22f9a-146">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

