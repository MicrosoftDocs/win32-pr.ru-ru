---
title: Свойство клавиатуры Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Извлекает устройство клавиатуры для виртуальной машины.
ms.assetid: bf516d07-eea9-40e3-b0d3-0fd4d3a04eb1
keywords:
- Свойство клавиатуры Virtual PC
- Свойство клавиатуры Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство клавиатуры
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Keyboard
- IVMVirtualMachine.get_Keyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31080b376a9e0fa999d568e5f3c7524d597aa0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341070"
---
# <a name="ivmvirtualmachinekeyboard-property"></a><span data-ttu-id="b4e97-106">Ивмвиртуалмачине:: Keyboard, свойство</span><span class="sxs-lookup"><span data-stu-id="b4e97-106">IVMVirtualMachine::Keyboard property</span></span>

<span data-ttu-id="b4e97-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b4e97-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b4e97-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b4e97-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b4e97-109">Извлекает устройство клавиатуры для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b4e97-109">Retrieves the keyboard device for the virtual machine.</span></span>

<span data-ttu-id="b4e97-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b4e97-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e97-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4e97-111">Syntax</span></span>


```C++
HRESULT get_Keyboard(
  [out, retval] IVMKeyboard **keyboard
);
```



## <a name="property-value"></a><span data-ttu-id="b4e97-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b4e97-112">Property value</span></span>

<span data-ttu-id="b4e97-113">Объект [**ивмкэйбоард**](ivmkeyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e97-113">The [**IVMKeyboard**](ivmkeyboard.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b4e97-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b4e97-114">Error codes</span></span>



| <span data-ttu-id="b4e97-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="b4e97-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b4e97-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e97-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b4e97-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b4e97-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b4e97-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b4e97-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b4e97-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b4e97-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b4e97-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b4e97-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b4e97-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b4e97-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b4e97-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="b4e97-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="b4e97-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b4e97-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b4e97-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b4e97-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b4e97-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b4e97-125">Requirements</span></span>



| <span data-ttu-id="b4e97-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b4e97-126">Requirement</span></span> | <span data-ttu-id="b4e97-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e97-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e97-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4e97-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b4e97-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b4e97-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b4e97-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4e97-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b4e97-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b4e97-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b4e97-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b4e97-132">End of client support</span></span><br/>    | <span data-ttu-id="b4e97-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4e97-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b4e97-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="b4e97-134">Product</span></span><br/>                  | <span data-ttu-id="b4e97-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b4e97-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b4e97-136">Header</span><span class="sxs-lookup"><span data-stu-id="b4e97-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4e97-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4e97-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b4e97-138">IID</span><span class="sxs-lookup"><span data-stu-id="b4e97-138">IID</span></span><br/>                      | <span data-ttu-id="b4e97-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b4e97-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b4e97-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4e97-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e97-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="b4e97-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

