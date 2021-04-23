---
title: Свойство Буснумбер Ивмдвддриве (Впккоминтерфацес. h)
description: Возвращает номер шины, к которой подключено устройство.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- Буснумбер свойство Virtual PC
- Буснумбер свойство Virtual PC, интерфейс Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, свойство Буснумбер
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672773"
---
# <a name="ivmdvddrivebusnumber-property"></a><span data-ttu-id="eec7f-106">Свойство Ивмдвддриве:: Буснумбер</span><span class="sxs-lookup"><span data-stu-id="eec7f-106">IVMDVDDrive::BusNumber property</span></span>

<span data-ttu-id="eec7f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eec7f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eec7f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="eec7f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="eec7f-109">Возвращает номер шины, к которой подключено устройство.</span><span class="sxs-lookup"><span data-stu-id="eec7f-109">Retrieves the bus number to which this device is attached.</span></span>

<span data-ttu-id="eec7f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eec7f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec7f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eec7f-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="eec7f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="eec7f-112">Property value</span></span>

<span data-ttu-id="eec7f-113">Номер шины.</span><span class="sxs-lookup"><span data-stu-id="eec7f-113">The bus number.</span></span> <span data-ttu-id="eec7f-114">Например, на шине IDE это значение будет представлять собой либо основное, либо дополнительное расположение.</span><span class="sxs-lookup"><span data-stu-id="eec7f-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eec7f-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="eec7f-115">Error codes</span></span>



| <span data-ttu-id="eec7f-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="eec7f-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="eec7f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eec7f-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eec7f-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eec7f-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="eec7f-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="eec7f-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="eec7f-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="eec7f-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="eec7f-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="eec7f-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="eec7f-122"><dt>Виртуальная машина \_ \_Диск E \_ Недопустимый</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="eec7f-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="eec7f-123">Расположение шины для этого DVD-дисковода не инициализировано должным образом.</span><span class="sxs-lookup"><span data-stu-id="eec7f-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="eec7f-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="eec7f-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="eec7f-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="eec7f-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="eec7f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="eec7f-126">Requirements</span></span>



| <span data-ttu-id="eec7f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="eec7f-127">Requirement</span></span> | <span data-ttu-id="eec7f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="eec7f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec7f-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eec7f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="eec7f-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eec7f-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eec7f-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eec7f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="eec7f-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="eec7f-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="eec7f-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="eec7f-133">End of client support</span></span><br/>    | <span data-ttu-id="eec7f-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eec7f-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eec7f-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="eec7f-135">Product</span></span><br/>                  | <span data-ttu-id="eec7f-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="eec7f-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="eec7f-137">Header</span><span class="sxs-lookup"><span data-stu-id="eec7f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec7f-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec7f-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="eec7f-139">IID</span><span class="sxs-lookup"><span data-stu-id="eec7f-139">IID</span></span><br/>                      | <span data-ttu-id="eec7f-140">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="eec7f-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="eec7f-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eec7f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec7f-142">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="eec7f-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

