---
title: Метод Ивмгуестос Инсталлинтегратионкомпонентс (Впккоминтерфацес. h)
description: Находит и устанавливает последние компоненты интеграции в операционную систему на виртуальной машине.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- Метод Инсталлинтегратионкомпонентс Virtual PC
- Метод Инсталлинтегратионкомпонентс Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, метод Инсталлинтегратионкомпонентс
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879ded1464ebd310e1d1da4e3a952dc086600350
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414821"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a><span data-ttu-id="4c11c-106">Метод Ивмгуестос:: Инсталлинтегратионкомпонентс</span><span class="sxs-lookup"><span data-stu-id="4c11c-106">IVMGuestOS::InstallIntegrationComponents method</span></span>

<span data-ttu-id="4c11c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4c11c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4c11c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4c11c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4c11c-109">Находит и устанавливает последние компоненты интеграции в операционную систему на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4c11c-109">Locates and installs the latest Integration Components into the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c11c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c11c-110">Syntax</span></span>


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a><span data-ttu-id="4c11c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c11c-111">Parameters</span></span>

<span data-ttu-id="4c11c-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4c11c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c11c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c11c-113">Return value</span></span>

<span data-ttu-id="4c11c-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="4c11c-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4c11c-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4c11c-115">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="4c11c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4c11c-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c11c-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4c11c-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="4c11c-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4c11c-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="4c11c-119"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4c11c-119"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                       | <span data-ttu-id="4c11c-120">Для этой операции должна быть запущена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="4c11c-120">The virtual machine must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="4c11c-121"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4c11c-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="4c11c-122">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="4c11c-122">The virtual machine could not be found.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4c11c-123"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="4c11c-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="4c11c-124">Виртуальная машина не имеет пустого DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="4c11c-124">The virtual machine does not have an empty DVD drive.</span></span><br/>                       |
| <dl> <span data-ttu-id="4c11c-125"><dt>**Виртуальная машина \_ \_ \_ \_ Ошибка отключения носителя**</dt> <dt>0xA0040508</dt></span><span class="sxs-lookup"><span data-stu-id="4c11c-125"><dt>**VM\_E\_MEDIA\_UNMOUNT\_FAIL**</dt> <dt>0xA0040508</dt></span></span> </dl>                   | <span data-ttu-id="4c11c-126">Сбой при попытке отключить носитель от DVD-дисковода виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4c11c-126">The attempt to unmount the media from the virtual machine DVD drive failed.</span></span><br/> |
| <dl> <span data-ttu-id="4c11c-127"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4c11c-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="4c11c-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4c11c-128">An unexpected error has occurred.</span></span><br/>                                           |
| <dl> <span data-ttu-id="4c11c-129"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="4c11c-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="4c11c-130">Системе не удается найти ISO-файл для компонентов интеграции.</span><span class="sxs-lookup"><span data-stu-id="4c11c-130">The system cannot find the ISO file for the Integration Components.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="4c11c-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4c11c-131">Requirements</span></span>



| <span data-ttu-id="4c11c-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4c11c-132">Requirement</span></span> | <span data-ttu-id="4c11c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4c11c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c11c-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c11c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4c11c-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4c11c-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c11c-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c11c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4c11c-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4c11c-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4c11c-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4c11c-138">End of client support</span></span><br/>    | <span data-ttu-id="4c11c-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c11c-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4c11c-140">Продукт</span><span class="sxs-lookup"><span data-stu-id="4c11c-140">Product</span></span><br/>                  | <span data-ttu-id="4c11c-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4c11c-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4c11c-142">Header</span><span class="sxs-lookup"><span data-stu-id="4c11c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c11c-143"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c11c-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4c11c-144">IID</span><span class="sxs-lookup"><span data-stu-id="4c11c-144">IID</span></span><br/>                      | <span data-ttu-id="4c11c-145">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="4c11c-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4c11c-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c11c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c11c-147">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="4c11c-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

