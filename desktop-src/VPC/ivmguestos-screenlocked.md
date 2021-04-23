---
title: Свойство Скринлоккед Ивмгуестос (Впккоминтерфацес. h)
description: Указывает, заблокирован ли экран в операционной системе на виртуальной машине.
ms.assetid: 5ce2e0ad-b98c-4aa7-99b5-0fc85026a121
keywords:
- Скринлоккед свойство Virtual PC
- Скринлоккед свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Скринлоккед
topic_type:
- apiref
api_name:
- IVMGuestOS.ScreenLocked
- IVMGuestOS.get_ScreenLocked
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1f14bf0a61f06e9f36b44d02881cf7edc1f793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071724"
---
# <a name="ivmguestosscreenlocked-property"></a><span data-ttu-id="7cdf4-106">Свойство Ивмгуестос:: Скринлоккед</span><span class="sxs-lookup"><span data-stu-id="7cdf4-106">IVMGuestOS::ScreenLocked property</span></span>

<span data-ttu-id="7cdf4-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7cdf4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7cdf4-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7cdf4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7cdf4-109">Указывает, заблокирован ли экран в операционной системе на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7cdf4-109">Indicates whether the screen in the guest operating system is locked.</span></span>

<span data-ttu-id="7cdf4-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7cdf4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cdf4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cdf4-111">Syntax</span></span>


```C++
HRESULT get_ScreenLocked(
  [out, retval] VARIANT_BOOL *guestScreenLocked
);
```



## <a name="property-value"></a><span data-ttu-id="7cdf4-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7cdf4-112">Property value</span></span>

<span data-ttu-id="7cdf4-113">**Вариант \_ TRUE** , если экран заблокирован в гостевой операционной системе, в противном случае — значение **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="7cdf4-113">**VARIANT\_TRUE** if screen is locked in guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7cdf4-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7cdf4-114">Error codes</span></span>



| <span data-ttu-id="7cdf4-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="7cdf4-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="7cdf4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7cdf4-116">Meaning</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7cdf4-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7cdf4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="7cdf4-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7cdf4-118">The operation was successful.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="7cdf4-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="7cdf4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="7cdf4-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7cdf4-120">The parameter is **NULL**.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="7cdf4-121"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="7cdf4-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="7cdf4-122">Для этой операции должна быть запущена виртуальная машина (ВМ).</span><span class="sxs-lookup"><span data-stu-id="7cdf4-122">The virtual machine (VM) must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="7cdf4-123"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="7cdf4-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="7cdf4-124">Компонент интеграции не включен в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="7cdf4-124">The integration components feature is not enabled in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="7cdf4-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7cdf4-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="7cdf4-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7cdf4-126">An unexpected error has occurred.</span></span><br/>                                                |



## <a name="requirements"></a><span data-ttu-id="7cdf4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7cdf4-127">Requirements</span></span>



| <span data-ttu-id="7cdf4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7cdf4-128">Requirement</span></span> | <span data-ttu-id="7cdf4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7cdf4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdf4-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7cdf4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7cdf4-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7cdf4-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7cdf4-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7cdf4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7cdf4-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7cdf4-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7cdf4-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7cdf4-134">End of client support</span></span><br/>    | <span data-ttu-id="7cdf4-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7cdf4-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7cdf4-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="7cdf4-136">Product</span></span><br/>                  | <span data-ttu-id="7cdf4-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7cdf4-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7cdf4-138">Header</span><span class="sxs-lookup"><span data-stu-id="7cdf4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cdf4-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cdf4-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7cdf4-140">IID</span><span class="sxs-lookup"><span data-stu-id="7cdf4-140">IID</span></span><br/>                      | <span data-ttu-id="7cdf4-141">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="7cdf4-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="7cdf4-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cdf4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cdf4-143">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="7cdf4-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

