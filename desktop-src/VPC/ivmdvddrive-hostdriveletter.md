---
title: Свойство Хостдривелеттер Ивмдвддриве (Впккоминтерфацес. h)
description: Буква диска узла, заданная для этого устройства.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Хостдривелеттер свойство Virtual PC
- Хостдривелеттер свойство Virtual PC, интерфейс Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, свойство Хостдривелеттер
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801972"
---
# <a name="ivmdvddrivehostdriveletter-property"></a><span data-ttu-id="ae7af-106">Свойство Ивмдвддриве:: Хостдривелеттер</span><span class="sxs-lookup"><span data-stu-id="ae7af-106">IVMDVDDrive::HostDriveLetter property</span></span>

<span data-ttu-id="ae7af-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ae7af-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ae7af-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ae7af-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ae7af-109">Извлекает букву диска узла, установленного для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="ae7af-109">Retrieves the letter of the host drive set for this device.</span></span>

<span data-ttu-id="ae7af-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ae7af-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7af-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae7af-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="ae7af-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ae7af-112">Property value</span></span>

<span data-ttu-id="ae7af-113">Буква диска.</span><span class="sxs-lookup"><span data-stu-id="ae7af-113">The drive letter.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ae7af-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ae7af-114">Error codes</span></span>



| <span data-ttu-id="ae7af-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="ae7af-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="ae7af-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ae7af-116">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae7af-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ae7af-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="ae7af-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ae7af-118">The operation was successful.</span></span><br/>                             |
| <dl> <span data-ttu-id="ae7af-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="ae7af-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="ae7af-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ae7af-120">The parameter is **NULL**.</span></span><br/>                                |
| <dl> <span data-ttu-id="ae7af-121"><dt>Д \_ Сбой</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="ae7af-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="ae7af-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ae7af-122">An unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="ae7af-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ae7af-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="ae7af-124">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ae7af-124">The virtual machine could not be found.</span></span><br/>                   |
| <dl> <span data-ttu-id="ae7af-125"><dt>Виртуальная машина \_ \_ \_ Неверный \_ тип носителя</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="ae7af-125"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="ae7af-126">Носитель, записываемый этим DVD-дисководом, не является диском узла.</span><span class="sxs-lookup"><span data-stu-id="ae7af-126">The media captured by this DVD drive is not a host drive.</span></span><br/> |
| <dl> <span data-ttu-id="ae7af-127"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ae7af-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="ae7af-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ae7af-128">An unexpected error has occurred.</span></span><br/>                         |



## <a name="requirements"></a><span data-ttu-id="ae7af-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ae7af-129">Requirements</span></span>



| <span data-ttu-id="ae7af-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ae7af-130">Requirement</span></span> | <span data-ttu-id="ae7af-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ae7af-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7af-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae7af-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ae7af-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ae7af-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae7af-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae7af-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ae7af-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae7af-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ae7af-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ae7af-136">End of client support</span></span><br/>    | <span data-ttu-id="ae7af-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ae7af-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ae7af-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="ae7af-138">Product</span></span><br/>                  | <span data-ttu-id="ae7af-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ae7af-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ae7af-140">Header</span><span class="sxs-lookup"><span data-stu-id="ae7af-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae7af-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae7af-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ae7af-142">IID</span><span class="sxs-lookup"><span data-stu-id="ae7af-142">IID</span></span><br/>                      | <span data-ttu-id="ae7af-143">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="ae7af-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ae7af-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae7af-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae7af-145">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="ae7af-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

