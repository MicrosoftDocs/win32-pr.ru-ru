---
title: Свойство Конфигид Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Извлекает уникальный идентификатор виртуальной машины.
ms.assetid: e1679822-d733-4c7a-a5ad-82cbc24a6329
keywords:
- Конфигид свойство Virtual PC
- Конфигид свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Конфигид
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ConfigID
- IVMVirtualMachine.get_ConfigID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291a1faf3012016d35130b21ff4743faae25b794
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071831"
---
# <a name="ivmvirtualmachineconfigid-property"></a><span data-ttu-id="91c50-106">Свойство Ивмвиртуалмачине:: Конфигид</span><span class="sxs-lookup"><span data-stu-id="91c50-106">IVMVirtualMachine::ConfigID property</span></span>

<span data-ttu-id="91c50-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="91c50-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="91c50-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="91c50-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="91c50-109">Извлекает уникальный идентификатор виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="91c50-109">Retrieves the unique identifier for the virtual machine.</span></span>

<span data-ttu-id="91c50-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91c50-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c50-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91c50-111">Syntax</span></span>


```C++
HRESULT get_ConfigID(
  [out, retval] BSTR *virtualMachineConfigID
);
```



## <a name="property-value"></a><span data-ttu-id="91c50-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="91c50-112">Property value</span></span>

<span data-ttu-id="91c50-113">Уникальный идентификатор, идентифицирующий виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="91c50-113">The unique ID that identifies the virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="91c50-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="91c50-114">Error codes</span></span>



| <span data-ttu-id="91c50-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="91c50-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="91c50-116">Значение</span><span class="sxs-lookup"><span data-stu-id="91c50-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="91c50-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91c50-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="91c50-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="91c50-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="91c50-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="91c50-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="91c50-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="91c50-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="91c50-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91c50-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="91c50-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="91c50-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="91c50-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="91c50-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="91c50-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="91c50-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="91c50-125">Требования</span><span class="sxs-lookup"><span data-stu-id="91c50-125">Requirements</span></span>



| <span data-ttu-id="91c50-126">Требование</span><span class="sxs-lookup"><span data-stu-id="91c50-126">Requirement</span></span> | <span data-ttu-id="91c50-127">Значение</span><span class="sxs-lookup"><span data-stu-id="91c50-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c50-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91c50-128">Minimum supported client</span></span><br/> | <span data-ttu-id="91c50-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="91c50-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91c50-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91c50-130">Minimum supported server</span></span><br/> | <span data-ttu-id="91c50-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="91c50-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="91c50-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="91c50-132">End of client support</span></span><br/>    | <span data-ttu-id="91c50-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91c50-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="91c50-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="91c50-134">Product</span></span><br/>                  | <span data-ttu-id="91c50-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="91c50-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="91c50-136">Header</span><span class="sxs-lookup"><span data-stu-id="91c50-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="91c50-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="91c50-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="91c50-138">IID</span><span class="sxs-lookup"><span data-stu-id="91c50-138">IID</span></span><br/>                      | <span data-ttu-id="91c50-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="91c50-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="91c50-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91c50-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c50-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="91c50-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

