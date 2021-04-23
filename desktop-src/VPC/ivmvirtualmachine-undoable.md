---
title: Свойство, Ивмвиртуалмачине отменяемым (Впккоминтерфацес. h)
description: Определяет, включены ли диски отмены для жестких дисков, подключенных к виртуальной машине.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- Необратимое свойство Virtual PC
- Свойство, которое вы отменяеми Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, обратимое свойство
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cbc77f4d68fbdbfcc8d3998e3c207b8f4245c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534241"
---
# <a name="ivmvirtualmachineundoable-property"></a><span data-ttu-id="f9fc5-106">Свойство Ивмвиртуалмачине:: Undoed</span><span class="sxs-lookup"><span data-stu-id="f9fc5-106">IVMVirtualMachine::Undoable property</span></span>

<span data-ttu-id="f9fc5-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f9fc5-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f9fc5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f9fc5-109">Определяет, включены ли диски отмены для жестких дисков, подключенных к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-109">Determines whether undo drives are enabled for hard disks connected to the virtual machine (VM).</span></span>

<span data-ttu-id="f9fc5-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fc5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9fc5-111">Syntax</span></span>


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a><span data-ttu-id="f9fc5-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f9fc5-112">Property value</span></span>

<span data-ttu-id="f9fc5-113">Указывает **вариант \_ true** , если диски отмены включены для жестких дисков, ПОДКЛЮЧЕННЫХ к виртуальной машине, и **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-113">Specifies **VARIANT\_TRUE** if undo drives are enabled for hard disks connected to the VM and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9fc5-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f9fc5-114">Error codes</span></span>



| <span data-ttu-id="f9fc5-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="f9fc5-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="f9fc5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f9fc5-116">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f9fc5-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f9fc5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="f9fc5-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f9fc5-119"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f9fc5-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="f9fc5-120">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-120">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="f9fc5-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="f9fc5-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="f9fc5-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f9fc5-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f9fc5-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="f9fc5-124">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="f9fc5-125"><dt>Виртуальная машина \_ \_Преф \_ Виртуальная машина E \_ Active</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="f9fc5-125"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="f9fc5-126">Виртуальная машина запущена или сохранена.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-126">The VM is running or saved.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="f9fc5-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9fc5-127">Remarks</span></span>

<span data-ttu-id="f9fc5-128">Если отключены диски отмены, все существующие файлы диска отмены будут удалены.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-128">If undo drives are disabled, any existing undo drive files will be deleted.</span></span>

<span data-ttu-id="f9fc5-129">Это свойство нельзя задать, если виртуальная машина запущена или сохранена.</span><span class="sxs-lookup"><span data-stu-id="f9fc5-129">You cannot set this property if the VM is running or saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9fc5-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f9fc5-130">Requirements</span></span>



| <span data-ttu-id="f9fc5-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f9fc5-131">Requirement</span></span> | <span data-ttu-id="f9fc5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f9fc5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9fc5-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9fc5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f9fc5-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f9fc5-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9fc5-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9fc5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f9fc5-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f9fc5-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f9fc5-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f9fc5-137">End of client support</span></span><br/>    | <span data-ttu-id="f9fc5-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9fc5-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f9fc5-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="f9fc5-139">Product</span></span><br/>                  | <span data-ttu-id="f9fc5-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f9fc5-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f9fc5-141">Header</span><span class="sxs-lookup"><span data-stu-id="f9fc5-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9fc5-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9fc5-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f9fc5-143">IID</span><span class="sxs-lookup"><span data-stu-id="f9fc5-143">IID</span></span><br/>                      | <span data-ttu-id="f9fc5-144">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="f9fc5-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f9fc5-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9fc5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fc5-146">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="f9fc5-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

