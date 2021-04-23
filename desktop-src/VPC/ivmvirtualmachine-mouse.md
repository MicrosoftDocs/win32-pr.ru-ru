---
title: Свойство мыши Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Извлекает устройство мыши для виртуальной машины.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Виртуальный ПК свойства мыши
- Свойство мыши Virtual PC, интерфейс Ивмвиртуалмачине
- Интерфейс Ивмвиртуалмачине Virtual PC, свойство Mouse
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111d511f4e7948a83a968b154721bf81dbfe53b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691942"
---
# <a name="ivmvirtualmachinemouse-property"></a><span data-ttu-id="5ac5c-106">Ивмвиртуалмачине:: Mouse, свойство</span><span class="sxs-lookup"><span data-stu-id="5ac5c-106">IVMVirtualMachine::Mouse property</span></span>

<span data-ttu-id="5ac5c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5ac5c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5ac5c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5ac5c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5ac5c-109">Извлекает устройство мыши для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ac5c-109">Retrieves the mouse device for the virtual machine.</span></span>

<span data-ttu-id="5ac5c-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5ac5c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac5c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ac5c-111">Syntax</span></span>


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a><span data-ttu-id="5ac5c-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5ac5c-112">Property value</span></span>

<span data-ttu-id="5ac5c-113">Объект [**ивммаусе**](ivmmouse.md) .</span><span class="sxs-lookup"><span data-stu-id="5ac5c-113">An [**IVMMouse**](ivmmouse.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5ac5c-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5ac5c-114">Error codes</span></span>



| <span data-ttu-id="5ac5c-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="5ac5c-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="5ac5c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5ac5c-116">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="5ac5c-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5ac5c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="5ac5c-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5ac5c-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="5ac5c-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="5ac5c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="5ac5c-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5ac5c-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="5ac5c-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5ac5c-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="5ac5c-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="5ac5c-122">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="5ac5c-123"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="5ac5c-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="5ac5c-124">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="5ac5c-124">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="5ac5c-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5ac5c-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="5ac5c-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5ac5c-126">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="5ac5c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5ac5c-127">Requirements</span></span>



| <span data-ttu-id="5ac5c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5ac5c-128">Requirement</span></span> | <span data-ttu-id="5ac5c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5ac5c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac5c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ac5c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac5c-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5ac5c-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ac5c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ac5c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac5c-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5ac5c-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5ac5c-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5ac5c-134">End of client support</span></span><br/>    | <span data-ttu-id="5ac5c-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ac5c-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5ac5c-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="5ac5c-136">Product</span></span><br/>                  | <span data-ttu-id="5ac5c-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5ac5c-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5ac5c-138">Header</span><span class="sxs-lookup"><span data-stu-id="5ac5c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac5c-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ac5c-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5ac5c-140">IID</span><span class="sxs-lookup"><span data-stu-id="5ac5c-140">IID</span></span><br/>                      | <span data-ttu-id="5ac5c-141">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="5ac5c-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5ac5c-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ac5c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac5c-143">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="5ac5c-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

