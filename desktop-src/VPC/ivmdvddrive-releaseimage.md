---
title: Метод Ивмдвддриве Релеасеимаже (Впккоминтерфацес. h)
description: Освобождает захваченный образ ISO с DVD-диска.
ms.assetid: 7cc95cf3-9d25-495f-863c-8eddd4068835
keywords:
- Метод Релеасеимаже Virtual PC
- Метод Релеасеимаже Virtual PC, интерфейс Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, метод Релеасеимаже
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a36a13b258d155760269399d9f25f5eda6f296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489339"
---
# <a name="ivmdvddrivereleaseimage-method"></a><span data-ttu-id="273f9-106">Метод Ивмдвддриве:: Релеасеимаже</span><span class="sxs-lookup"><span data-stu-id="273f9-106">IVMDVDDrive::ReleaseImage method</span></span>

<span data-ttu-id="273f9-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="273f9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="273f9-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="273f9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="273f9-109">Освобождает захваченный образ ISO с DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="273f9-109">Releases a captured ISO image from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="273f9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="273f9-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="273f9-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="273f9-111">Parameters</span></span>

<span data-ttu-id="273f9-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="273f9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="273f9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="273f9-113">Return value</span></span>

<span data-ttu-id="273f9-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="273f9-114">This method can return one of these values.</span></span>



| <span data-ttu-id="273f9-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="273f9-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="273f9-116">Описание</span><span class="sxs-lookup"><span data-stu-id="273f9-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="273f9-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="273f9-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="273f9-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="273f9-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="273f9-119"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="273f9-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="273f9-120">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="273f9-120">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="273f9-121"><dt>**Виртуальная машина \_ \_ \_ Неверный \_ тип носителя**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="273f9-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="273f9-122">Текущий сохраненный носитель не является диском узла.</span><span class="sxs-lookup"><span data-stu-id="273f9-122">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="273f9-123"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="273f9-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="273f9-124">Не удалось инициализировать диск из-за недопустимого расположения шины.</span><span class="sxs-lookup"><span data-stu-id="273f9-124">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="273f9-125"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="273f9-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="273f9-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="273f9-126">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="273f9-127">Требования</span><span class="sxs-lookup"><span data-stu-id="273f9-127">Requirements</span></span>



| <span data-ttu-id="273f9-128">Требование</span><span class="sxs-lookup"><span data-stu-id="273f9-128">Requirement</span></span> | <span data-ttu-id="273f9-129">Значение</span><span class="sxs-lookup"><span data-stu-id="273f9-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="273f9-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="273f9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="273f9-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="273f9-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="273f9-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="273f9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="273f9-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="273f9-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="273f9-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="273f9-134">End of client support</span></span><br/>    | <span data-ttu-id="273f9-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="273f9-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="273f9-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="273f9-136">Product</span></span><br/>                  | <span data-ttu-id="273f9-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="273f9-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="273f9-138">Header</span><span class="sxs-lookup"><span data-stu-id="273f9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="273f9-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="273f9-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="273f9-140">IID</span><span class="sxs-lookup"><span data-stu-id="273f9-140">IID</span></span><br/>                      | <span data-ttu-id="273f9-141">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="273f9-141">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="273f9-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="273f9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273f9-143">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="273f9-143">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

