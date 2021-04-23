---
title: Метод Ивмдвддриве Релеасехостдриве (Впккоминтерфацес. h)
description: Освобождает захваченный диск узла с DVD-диска.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- Метод Релеасехостдриве Virtual PC
- Метод Релеасехостдриве Virtual PC, интерфейс Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, метод Релеасехостдриве
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415313"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a><span data-ttu-id="729da-106">Метод Ивмдвддриве:: Релеасехостдриве</span><span class="sxs-lookup"><span data-stu-id="729da-106">IVMDVDDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="729da-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="729da-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="729da-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="729da-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="729da-109">Освобождает захваченный диск узла с DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="729da-109">Releases a captured host drive from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="729da-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="729da-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="729da-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="729da-111">Parameters</span></span>

<span data-ttu-id="729da-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="729da-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="729da-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="729da-113">Return value</span></span>

<span data-ttu-id="729da-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="729da-114">This method can return one of these values.</span></span>



| <span data-ttu-id="729da-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="729da-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="729da-116">Описание</span><span class="sxs-lookup"><span data-stu-id="729da-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="729da-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="729da-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="729da-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="729da-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="729da-119"><dt>**Д \_ Сбой**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="729da-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="729da-120">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="729da-120">An unexpected error has occurred.</span></span><br/>                                  |
| <dl> <span data-ttu-id="729da-121"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="729da-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="729da-122">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="729da-122">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="729da-123"><dt>**Виртуальная машина \_ \_ \_ Неверный \_ тип носителя**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="729da-123"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="729da-124">Текущий сохраненный носитель не является диском узла.</span><span class="sxs-lookup"><span data-stu-id="729da-124">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="729da-125"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="729da-125"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="729da-126">Не удалось инициализировать диск из-за недопустимого расположения шины.</span><span class="sxs-lookup"><span data-stu-id="729da-126">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="729da-127"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="729da-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="729da-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="729da-128">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="729da-129">Требования</span><span class="sxs-lookup"><span data-stu-id="729da-129">Requirements</span></span>



| <span data-ttu-id="729da-130">Требование</span><span class="sxs-lookup"><span data-stu-id="729da-130">Requirement</span></span> | <span data-ttu-id="729da-131">Значение</span><span class="sxs-lookup"><span data-stu-id="729da-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="729da-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="729da-132">Minimum supported client</span></span><br/> | <span data-ttu-id="729da-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="729da-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="729da-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="729da-134">Minimum supported server</span></span><br/> | <span data-ttu-id="729da-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="729da-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="729da-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="729da-136">End of client support</span></span><br/>    | <span data-ttu-id="729da-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="729da-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="729da-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="729da-138">Product</span></span><br/>                  | <span data-ttu-id="729da-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="729da-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="729da-140">Header</span><span class="sxs-lookup"><span data-stu-id="729da-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="729da-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="729da-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="729da-142">IID</span><span class="sxs-lookup"><span data-stu-id="729da-142">IID</span></span><br/>                      | <span data-ttu-id="729da-143">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="729da-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="729da-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="729da-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="729da-145">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="729da-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

