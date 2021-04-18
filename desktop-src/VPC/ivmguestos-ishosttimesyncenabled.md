---
title: Свойство Ишосттимесинценаблед Ивмгуестос (Впккоминтерфацес. h)
description: Указывает, должны ли компоненты интеграции на этой виртуальной машине синхронизировать часы гостевой виртуальной машины с часами узла.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- Ишосттимесинценаблед свойство Virtual PC
- Ишосттимесинценаблед свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Ишосттимесинценаблед
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87afddb2e3bc940c5dba7e2548e4355d36142012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650374"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a><span data-ttu-id="49a69-106">Свойство Ивмгуестос:: Ишосттимесинценаблед</span><span class="sxs-lookup"><span data-stu-id="49a69-106">IVMGuestOS::IsHostTimeSyncEnabled property</span></span>

<span data-ttu-id="49a69-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="49a69-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="49a69-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="49a69-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="49a69-109">Указывает, должны ли компоненты интеграции в этой виртуальной машине синхронизировать часы гостевой виртуальной машины с часами узла.</span><span class="sxs-lookup"><span data-stu-id="49a69-109">Indicates whether the Integration Components in this virtual machine (VM) should synchronize the guest's clock with the host's clock.</span></span>

<span data-ttu-id="49a69-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="49a69-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a69-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49a69-111">Syntax</span></span>


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="49a69-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="49a69-112">Property value</span></span>

<span data-ttu-id="49a69-113">Используйте **вариант \_ true** , если компоненты интеграции в этой виртуальной машине должны синхронизировать часы гостевой виртуальной машины с часами узла и **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="49a69-113">Use **VARIANT\_TRUE** if the integration components in this VM should synchronize the guest's clock with the host's clock and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="49a69-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="49a69-114">Error codes</span></span>



| <span data-ttu-id="49a69-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="49a69-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="49a69-116">Значение</span><span class="sxs-lookup"><span data-stu-id="49a69-116">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="49a69-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="49a69-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="49a69-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="49a69-118">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="49a69-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="49a69-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="49a69-120">Параметр @ *Enable* не указан.</span><span class="sxs-lookup"><span data-stu-id="49a69-120">The *isEnabled* parameter is not specified.</span></span><br/> |
| <dl> <span data-ttu-id="49a69-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="49a69-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="49a69-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="49a69-122">The configuration is unknown.</span></span><br/>               |
| <dl> <span data-ttu-id="49a69-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="49a69-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="49a69-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="49a69-124">An unexpected error has occurred.</span></span><br/>           |



## <a name="remarks"></a><span data-ttu-id="49a69-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49a69-125">Remarks</span></span>

<span data-ttu-id="49a69-126">Этот параметр нельзя изменить, пока виртуальная машина активна (то есть запущена или находится в сохраненном состоянии).</span><span class="sxs-lookup"><span data-stu-id="49a69-126">You cannot change this setting while the virtual machine is active (that is, running or in saved state).</span></span>

## <a name="requirements"></a><span data-ttu-id="49a69-127">Требования</span><span class="sxs-lookup"><span data-stu-id="49a69-127">Requirements</span></span>



| <span data-ttu-id="49a69-128">Требование</span><span class="sxs-lookup"><span data-stu-id="49a69-128">Requirement</span></span> | <span data-ttu-id="49a69-129">Значение</span><span class="sxs-lookup"><span data-stu-id="49a69-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="49a69-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49a69-130">Minimum supported client</span></span><br/> | <span data-ttu-id="49a69-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="49a69-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49a69-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49a69-132">Minimum supported server</span></span><br/> | <span data-ttu-id="49a69-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="49a69-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="49a69-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="49a69-134">End of client support</span></span><br/>    | <span data-ttu-id="49a69-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="49a69-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="49a69-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="49a69-136">Product</span></span><br/>                  | <span data-ttu-id="49a69-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="49a69-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="49a69-138">Header</span><span class="sxs-lookup"><span data-stu-id="49a69-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="49a69-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="49a69-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="49a69-140">IID</span><span class="sxs-lookup"><span data-stu-id="49a69-140">IID</span></span><br/>                      | <span data-ttu-id="49a69-141">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="49a69-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="49a69-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49a69-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a69-143">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="49a69-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

