---
title: Свойство Двдромдривес Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Получает перечисляемую коллекцию компакт-дисков и DVD-дисководов, подключенных к виртуальной машине.
ms.assetid: e9e7d912-568f-4a3d-85cf-63f6fa99cb19
keywords:
- Двдромдривес свойство Virtual PC
- Двдромдривес свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Двдромдривес
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DVDROMDrives
- IVMVirtualMachine.get_DVDROMDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9980d783b19bfef7ce5437253b7923d6e6a2ebf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535174"
---
# <a name="ivmvirtualmachinedvdromdrives-property"></a><span data-ttu-id="02c9f-106">Ивмвиртуалмачине: свойство Вдромдривес:D</span><span class="sxs-lookup"><span data-stu-id="02c9f-106">IVMVirtualMachine::DVDROMDrives property</span></span>

<span data-ttu-id="02c9f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02c9f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="02c9f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="02c9f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="02c9f-109">Получает перечисляемую коллекцию компакт-дисков и DVD-дисководов, подключенных к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="02c9f-109">Retrieves an enumerable collection of CD and DVD drives attached to the virtual machine.</span></span>

<span data-ttu-id="02c9f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="02c9f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c9f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02c9f-111">Syntax</span></span>


```C++
HRESULT get_DVDROMDrives(
  [out, retval] IVMDVDDriveCollection **dvdROMCollection
);
```



## <a name="property-value"></a><span data-ttu-id="02c9f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="02c9f-112">Property value</span></span>

<span data-ttu-id="02c9f-113">Объект [**ивмдвддривеколлектион**](ivmdvddrivecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="02c9f-113">An [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02c9f-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="02c9f-114">Error codes</span></span>



| <span data-ttu-id="02c9f-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="02c9f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="02c9f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="02c9f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="02c9f-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="02c9f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="02c9f-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="02c9f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="02c9f-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="02c9f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="02c9f-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="02c9f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="02c9f-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="02c9f-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="02c9f-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="02c9f-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="02c9f-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="02c9f-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="02c9f-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="02c9f-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="02c9f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="02c9f-125">Requirements</span></span>



| <span data-ttu-id="02c9f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="02c9f-126">Requirement</span></span> | <span data-ttu-id="02c9f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="02c9f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c9f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02c9f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="02c9f-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="02c9f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02c9f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02c9f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="02c9f-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="02c9f-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="02c9f-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="02c9f-132">End of client support</span></span><br/>    | <span data-ttu-id="02c9f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02c9f-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="02c9f-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="02c9f-134">Product</span></span><br/>                  | <span data-ttu-id="02c9f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="02c9f-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="02c9f-136">Header</span><span class="sxs-lookup"><span data-stu-id="02c9f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="02c9f-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="02c9f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="02c9f-138">IID</span><span class="sxs-lookup"><span data-stu-id="02c9f-138">IID</span></span><br/>                      | <span data-ttu-id="02c9f-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="02c9f-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="02c9f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02c9f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c9f-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="02c9f-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

