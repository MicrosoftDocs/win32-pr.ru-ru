---
title: Свойство Суитемаск Ивмгуестос (Впккоминтерфацес. h)
description: Получает Суитемаск гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Суитемаск свойство Virtual PC
- Суитемаск свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Суитемаск
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803844"
---
# <a name="ivmguestossuitemask-property"></a><span data-ttu-id="aa97b-106">Свойство Ивмгуестос:: Суитемаск</span><span class="sxs-lookup"><span data-stu-id="aa97b-106">IVMGuestOS::SuiteMask property</span></span>

<span data-ttu-id="aa97b-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa97b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="aa97b-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="aa97b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="aa97b-109">Получает Суитемаск гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="aa97b-109">Retrieves the SuiteMask of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="aa97b-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="aa97b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa97b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa97b-111">Syntax</span></span>


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a><span data-ttu-id="aa97b-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="aa97b-112">Property value</span></span>

<span data-ttu-id="aa97b-113">Маска набора.</span><span class="sxs-lookup"><span data-stu-id="aa97b-113">The suite mask.</span></span> <span data-ttu-id="aa97b-114">Поддерживаются следующие строковые значения.</span><span class="sxs-lookup"><span data-stu-id="aa97b-114">The following string values are supported.</span></span>



| <span data-ttu-id="aa97b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="aa97b-115">Value</span></span>                                                                                   | <span data-ttu-id="aa97b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aa97b-116">Meaning</span></span>                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa97b-117"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-117"><dt>"0x00000004"</dt></span></span> </dl> | <span data-ttu-id="aa97b-118">Компоненты Microsoft BackOffice установлены.</span><span class="sxs-lookup"><span data-stu-id="aa97b-118">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="aa97b-119"><dt>"0x00000400"</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-119"><dt>"0x00000400"</dt></span></span> </dl> | <span data-ttu-id="aa97b-120">Установлен выпуск Windows Server 2003, Web Edition.</span><span class="sxs-lookup"><span data-stu-id="aa97b-120">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="aa97b-121"><dt>"0x00004000"</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-121"><dt>"0x00004000"</dt></span></span> </dl> | <span data-ttu-id="aa97b-122">Windows Server 2003, выпуски Compute Cluster Edition установлены.</span><span class="sxs-lookup"><span data-stu-id="aa97b-122">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="aa97b-123"><dt>"0x00000080"</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-123"><dt>"0x00000080"</dt></span></span> </dl> | <span data-ttu-id="aa97b-124">Windows Server 2008 R2 Datacenter, установлен Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition или Windows 2000 Datacenter Server.</span><span class="sxs-lookup"><span data-stu-id="aa97b-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/> |
| <dl> <span data-ttu-id="aa97b-125"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-125"><dt>"0x00000002"</dt></span></span> </dl> | <span data-ttu-id="aa97b-126">Установлен Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition или Windows 2000 Advanced Server.</span><span class="sxs-lookup"><span data-stu-id="aa97b-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span><br/>   |
| <dl> <span data-ttu-id="aa97b-127"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-127"><dt>"0x00000040"</dt></span></span> </dl> | <span data-ttu-id="aa97b-128">Установлена операционная система Windows XP Embedded.</span><span class="sxs-lookup"><span data-stu-id="aa97b-128">Windows XP Embedded is installed.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="aa97b-129"><dt>"0x00000200"</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-129"><dt>"0x00000200"</dt></span></span> </dl> | <span data-ttu-id="aa97b-130">Установлена ОС Windows Vista Home Premium, Windows Vista Домашняя базовая или Windows XP Home Edition.</span><span class="sxs-lookup"><span data-stu-id="aa97b-130">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="aa97b-131"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-131"><dt>"0x00000100"</dt></span></span> </dl> | <span data-ttu-id="aa97b-132">Удаленный рабочий стол поддерживается, но поддерживается только один интерактивный сеанс.</span><span class="sxs-lookup"><span data-stu-id="aa97b-132">Remote Desktop is supported, but only one interactive session is supported.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="aa97b-133"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-133"><dt>"0x00000001"</dt></span></span> </dl> | <span data-ttu-id="aa97b-134">Microsoft Small Business Server был установлен в системе, но может быть обновлен до другой версии Windows.</span><span class="sxs-lookup"><span data-stu-id="aa97b-134">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span><br/>                                 |
| <dl> <span data-ttu-id="aa97b-135"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-135"><dt>"0x00000020"</dt></span></span> </dl> | <span data-ttu-id="aa97b-136">Microsoft Small Business Server устанавливается с лицензией на клиентскую лицензию принудительно.</span><span class="sxs-lookup"><span data-stu-id="aa97b-136">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="aa97b-137"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-137"><dt>"0x00002000"</dt></span></span> </dl> | <span data-ttu-id="aa97b-138">Установлен Windows Storage Server 2003 R2 или Windows Storage Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aa97b-138">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="aa97b-139"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-139"><dt>"0x00000010"</dt></span></span> </dl> | <span data-ttu-id="aa97b-140">Службы удаленных рабочих столов установлен.</span><span class="sxs-lookup"><span data-stu-id="aa97b-140">Remote Desktop Services is installed.</span></span> <span data-ttu-id="aa97b-141">Это значение всегда задано.</span><span class="sxs-lookup"><span data-stu-id="aa97b-141">This value is always set.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="aa97b-142"><dt>"0x00008000"</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-142"><dt>"0x00008000"</dt></span></span> </dl> | <span data-ttu-id="aa97b-143">Установлен Windows Home Server.</span><span class="sxs-lookup"><span data-stu-id="aa97b-143">Windows Home Server is installed.</span></span><br/>                                                                                                                           |



 

## <a name="error-codes"></a><span data-ttu-id="aa97b-144">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="aa97b-144">Error codes</span></span>



| <span data-ttu-id="aa97b-145">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="aa97b-145">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="aa97b-146">Значение</span><span class="sxs-lookup"><span data-stu-id="aa97b-146">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="aa97b-147"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-147"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="aa97b-148">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aa97b-148">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="aa97b-149"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="aa97b-149"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="aa97b-150">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="aa97b-150">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="aa97b-151"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-151"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="aa97b-152">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="aa97b-152">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="aa97b-153"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-153"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="aa97b-154">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="aa97b-154">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="aa97b-155"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-155"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="aa97b-156">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="aa97b-156">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="aa97b-157">Требования</span><span class="sxs-lookup"><span data-stu-id="aa97b-157">Requirements</span></span>



| <span data-ttu-id="aa97b-158">Требование</span><span class="sxs-lookup"><span data-stu-id="aa97b-158">Requirement</span></span> | <span data-ttu-id="aa97b-159">Значение</span><span class="sxs-lookup"><span data-stu-id="aa97b-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa97b-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa97b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="aa97b-161">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="aa97b-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa97b-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa97b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="aa97b-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="aa97b-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aa97b-164">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="aa97b-164">End of client support</span></span><br/>    | <span data-ttu-id="aa97b-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa97b-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="aa97b-166">Продукт</span><span class="sxs-lookup"><span data-stu-id="aa97b-166">Product</span></span><br/>                  | <span data-ttu-id="aa97b-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="aa97b-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="aa97b-168">Header</span><span class="sxs-lookup"><span data-stu-id="aa97b-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa97b-169"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa97b-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="aa97b-170">IID</span><span class="sxs-lookup"><span data-stu-id="aa97b-170">IID</span></span><br/>                      | <span data-ttu-id="aa97b-171">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="aa97b-171">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="aa97b-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa97b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa97b-173">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="aa97b-173">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

