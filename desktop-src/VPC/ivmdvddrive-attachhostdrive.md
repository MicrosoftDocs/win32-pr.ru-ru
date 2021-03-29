---
title: Метод Ивмдвддриве Аттачхостдриве (Впккоминтерфацес. h)
description: Подключает диск узла к DVD-дисководу в виртуальной машине.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- Метод Аттачхостдриве Virtual PC
- Метод Аттачхостдриве Virtual PC, интерфейс Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, метод Аттачхостдриве
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012afcdc0b88aa5b77f1d85cc5becff1e70853f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650392"
---
# <a name="ivmdvddriveattachhostdrive-method"></a><span data-ttu-id="2996e-106">Метод Ивмдвддриве:: Аттачхостдриве</span><span class="sxs-lookup"><span data-stu-id="2996e-106">IVMDVDDrive::AttachHostDrive method</span></span>

<span data-ttu-id="2996e-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2996e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2996e-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2996e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2996e-109">Подключает диск узла к DVD-дисководу в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2996e-109">Attaches a host drive to the DVD drive within the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2996e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2996e-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="2996e-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2996e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2996e-112">*буква_диска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2996e-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2996e-113">Буква диска узла, который должен быть присоединен.</span><span class="sxs-lookup"><span data-stu-id="2996e-113">The letter of the host drive that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2996e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2996e-114">Return value</span></span>

<span data-ttu-id="2996e-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2996e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2996e-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="2996e-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="2996e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2996e-117">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2996e-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2996e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="2996e-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2996e-119">The operation was successful.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="2996e-120"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2996e-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="2996e-121">Не указана буква диска, или указана недопустимая буква диска.</span><span class="sxs-lookup"><span data-stu-id="2996e-121">No drive letter was specified, or the specified drive letter is invalid.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="2996e-122"><dt>**Д \_ Сбой**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="2996e-122"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="2996e-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2996e-123">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="2996e-124"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2996e-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="2996e-125">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="2996e-125">The virtual machine could not be found.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="2996e-126"><dt>**Виртуальная машина \_ \_Диск E \_ \_ используется**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="2996e-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="2996e-127">Диск DVD или ISO-образ узла уже подключен к этому диску в виртуальной машине, или указанный диск узла уже используется в другой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2996e-127">A host DVD drive or ISO image is already attached to this drive within the virtual machine, or the specified host drive is already in use within another virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="2996e-128"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="2996e-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="2996e-129">Расположение шины для этого диска недопустимо, или диск не является допустимым DVD-дисководом.</span><span class="sxs-lookup"><span data-stu-id="2996e-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="2996e-130"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2996e-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="2996e-131">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2996e-131">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="2996e-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2996e-132">Requirements</span></span>



| <span data-ttu-id="2996e-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2996e-133">Requirement</span></span> | <span data-ttu-id="2996e-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2996e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2996e-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2996e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2996e-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2996e-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2996e-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2996e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2996e-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2996e-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2996e-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2996e-139">End of client support</span></span><br/>    | <span data-ttu-id="2996e-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2996e-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2996e-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="2996e-141">Product</span></span><br/>                  | <span data-ttu-id="2996e-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2996e-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2996e-143">Header</span><span class="sxs-lookup"><span data-stu-id="2996e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2996e-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2996e-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2996e-145">IID</span><span class="sxs-lookup"><span data-stu-id="2996e-145">IID</span></span><br/>                      | <span data-ttu-id="2996e-146">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="2996e-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="2996e-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2996e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2996e-148">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="2996e-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

