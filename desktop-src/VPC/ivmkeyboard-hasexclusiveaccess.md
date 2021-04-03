---
title: Свойство Хасексклусивеакцесс Ивмкэйбоард (Впккоминтерфацес. h)
description: Указывает, имеет ли этот объект исключительный контроль над устройством клавиатуры виртуальной машины.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Хасексклусивеакцесс свойство Virtual PC
- Хасексклусивеакцесс свойство Virtual PC, интерфейс Ивмкэйбоард
- Ивмкэйбоард интерфейс Virtual PC, свойство Хасексклусивеакцесс
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137231"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a><span data-ttu-id="f13f0-106">Свойство Ивмкэйбоард:: Хасексклусивеакцесс</span><span class="sxs-lookup"><span data-stu-id="f13f0-106">IVMKeyboard::HasExclusiveAccess property</span></span>

<span data-ttu-id="f13f0-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f13f0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f13f0-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f13f0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f13f0-109">Указывает, имеет ли этот объект исключительный контроль над устройством клавиатуры виртуальной машины (ВМ).</span><span class="sxs-lookup"><span data-stu-id="f13f0-109">Indicates whether this object has exclusive control over the virtual machine's (VM) keyboard device.</span></span>

<span data-ttu-id="f13f0-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f13f0-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f13f0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f13f0-111">Syntax</span></span>


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a><span data-ttu-id="f13f0-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f13f0-112">Property value</span></span>

<span data-ttu-id="f13f0-113">**Значение true** , если получен монопольный доступ к устройству клавиатуры виртуальной машины; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="f13f0-113">**TRUE** if exclusive access to the VM's keyboard device has been acquired, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f13f0-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f13f0-114">Error codes</span></span>



| <span data-ttu-id="f13f0-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="f13f0-115">Name/value</span></span>                                                                                                                                                                   | <span data-ttu-id="f13f0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f13f0-116">Meaning</span></span>                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f13f0-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f13f0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                      | <span data-ttu-id="f13f0-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f13f0-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="f13f0-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="f13f0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                        | <span data-ttu-id="f13f0-120">Параметр *Exclusive* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f13f0-120">The *isExclusive* parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="f13f0-121"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f13f0-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                   | <span data-ttu-id="f13f0-122">Запрошенный монопольный режим уже задан для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="f13f0-122">The requested exclusive mode is already set for this device.</span></span> <span data-ttu-id="f13f0-123">Это может произойти при попытке установить монопольный режим, когда он уже был получен, или при попытке освободить монопольный режим, если он не был ранее получен.</span><span class="sxs-lookup"><span data-stu-id="f13f0-123">This can happen when trying to set exclusive mode when it has already been acquired, or when trying to release exclusive mode when it had not been previously acquired.</span></span><br/> |
| <dl> <span data-ttu-id="f13f0-124"><dt>Виртуальная машина \_ E \_ установить \_ монопольный \_ режим \_ не</dt> <dt>0xA0040825</dt></span><span class="sxs-lookup"><span data-stu-id="f13f0-124"><dt>VM\_E\_SET\_EXCLUSIVE\_MODE\_FAIL</dt> <dt>0xA0040825</dt></span></span> </dl> | <span data-ttu-id="f13f0-125">Не удалось задать или освободить монопольный режим по запросу.</span><span class="sxs-lookup"><span data-stu-id="f13f0-125">Failed to set or release exclusive mode as requested.</span></span> <span data-ttu-id="f13f0-126">Это может быть вызвано тем, что виртуальная машина больше не работает, или поскольку другой процесс уже получил монопольный режим на клавиатуре виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f13f0-126">This could be because the VM is no longer running, or because another process has already acquired exclusive mode on the VM's keyboard device.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f13f0-127"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f13f0-127"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                     | <span data-ttu-id="f13f0-128">Указанная строка пуста или содержит недопустимый код ключа.</span><span class="sxs-lookup"><span data-stu-id="f13f0-128">The specified string is empty, or contains an invalid key code.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="f13f0-129"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f13f0-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                | <span data-ttu-id="f13f0-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f13f0-130">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="f13f0-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f13f0-131">Requirements</span></span>



| <span data-ttu-id="f13f0-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f13f0-132">Requirement</span></span> | <span data-ttu-id="f13f0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f13f0-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f13f0-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f13f0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f13f0-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f13f0-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f13f0-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f13f0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f13f0-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f13f0-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f13f0-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f13f0-138">End of client support</span></span><br/>    | <span data-ttu-id="f13f0-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f13f0-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f13f0-140">Продукт</span><span class="sxs-lookup"><span data-stu-id="f13f0-140">Product</span></span><br/>                  | <span data-ttu-id="f13f0-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f13f0-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f13f0-142">Header</span><span class="sxs-lookup"><span data-stu-id="f13f0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f13f0-143"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f13f0-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f13f0-144">IID</span><span class="sxs-lookup"><span data-stu-id="f13f0-144">IID</span></span><br/>                      | <span data-ttu-id="f13f0-145">IID \_ ивмкэйбоард определен как 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="f13f0-145">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f13f0-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f13f0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f13f0-147">**ивмкэйбоард**</span><span class="sxs-lookup"><span data-stu-id="f13f0-147">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

