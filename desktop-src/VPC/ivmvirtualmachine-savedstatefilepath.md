---
title: Свойство Саведстатефилепас Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Получает полный путь к сохраненному файлу состояния.
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- Саведстатефилепас свойство Virtual PC
- Саведстатефилепас свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Саведстатефилепас
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9baea53e3fce2455a2bdfa361e56b45b9b65d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137006"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a><span data-ttu-id="fd0e5-106">Свойство Ивмвиртуалмачине:: Саведстатефилепас</span><span class="sxs-lookup"><span data-stu-id="fd0e5-106">IVMVirtualMachine::SavedStateFilePath property</span></span>

<span data-ttu-id="fd0e5-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd0e5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd0e5-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd0e5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd0e5-109">Получает полный путь к сохраненному файлу состояния.</span><span class="sxs-lookup"><span data-stu-id="fd0e5-109">Retrieves the full path to the saved state file.</span></span>

<span data-ttu-id="fd0e5-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fd0e5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0e5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd0e5-111">Syntax</span></span>


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a><span data-ttu-id="fd0e5-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fd0e5-112">Property value</span></span>

<span data-ttu-id="fd0e5-113">Полный путь к сохраненному файлу состояния виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd0e5-113">The fully qualified path to the virtual machine's saved state file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fd0e5-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fd0e5-114">Error codes</span></span>



| <span data-ttu-id="fd0e5-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="fd0e5-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="fd0e5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fd0e5-116">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd0e5-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd0e5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="fd0e5-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fd0e5-118">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="fd0e5-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="fd0e5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="fd0e5-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fd0e5-120">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="fd0e5-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fd0e5-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="fd0e5-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="fd0e5-122">The configuration is unknown.</span></span><br/>                           |
| <dl> <span data-ttu-id="fd0e5-123"><dt>Виртуальная машина \_ Электронная \_ Виртуальная машина \_ без \_ сохраненного \_ состояния</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="fd0e5-123"><dt>VM\_E\_VM\_NO\_SAVED\_STATE</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="fd0e5-124">Виртуальная машина не имеет связанного файла сохраненного состояния.</span><span class="sxs-lookup"><span data-stu-id="fd0e5-124">The virtual machine has no associated saved state file.</span></span><br/> |
| <dl> <span data-ttu-id="fd0e5-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd0e5-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="fd0e5-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fd0e5-126">An unexpected error has occurred.</span></span><br/>                       |



## <a name="requirements"></a><span data-ttu-id="fd0e5-127">Требования</span><span class="sxs-lookup"><span data-stu-id="fd0e5-127">Requirements</span></span>



| <span data-ttu-id="fd0e5-128">Требование</span><span class="sxs-lookup"><span data-stu-id="fd0e5-128">Requirement</span></span> | <span data-ttu-id="fd0e5-129">Значение</span><span class="sxs-lookup"><span data-stu-id="fd0e5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0e5-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd0e5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0e5-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd0e5-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd0e5-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd0e5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0e5-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd0e5-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd0e5-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fd0e5-134">End of client support</span></span><br/>    | <span data-ttu-id="fd0e5-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd0e5-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd0e5-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="fd0e5-136">Product</span></span><br/>                  | <span data-ttu-id="fd0e5-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd0e5-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd0e5-138">Header</span><span class="sxs-lookup"><span data-stu-id="fd0e5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd0e5-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0e5-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd0e5-140">IID</span><span class="sxs-lookup"><span data-stu-id="fd0e5-140">IID</span></span><br/>                      | <span data-ttu-id="fd0e5-141">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="fd0e5-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fd0e5-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd0e5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0e5-143">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="fd0e5-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

