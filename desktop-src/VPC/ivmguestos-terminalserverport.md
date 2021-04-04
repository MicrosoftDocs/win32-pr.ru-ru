---
title: Ивмгуестос Терминалсерверпорт, свойство
description: Порт, используемый службы удаленных рабочих столов в гостевой операционной системе.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- Терминалсерверпорт свойство Virtual PC
- Терминалсерверпорт свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Терминалсерверпорт
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137323"
---
# <a name="ivmguestosterminalserverport-property"></a><span data-ttu-id="0d5a7-106">Свойство Ивмгуестос:: Терминалсерверпорт</span><span class="sxs-lookup"><span data-stu-id="0d5a7-106">IVMGuestOS::TerminalServerPort property</span></span>

<span data-ttu-id="0d5a7-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0d5a7-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0d5a7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0d5a7-109">Порт, используемый службы удаленных рабочих столов (ранее назывался службами терминалов) в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-109">Port used by Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="0d5a7-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d5a7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d5a7-111">Syntax</span></span>


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a><span data-ttu-id="0d5a7-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0d5a7-112">Property value</span></span>

<span data-ttu-id="0d5a7-113">Возвращает порт, используемый службы удаленных рабочих столов в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-113">Returns the port used by Remote Desktop Services in the guest operating system.</span></span>



| <span data-ttu-id="0d5a7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0d5a7-114">Value</span></span>                                                                              | <span data-ttu-id="0d5a7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0d5a7-115">Meaning</span></span>                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="0d5a7-116"><dt>3389</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a7-116"><dt>3389</dt></span></span> </dl>    | <span data-ttu-id="0d5a7-117">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0d5a7-117">Default value</span></span><br/>                      |
| <dl> <span data-ttu-id="0d5a7-118"><dt>1 65535</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a7-118"><dt>1 65535</dt></span></span> </dl> | <span data-ttu-id="0d5a7-119">Допустимый диапазон</span><span class="sxs-lookup"><span data-stu-id="0d5a7-119">Valid range</span></span><br/>                        |
| <dl> <span data-ttu-id="0d5a7-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a7-120"><dt>0</dt></span></span> </dl>       | <span data-ttu-id="0d5a7-121">Допустимое значение порта недоступно.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-121">Valid port value is not available.</span></span><br/> |



 

## <a name="error-codes"></a><span data-ttu-id="0d5a7-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="0d5a7-122">Error codes</span></span>



| <span data-ttu-id="0d5a7-123">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="0d5a7-123">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="0d5a7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0d5a7-124">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d5a7-125"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a7-125"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="0d5a7-126">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-126">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="0d5a7-127"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a7-127"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="0d5a7-128">Службы удаленных рабочих столов еще не инициализирован в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-128">Remote Desktop Services is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="0d5a7-129"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="0d5a7-129"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="0d5a7-130">Параметр *тспорт* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-130">The *tsPort* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="0d5a7-131"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a7-131"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="0d5a7-132">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-132">The virtual machine is not running.</span></span><br/>                                           |
| <dl> <span data-ttu-id="0d5a7-133"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a7-133"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="0d5a7-134">Компоненты интеграции не установлены на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-134">Integration components are not installed in this virtual machine.</span></span><br/>             |
| <dl> <span data-ttu-id="0d5a7-135"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a7-135"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="0d5a7-136">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-136">An unexpected error has occurred.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="0d5a7-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d5a7-137">Remarks</span></span>

<span data-ttu-id="0d5a7-138">Значение этого свойства является недопустимым, если свойство [**терминалсервицесинитиализед**](ivmguestos-terminalservicesinitialized.md) не имеет значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-138">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="0d5a7-139">Если свойство [**терминалсервицесинитиализед**](ivmguestos-terminalservicesinitialized.md) имеет значение **Variant \_ false** из-за ошибки соединения в порте, то значение, возвращаемое свойством **терминалсерверпорт** , содержит ошибку.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-139">If the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_FALSE** due to a connection error on the port, then the value returned by the **TerminalServerPort** property contains the error value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d5a7-140">Требования</span><span class="sxs-lookup"><span data-stu-id="0d5a7-140">Requirements</span></span>



| <span data-ttu-id="0d5a7-141">Требование</span><span class="sxs-lookup"><span data-stu-id="0d5a7-141">Requirement</span></span> | <span data-ttu-id="0d5a7-142">Значение</span><span class="sxs-lookup"><span data-stu-id="0d5a7-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5a7-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d5a7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0d5a7-144">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0d5a7-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0d5a7-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d5a7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0d5a7-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0d5a7-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="0d5a7-147">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0d5a7-147">End of client support</span></span><br/>    | <span data-ttu-id="0d5a7-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d5a7-148">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="0d5a7-149">IDL</span><span class="sxs-lookup"><span data-stu-id="0d5a7-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d5a7-150"><dt>Ивмгуестос. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a7-150"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="0d5a7-151">IID</span><span class="sxs-lookup"><span data-stu-id="0d5a7-151">IID</span></span><br/>                      | <span data-ttu-id="0d5a7-152">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="0d5a7-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="0d5a7-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d5a7-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5a7-154">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="0d5a7-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

