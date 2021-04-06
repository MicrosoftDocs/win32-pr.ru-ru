---
title: Свойство Харддискконнектионс Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Возвращает перечисляемую коллекцию подключений к жестким дискам.
ms.assetid: 167eb8af-bbc1-49a8-83fd-8d946b50530d
keywords:
- Харддискконнектионс свойство Virtual PC
- Харддискконнектионс свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Харддискконнектионс
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HardDiskConnections
- IVMVirtualMachine.get_HardDiskConnections
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4a409337dc6fb437a98fe002f6e0d5d4da44b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802686"
---
# <a name="ivmvirtualmachineharddiskconnections-property"></a><span data-ttu-id="971b2-106">Свойство Ивмвиртуалмачине:: Харддискконнектионс</span><span class="sxs-lookup"><span data-stu-id="971b2-106">IVMVirtualMachine::HardDiskConnections property</span></span>

<span data-ttu-id="971b2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="971b2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="971b2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="971b2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="971b2-109">Возвращает перечисляемую коллекцию подключений к жестким дискам.</span><span class="sxs-lookup"><span data-stu-id="971b2-109">Retrieves an enumerable collection of hard disk connections.</span></span>

<span data-ttu-id="971b2-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="971b2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="971b2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="971b2-111">Syntax</span></span>


```C++
HRESULT get_HardDiskConnections(
  [out, retval] IVMHardDiskConnectionCollection **hardDiskConnectionCollection
);
```



## <a name="property-value"></a><span data-ttu-id="971b2-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="971b2-112">Property value</span></span>

<span data-ttu-id="971b2-113">Объект [**ивмхарддискконнектионколлектион**](ivmharddiskconnectioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="971b2-113">An [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="971b2-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="971b2-114">Error codes</span></span>



| <span data-ttu-id="971b2-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="971b2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="971b2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="971b2-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="971b2-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="971b2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="971b2-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="971b2-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="971b2-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="971b2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="971b2-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="971b2-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="971b2-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="971b2-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="971b2-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="971b2-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="971b2-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="971b2-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="971b2-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="971b2-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="971b2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="971b2-125">Requirements</span></span>



| <span data-ttu-id="971b2-126">Требование</span><span class="sxs-lookup"><span data-stu-id="971b2-126">Requirement</span></span> | <span data-ttu-id="971b2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="971b2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="971b2-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="971b2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="971b2-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="971b2-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="971b2-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="971b2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="971b2-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="971b2-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="971b2-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="971b2-132">End of client support</span></span><br/>    | <span data-ttu-id="971b2-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="971b2-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="971b2-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="971b2-134">Product</span></span><br/>                  | <span data-ttu-id="971b2-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="971b2-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="971b2-136">Header</span><span class="sxs-lookup"><span data-stu-id="971b2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="971b2-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="971b2-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="971b2-138">IID</span><span class="sxs-lookup"><span data-stu-id="971b2-138">IID</span></span><br/>                      | <span data-ttu-id="971b2-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="971b2-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="971b2-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="971b2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="971b2-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="971b2-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

