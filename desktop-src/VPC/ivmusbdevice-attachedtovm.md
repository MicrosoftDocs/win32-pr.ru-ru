---
title: Свойство Аттачедтовм Ивмусбдевице (Впккоминтерфацес. h)
description: Извлекает имя виртуальной машины, к которой подключено USB-устройство.
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- Аттачедтовм свойство Virtual PC
- Аттачедтовм свойство Virtual PC, интерфейс Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, свойство Аттачедтовм
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071692"
---
# <a name="ivmusbdeviceattachedtovm-property"></a><span data-ttu-id="dcc05-106">Свойство Ивмусбдевице:: Аттачедтовм</span><span class="sxs-lookup"><span data-stu-id="dcc05-106">IVMUSBDevice::AttachedToVM property</span></span>

<span data-ttu-id="dcc05-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dcc05-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dcc05-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dcc05-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dcc05-109">Извлекает имя виртуальной машины, к которой подключено USB-устройство.</span><span class="sxs-lookup"><span data-stu-id="dcc05-109">Retrieves the name of the virtual machine to which the USB Device is attached.</span></span>

<span data-ttu-id="dcc05-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dcc05-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc05-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcc05-111">Syntax</span></span>


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a><span data-ttu-id="dcc05-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dcc05-112">Property value</span></span>

<span data-ttu-id="dcc05-113">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dcc05-113">The name of the virtual machine (VM).</span></span>

## <a name="error-codes"></a><span data-ttu-id="dcc05-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dcc05-114">Error codes</span></span>



| <span data-ttu-id="dcc05-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="dcc05-115">Name/value</span></span>                                                                                                                                                           | <span data-ttu-id="dcc05-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dcc05-116">Meaning</span></span>                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcc05-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dcc05-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="dcc05-118">Устройство подключено к виртуальной машине и возвращается имя.</span><span class="sxs-lookup"><span data-stu-id="dcc05-118">The device is attached to the VM, and its name is returned.</span></span><br/> |
| <dl> <span data-ttu-id="dcc05-119"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dcc05-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                           | <span data-ttu-id="dcc05-120">Устройство подключено к узлу.</span><span class="sxs-lookup"><span data-stu-id="dcc05-120">The device is attached to the host.</span></span><br/>                         |
| <dl> <span data-ttu-id="dcc05-121"><dt>Виртуальная машина \_ 0xA00400929 \_ \_ внешняя \_ Виртуальная машина USB</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dcc05-121"><dt>VM\_E\_USB\_EXTERNAL\_VM</dt> <dt>0xA00400929</dt></span></span> </dl> | <span data-ttu-id="dcc05-122">Устройство подключено к виртуальной машине в другом сеансе пользователя.</span><span class="sxs-lookup"><span data-stu-id="dcc05-122">The device is attached to a VM in another user session.</span></span><br/>     |
| <dl> <span data-ttu-id="dcc05-123"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="dcc05-123"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="dcc05-124">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dcc05-124">The parameter is **NULL**.</span></span><br/>                                  |



## <a name="requirements"></a><span data-ttu-id="dcc05-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dcc05-125">Requirements</span></span>



| <span data-ttu-id="dcc05-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dcc05-126">Requirement</span></span> | <span data-ttu-id="dcc05-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dcc05-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc05-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dcc05-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc05-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dcc05-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dcc05-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dcc05-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc05-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dcc05-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dcc05-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dcc05-132">End of client support</span></span><br/>    | <span data-ttu-id="dcc05-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dcc05-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dcc05-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="dcc05-134">Product</span></span><br/>                  | <span data-ttu-id="dcc05-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dcc05-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dcc05-136">Header</span><span class="sxs-lookup"><span data-stu-id="dcc05-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcc05-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcc05-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dcc05-138">IID</span><span class="sxs-lookup"><span data-stu-id="dcc05-138">IID</span></span><br/>                      | <span data-ttu-id="dcc05-139">IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="dcc05-139">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="dcc05-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcc05-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc05-141">**ивмусбдевице**</span><span class="sxs-lookup"><span data-stu-id="dcc05-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

