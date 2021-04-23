---
title: Свойство Терминалсервицесинитиализед Ивмгуестос (Впккоминтерфацес. h)
description: Состояние службы удаленных рабочих столов в гостевой операционной системе.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- Терминалсервицесинитиализед свойство Virtual PC
- Терминалсервицесинитиализед свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Терминалсервицесинитиализед
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92ce23b4b07f3e2d06f605f4598c8b31e4c70692
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535303"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a><span data-ttu-id="8e237-106">Свойство Ивмгуестос:: Терминалсервицесинитиализед</span><span class="sxs-lookup"><span data-stu-id="8e237-106">IVMGuestOS::TerminalServicesInitialized property</span></span>

<span data-ttu-id="8e237-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8e237-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e237-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e237-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e237-109">Получает состояние службы удаленных рабочих столов (прежнее название — службы терминалов) в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="8e237-109">Retrieves the status of Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="8e237-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8e237-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e237-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e237-111">Syntax</span></span>


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a><span data-ttu-id="8e237-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8e237-112">Property value</span></span>

<span data-ttu-id="8e237-113">Состояние инициализации.</span><span class="sxs-lookup"><span data-stu-id="8e237-113">The initialization status.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8e237-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8e237-114">Error codes</span></span>



| <span data-ttu-id="8e237-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="8e237-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="8e237-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8e237-116">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e237-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e237-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="8e237-118">Операция выполнена успешно, службы удаленных рабочих столов была инициализирована.</span><span class="sxs-lookup"><span data-stu-id="8e237-118">The operation was successful and Remote Desktop Services has been initialized.</span></span> <span data-ttu-id="8e237-119">Возвращаемое значение свойства указывает, доступна ли службы удаленных рабочих столов в операционной системе на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8e237-119">The returned property value indicates whether Remote Desktop Services is available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="8e237-120"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8e237-120"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="8e237-121">Компонент интеграции работает, но службы удаленных рабочих столов еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="8e237-121">The integration components feature is running, but Remote Desktop Services is not yet initialized.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8e237-122"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="8e237-122"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="8e237-123">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8e237-123">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="8e237-124"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="8e237-124"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="8e237-125">Для этой операции должна быть запущена виртуальная машина (ВМ).</span><span class="sxs-lookup"><span data-stu-id="8e237-125">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="8e237-126"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="8e237-126"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="8e237-127">Компонент интеграции не работает в операционной системе на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8e237-127">The integration components feature is not running in the guest operating system.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="8e237-128"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8e237-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="8e237-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8e237-129">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="8e237-130">Требования</span><span class="sxs-lookup"><span data-stu-id="8e237-130">Requirements</span></span>



| <span data-ttu-id="8e237-131">Требование</span><span class="sxs-lookup"><span data-stu-id="8e237-131">Requirement</span></span> | <span data-ttu-id="8e237-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8e237-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e237-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e237-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8e237-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e237-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e237-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e237-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8e237-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8e237-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8e237-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8e237-137">End of client support</span></span><br/>    | <span data-ttu-id="8e237-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e237-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8e237-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="8e237-139">Product</span></span><br/>                  | <span data-ttu-id="8e237-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e237-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8e237-141">Header</span><span class="sxs-lookup"><span data-stu-id="8e237-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e237-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e237-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8e237-143">IID</span><span class="sxs-lookup"><span data-stu-id="8e237-143">IID</span></span><br/>                      | <span data-ttu-id="8e237-144">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="8e237-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8e237-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e237-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e237-146">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="8e237-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

