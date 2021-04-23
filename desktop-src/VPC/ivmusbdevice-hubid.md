---
title: Свойство Хубид Ивмусбдевице (Впккоминтерфацес. h)
description: Возвращает идентификатор концентратора, к которому подключено устройство.
ms.assetid: 22e1d8fb-33f4-43a3-883f-174ddafa17c2
keywords:
- Хубид свойство Virtual PC
- Хубид свойство Virtual PC, интерфейс Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, свойство Хубид
topic_type:
- apiref
api_name:
- IVMUSBDevice.HubID
- IVMUSBDevice.get_HubID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53faa79ee999022f993070767846ee4e4723c3a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071832"
---
# <a name="ivmusbdevicehubid-property"></a><span data-ttu-id="700ec-106">Свойство Ивмусбдевице:: Хубид</span><span class="sxs-lookup"><span data-stu-id="700ec-106">IVMUSBDevice::HubID property</span></span>

<span data-ttu-id="700ec-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="700ec-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="700ec-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="700ec-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="700ec-109">Возвращает идентификатор концентратора, к которому подключено устройство.</span><span class="sxs-lookup"><span data-stu-id="700ec-109">Retrieves the identifier of the hub on which the device is connected.</span></span>

<span data-ttu-id="700ec-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="700ec-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="700ec-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="700ec-111">Syntax</span></span>


```C++
HRESULT get_HubID(
  [out, retval] long *hubID
);
```



## <a name="property-value"></a><span data-ttu-id="700ec-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="700ec-112">Property value</span></span>

<span data-ttu-id="700ec-113">Идентификатор концентратора.</span><span class="sxs-lookup"><span data-stu-id="700ec-113">The hub identifier.</span></span> <span data-ttu-id="700ec-114">Это значение назначается драйвером соединителя USB.</span><span class="sxs-lookup"><span data-stu-id="700ec-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="700ec-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="700ec-115">Error codes</span></span>



| <span data-ttu-id="700ec-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="700ec-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="700ec-117">Значение</span><span class="sxs-lookup"><span data-stu-id="700ec-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="700ec-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="700ec-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="700ec-119">Метод завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="700ec-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="700ec-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="700ec-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="700ec-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="700ec-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="700ec-122">Требования</span><span class="sxs-lookup"><span data-stu-id="700ec-122">Requirements</span></span>



| <span data-ttu-id="700ec-123">Требование</span><span class="sxs-lookup"><span data-stu-id="700ec-123">Requirement</span></span> | <span data-ttu-id="700ec-124">Значение</span><span class="sxs-lookup"><span data-stu-id="700ec-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="700ec-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="700ec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="700ec-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="700ec-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="700ec-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="700ec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="700ec-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="700ec-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="700ec-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="700ec-129">End of client support</span></span><br/>    | <span data-ttu-id="700ec-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="700ec-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="700ec-131">Продукт</span><span class="sxs-lookup"><span data-stu-id="700ec-131">Product</span></span><br/>                  | <span data-ttu-id="700ec-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="700ec-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="700ec-133">Header</span><span class="sxs-lookup"><span data-stu-id="700ec-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="700ec-134"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="700ec-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="700ec-135">IID</span><span class="sxs-lookup"><span data-stu-id="700ec-135">IID</span></span><br/>                      | <span data-ttu-id="700ec-136">IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="700ec-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="700ec-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="700ec-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700ec-138">**ивмусбдевице**</span><span class="sxs-lookup"><span data-stu-id="700ec-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

