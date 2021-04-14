---
title: Свойство Каншутдовн Ивмгуестос (Впккоминтерфацес. h)
description: Указывает, можно ли аккуратно завершить работу гостевой операционной системы.
ms.assetid: 239cba43-9494-4efd-a4c8-0bb47f476b81
keywords:
- Каншутдовн свойство Virtual PC
- Каншутдовн свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Каншутдовн
topic_type:
- apiref
api_name:
- IVMGuestOS.CanShutdown
- IVMGuestOS.get_CanShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f76e652b7a172da6f5a438f72b09443a13dcce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341245"
---
# <a name="ivmguestoscanshutdown-property"></a><span data-ttu-id="72cc2-106">Свойство Ивмгуестос:: Каншутдовн</span><span class="sxs-lookup"><span data-stu-id="72cc2-106">IVMGuestOS::CanShutdown property</span></span>

<span data-ttu-id="72cc2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="72cc2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="72cc2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="72cc2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="72cc2-109">Указывает, может ли гостевая операционная система завершать работу (требуются компоненты интеграции).</span><span class="sxs-lookup"><span data-stu-id="72cc2-109">Indicates whether the guest operating system can be cleanly shut down (requires Integration Components).</span></span>

<span data-ttu-id="72cc2-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="72cc2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="72cc2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72cc2-111">Syntax</span></span>


```C++
HRESULT get_CanShutdown(
  [out, retval] VARIANT_BOOL *canShutdown
);
```



## <a name="property-value"></a><span data-ttu-id="72cc2-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="72cc2-112">Property value</span></span>

<span data-ttu-id="72cc2-113">**Вариант \_ Значение TRUE** , если операционная система поддерживает операцию завершения работы и **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="72cc2-113">**VARIANT\_TRUE** if the operating system supports the shutdown operation and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="72cc2-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="72cc2-114">Error codes</span></span>



| <span data-ttu-id="72cc2-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="72cc2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="72cc2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="72cc2-116">Meaning</span></span>                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="72cc2-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="72cc2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="72cc2-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="72cc2-118">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="72cc2-119"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="72cc2-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="72cc2-120">Виртуальная машина не включена.</span><span class="sxs-lookup"><span data-stu-id="72cc2-120">The virtual machine is not turned on.</span></span><br/>   |
| <dl> <span data-ttu-id="72cc2-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="72cc2-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="72cc2-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="72cc2-122">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="72cc2-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="72cc2-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="72cc2-124">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="72cc2-124">The virtual machine could not be found.</span></span><br/> |
| <dl> <span data-ttu-id="72cc2-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="72cc2-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="72cc2-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="72cc2-126">An unexpected error has occurred.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="72cc2-127">Требования</span><span class="sxs-lookup"><span data-stu-id="72cc2-127">Requirements</span></span>



| <span data-ttu-id="72cc2-128">Требование</span><span class="sxs-lookup"><span data-stu-id="72cc2-128">Requirement</span></span> | <span data-ttu-id="72cc2-129">Значение</span><span class="sxs-lookup"><span data-stu-id="72cc2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="72cc2-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72cc2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="72cc2-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="72cc2-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72cc2-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72cc2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="72cc2-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="72cc2-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="72cc2-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="72cc2-134">End of client support</span></span><br/>    | <span data-ttu-id="72cc2-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="72cc2-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="72cc2-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="72cc2-136">Product</span></span><br/>                  | <span data-ttu-id="72cc2-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="72cc2-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="72cc2-138">Header</span><span class="sxs-lookup"><span data-stu-id="72cc2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="72cc2-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="72cc2-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="72cc2-140">IID</span><span class="sxs-lookup"><span data-stu-id="72cc2-140">IID</span></span><br/>                      | <span data-ttu-id="72cc2-141">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="72cc2-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="72cc2-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72cc2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72cc2-143">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="72cc2-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

