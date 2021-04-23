---
title: Свойство Ивмгуестос ComputerName (Впккоминтерфацес. h)
description: Имя компьютера гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: b35fa1a1-e105-43e6-9a2f-a5c7e71772cf
keywords:
- Свойство ComputerName Virtual PC
- Свойство ComputerName Virtual PC, интерфейс Ивмгуестос
- Интерфейс Ивмгуестос Virtual PC, свойство ComputerName
topic_type:
- apiref
api_name:
- IVMGuestOS.ComputerName
- IVMGuestOS.get_ComputerName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b266c238809284b340095dd25390d6e5f3d2b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492897"
---
# <a name="ivmguestoscomputername-property"></a><span data-ttu-id="6a19e-106">Свойство Ивмгуестос:: ComputerName</span><span class="sxs-lookup"><span data-stu-id="6a19e-106">IVMGuestOS::ComputerName property</span></span>

<span data-ttu-id="6a19e-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6a19e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6a19e-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6a19e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6a19e-109">Возвращает имя компьютера гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6a19e-109">Retrieves the computer name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="6a19e-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6a19e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a19e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a19e-111">Syntax</span></span>


```C++
HRESULT get_ComputerName(
  [out, retval] BSTR *guestComputerName
);
```



## <a name="property-value"></a><span data-ttu-id="6a19e-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6a19e-112">Property value</span></span>

<span data-ttu-id="6a19e-113">Имя компьютера гостевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6a19e-113">The computer name of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6a19e-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6a19e-114">Error codes</span></span>



| <span data-ttu-id="6a19e-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="6a19e-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="6a19e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6a19e-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6a19e-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6a19e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="6a19e-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6a19e-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="6a19e-119"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6a19e-119"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="6a19e-120">Параметр является недопустимым или не указан.</span><span class="sxs-lookup"><span data-stu-id="6a19e-120">The parameter is not valid or not specified.</span></span><br/>         |
| <dl> <span data-ttu-id="6a19e-121"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="6a19e-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="6a19e-122">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="6a19e-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="6a19e-123"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="6a19e-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="6a19e-124">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6a19e-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="6a19e-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6a19e-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="6a19e-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6a19e-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="6a19e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6a19e-127">Requirements</span></span>



| <span data-ttu-id="6a19e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6a19e-128">Requirement</span></span> | <span data-ttu-id="6a19e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6a19e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a19e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a19e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6a19e-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6a19e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6a19e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a19e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6a19e-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6a19e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6a19e-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6a19e-134">End of client support</span></span><br/>    | <span data-ttu-id="6a19e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6a19e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6a19e-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="6a19e-136">Product</span></span><br/>                  | <span data-ttu-id="6a19e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6a19e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6a19e-138">Header</span><span class="sxs-lookup"><span data-stu-id="6a19e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a19e-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a19e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6a19e-140">IID</span><span class="sxs-lookup"><span data-stu-id="6a19e-140">IID</span></span><br/>                      | <span data-ttu-id="6a19e-141">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="6a19e-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6a19e-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a19e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a19e-143">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="6a19e-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

