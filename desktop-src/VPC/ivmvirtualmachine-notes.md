---
title: Свойство Ивмвиртуалмачине Notes (Впккоминтерфацес. h)
description: Примечания для виртуальной машины.
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Заметки свойство Virtual PC
- Заметки свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Notes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8fba8659a8f9546866129f21299e44006eb496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492573"
---
# <a name="ivmvirtualmachinenotes-property"></a><span data-ttu-id="4d821-106">Ивмвиртуалмачине:: Notes, свойство</span><span class="sxs-lookup"><span data-stu-id="4d821-106">IVMVirtualMachine::Notes property</span></span>

<span data-ttu-id="4d821-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4d821-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4d821-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4d821-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4d821-109">Извлекает и задает заметки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4d821-109">Retrieves and sets the notes for the virtual machine.</span></span>

<span data-ttu-id="4d821-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4d821-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d821-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d821-111">Syntax</span></span>


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a><span data-ttu-id="4d821-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4d821-112">Property value</span></span>

<span data-ttu-id="4d821-113">Указывает заметки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4d821-113">Specifies the notes for the virtual machine.</span></span> <span data-ttu-id="4d821-114">Максимальная длина строки — 65 536 символов.</span><span class="sxs-lookup"><span data-stu-id="4d821-114">The maximum length of the string is 65,536 characters.</span></span>

<span data-ttu-id="4d821-115">Чтобы удалить все заметки, передайте пустую строку.</span><span class="sxs-lookup"><span data-stu-id="4d821-115">To remove any notes, pass an empty string.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d821-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4d821-116">Error codes</span></span>



| <span data-ttu-id="4d821-117">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="4d821-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4d821-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4d821-118">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d821-119"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d821-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4d821-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4d821-120">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="4d821-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="4d821-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4d821-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4d821-122">The parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="4d821-123"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="4d821-123"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="4d821-124">Параметр недопустим или содержит более 65 536 символов.</span><span class="sxs-lookup"><span data-stu-id="4d821-124">The parameter is not valid or contains more than 65,536 characters.</span></span><br/> |
| <dl> <span data-ttu-id="4d821-125"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4d821-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="4d821-126">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="4d821-126">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="4d821-127"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4d821-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4d821-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4d821-128">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="4d821-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4d821-129">Requirements</span></span>



| <span data-ttu-id="4d821-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4d821-130">Requirement</span></span> | <span data-ttu-id="4d821-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4d821-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d821-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d821-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4d821-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4d821-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d821-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d821-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4d821-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4d821-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4d821-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4d821-136">End of client support</span></span><br/>    | <span data-ttu-id="4d821-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d821-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4d821-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="4d821-138">Product</span></span><br/>                  | <span data-ttu-id="4d821-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4d821-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4d821-140">Header</span><span class="sxs-lookup"><span data-stu-id="4d821-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d821-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d821-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4d821-142">IID</span><span class="sxs-lookup"><span data-stu-id="4d821-142">IID</span></span><br/>                      | <span data-ttu-id="4d821-143">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4d821-143">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4d821-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d821-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d821-145">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="4d821-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

