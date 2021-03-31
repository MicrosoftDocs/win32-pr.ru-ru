---
title: Свойство порта Ивмусбдевице (Впккоминтерфацес. h)
description: Возвращает идентификатор порта, к которому подключено устройство.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Свойство порта Virtual PC
- Свойство порта Virtual PC, интерфейс Ивмусбдевице
- Интерфейс Ивмусбдевице Virtual PC, свойство Port
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb821921d10b23fdb17256372708650d060e253b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803580"
---
# <a name="ivmusbdeviceport-property"></a><span data-ttu-id="13291-106">Ивмусбдевице: свойство порт:P</span><span class="sxs-lookup"><span data-stu-id="13291-106">IVMUSBDevice::Port property</span></span>

<span data-ttu-id="13291-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="13291-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="13291-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="13291-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="13291-109">Возвращает идентификатор порта, к которому подключено устройство.</span><span class="sxs-lookup"><span data-stu-id="13291-109">Retrieves the identifier of the port on which the device is connected.</span></span>

<span data-ttu-id="13291-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="13291-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="13291-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13291-111">Syntax</span></span>


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a><span data-ttu-id="13291-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="13291-112">Property value</span></span>

<span data-ttu-id="13291-113">Идентификатор порта.</span><span class="sxs-lookup"><span data-stu-id="13291-113">The port identifier.</span></span> <span data-ttu-id="13291-114">Это значение назначается драйвером соединителя USB.</span><span class="sxs-lookup"><span data-stu-id="13291-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13291-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="13291-115">Error codes</span></span>



| <span data-ttu-id="13291-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="13291-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="13291-117">Значение</span><span class="sxs-lookup"><span data-stu-id="13291-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="13291-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="13291-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="13291-119">Метод завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="13291-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="13291-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="13291-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="13291-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="13291-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="13291-122">Требования</span><span class="sxs-lookup"><span data-stu-id="13291-122">Requirements</span></span>



| <span data-ttu-id="13291-123">Требование</span><span class="sxs-lookup"><span data-stu-id="13291-123">Requirement</span></span> | <span data-ttu-id="13291-124">Значение</span><span class="sxs-lookup"><span data-stu-id="13291-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="13291-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13291-125">Minimum supported client</span></span><br/> | <span data-ttu-id="13291-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="13291-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13291-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13291-127">Minimum supported server</span></span><br/> | <span data-ttu-id="13291-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="13291-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="13291-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="13291-129">End of client support</span></span><br/>    | <span data-ttu-id="13291-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="13291-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="13291-131">Продукт</span><span class="sxs-lookup"><span data-stu-id="13291-131">Product</span></span><br/>                  | <span data-ttu-id="13291-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="13291-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="13291-133">Header</span><span class="sxs-lookup"><span data-stu-id="13291-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="13291-134"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="13291-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="13291-135">IID</span><span class="sxs-lookup"><span data-stu-id="13291-135">IID</span></span><br/>                      | <span data-ttu-id="13291-136">IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="13291-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="13291-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13291-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13291-138">**ивмусбдевице**</span><span class="sxs-lookup"><span data-stu-id="13291-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

