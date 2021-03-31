---
title: Свойство Мануфактурерстринг Ивмусбдевице (Впккоминтерфацес. h)
description: Получает имя изготовителя USB-устройства.
ms.assetid: 0d815887-96bf-4795-a4eb-32fb2f35c57e
keywords:
- Мануфактурерстринг свойство Virtual PC
- Мануфактурерстринг свойство Virtual PC, интерфейс Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, свойство Мануфактурерстринг
topic_type:
- apiref
api_name:
- IVMUSBDevice.ManufacturerString
- IVMUSBDevice.get_ManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8d74cbe737c59e10daf2cf3ee93e4b1f14983f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136719"
---
# <a name="ivmusbdevicemanufacturerstring-property"></a><span data-ttu-id="63ba2-106">Свойство Ивмусбдевице:: Мануфактурерстринг</span><span class="sxs-lookup"><span data-stu-id="63ba2-106">IVMUSBDevice::ManufacturerString property</span></span>

<span data-ttu-id="63ba2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63ba2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63ba2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63ba2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63ba2-109">Получает имя изготовителя USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="63ba2-109">Retrieves the name of the USB device manufacturer.</span></span>

<span data-ttu-id="63ba2-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63ba2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ba2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63ba2-111">Syntax</span></span>


```C++
HRESULT get_ManufacturerString(
  [out, retval] BSTR *manufacturerName
);
```



## <a name="property-value"></a><span data-ttu-id="63ba2-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="63ba2-112">Property value</span></span>

<span data-ttu-id="63ba2-113">Имя изготовителя USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="63ba2-113">The name of the USB device manufacturer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63ba2-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="63ba2-114">Error codes</span></span>



| <span data-ttu-id="63ba2-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="63ba2-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="63ba2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="63ba2-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="63ba2-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63ba2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="63ba2-118">Метод завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="63ba2-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="63ba2-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="63ba2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="63ba2-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="63ba2-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="63ba2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="63ba2-121">Requirements</span></span>



| <span data-ttu-id="63ba2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="63ba2-122">Requirement</span></span> | <span data-ttu-id="63ba2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="63ba2-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63ba2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="63ba2-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63ba2-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63ba2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63ba2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="63ba2-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="63ba2-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="63ba2-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="63ba2-128">End of client support</span></span><br/>    | <span data-ttu-id="63ba2-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63ba2-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="63ba2-130">Продукт</span><span class="sxs-lookup"><span data-stu-id="63ba2-130">Product</span></span><br/>                  | <span data-ttu-id="63ba2-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63ba2-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="63ba2-132">Header</span><span class="sxs-lookup"><span data-stu-id="63ba2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="63ba2-133"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="63ba2-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="63ba2-134">IID</span><span class="sxs-lookup"><span data-stu-id="63ba2-134">IID</span></span><br/>                      | <span data-ttu-id="63ba2-135">IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="63ba2-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="63ba2-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63ba2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ba2-137">**ивмусбдевице**</span><span class="sxs-lookup"><span data-stu-id="63ba2-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

