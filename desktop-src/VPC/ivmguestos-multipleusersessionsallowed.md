---
title: Ивмгуестос Мултиплеусерсессионсалловед, свойство
description: Определяет, разрешено ли в гостевой операционной системе несколько одновременных сеансов пользователей.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- Мултиплеусерсессионсалловед свойство Virtual PC
- Мултиплеусерсессионсалловед свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Мултиплеусерсессионсалловед
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136091"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a><span data-ttu-id="5c9e6-106">Свойство Ивмгуестос:: Мултиплеусерсессионсалловед</span><span class="sxs-lookup"><span data-stu-id="5c9e6-106">IVMGuestOS::MultipleUserSessionsAllowed property</span></span>

<span data-ttu-id="5c9e6-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5c9e6-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5c9e6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5c9e6-109">Определяет, разрешено ли в гостевой операционной системе несколько одновременных сеансов пользователей.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-109">Determines whether multiple simultaneous user sessions are allowed in the guest operating system.</span></span>

<span data-ttu-id="5c9e6-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c9e6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c9e6-111">Syntax</span></span>


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a><span data-ttu-id="5c9e6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5c9e6-112">Property value</span></span>

<span data-ttu-id="5c9e6-113">**Вариант \_ Значение TRUE** , если в гостевой операционной системе разрешено несколько одновременных сеансов пользователей; в противном случае — **\_ значение false** .</span><span class="sxs-lookup"><span data-stu-id="5c9e6-113">**VARIANT\_TRUE** if multiple simultaneous user sessions are allowed in the guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c9e6-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5c9e6-114">Error codes</span></span>



| <span data-ttu-id="5c9e6-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="5c9e6-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="5c9e6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5c9e6-116">Meaning</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c9e6-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5c9e6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="5c9e6-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-118">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="5c9e6-119"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5c9e6-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="5c9e6-120">Службы удаленных рабочих столов (ранее назывались службами терминалов) еще не инициализирован в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-120">Remote Desktop Services (formerly known as Terminal Services) is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="5c9e6-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="5c9e6-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="5c9e6-122">Параметр *сессионстатус* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-122">The *sessionStatus* parameter is **NULL**.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="5c9e6-123"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="5c9e6-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="5c9e6-124">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-124">The virtual machine is not running.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="5c9e6-125"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="5c9e6-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="5c9e6-126">Компоненты интеграции не установлены на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-126">Integration components are not installed in this virtual machine.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="5c9e6-127"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5c9e6-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="5c9e6-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-128">An unexpected error has occurred.</span></span><br/>                                                                                   |



## <a name="remarks"></a><span data-ttu-id="5c9e6-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c9e6-129">Remarks</span></span>

<span data-ttu-id="5c9e6-130">Значение этого свойства является недопустимым, если свойство [**терминалсервицесинитиализед**](ivmguestos-terminalservicesinitialized.md) не имеет значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-130">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="5c9e6-131">Для клиентских операционных систем Windows **мултиплеусерсессионсалловед** является **вариантом \_ true** , если поддерживается быстрое переключение пользователей.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-131">For Windows client operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Fast User Switching is supported.</span></span> <span data-ttu-id="5c9e6-132">Для операционных систем Windows Server **мултиплеусерсессионсалловед** имеет значение **\_ true** , если службы удаленных рабочих столов (ранее именуемые службами терминалов) установлен и включен.</span><span class="sxs-lookup"><span data-stu-id="5c9e6-132">For Windows Server operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Remote Desktop Services (formerly called Terminal Services) is installed and enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c9e6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="5c9e6-133">Requirements</span></span>



| <span data-ttu-id="5c9e6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="5c9e6-134">Requirement</span></span> | <span data-ttu-id="5c9e6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="5c9e6-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9e6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c9e6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5c9e6-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5c9e6-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c9e6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c9e6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5c9e6-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5c9e6-139">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5c9e6-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5c9e6-140">End of client support</span></span><br/>    | <span data-ttu-id="5c9e6-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c9e6-141">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="5c9e6-142">IDL</span><span class="sxs-lookup"><span data-stu-id="5c9e6-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c9e6-143"><dt>Ивмгуестос. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c9e6-143"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="5c9e6-144">IID</span><span class="sxs-lookup"><span data-stu-id="5c9e6-144">IID</span></span><br/>                      | <span data-ttu-id="5c9e6-145">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="5c9e6-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5c9e6-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c9e6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9e6-147">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="5c9e6-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

