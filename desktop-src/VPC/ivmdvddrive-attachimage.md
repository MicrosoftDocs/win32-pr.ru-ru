---
title: Метод Ивмдвддриве Аттачимаже (Впккоминтерфацес. h)
description: Подключает образ ISO к DVD-дисководу в виртуальной машине.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- Метод Аттачимаже Virtual PC
- Метод Аттачимаже Virtual PC, интерфейс Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, метод Аттачимаже
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416025"
---
# <a name="ivmdvddriveattachimage-method"></a><span data-ttu-id="175af-106">Метод Ивмдвддриве:: Аттачимаже</span><span class="sxs-lookup"><span data-stu-id="175af-106">IVMDVDDrive::AttachImage method</span></span>

<span data-ttu-id="175af-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="175af-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="175af-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="175af-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="175af-109">Подключает образ ISO к DVD-дисководу в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="175af-109">Attaches an ISO image to the DVD drive within the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="175af-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="175af-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a><span data-ttu-id="175af-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="175af-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="175af-112">*imagePath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="175af-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="175af-113">Полный путь к прикрепленному ISO-образу.</span><span class="sxs-lookup"><span data-stu-id="175af-113">The full path to the ISO image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="175af-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="175af-114">Return value</span></span>

<span data-ttu-id="175af-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="175af-115">This method can return one of these values.</span></span>



| <span data-ttu-id="175af-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="175af-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="175af-117">Описание</span><span class="sxs-lookup"><span data-stu-id="175af-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="175af-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="175af-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="175af-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="175af-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="175af-120"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="175af-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="175af-121">Параметр *imagePath* является каталогом.</span><span class="sxs-lookup"><span data-stu-id="175af-121">The *imagePath* parameter is a directory.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="175af-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="175af-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="175af-123">Параметр *imagePath* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="175af-123">The *imagePath* parameter is **NULL**.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="175af-124"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="175af-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="175af-125">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="175af-125">The VM could not be found.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="175af-126"><dt>**Виртуальная машина \_ \_Диск E \_ \_ используется**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="175af-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="175af-127">Диск DVD или ISO-образ узла уже подключен к этому диску.</span><span class="sxs-lookup"><span data-stu-id="175af-127">A host DVD drive or ISO image is already attached to this drive.</span></span><br/>                                  |
| <dl> <span data-ttu-id="175af-128"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="175af-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="175af-129">Расположение шины для этого диска недопустимо, или диск не является допустимым DVD-дисководом.</span><span class="sxs-lookup"><span data-stu-id="175af-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/> |
| <dl> <span data-ttu-id="175af-130"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="175af-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="175af-131">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="175af-131">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="175af-132">Требования</span><span class="sxs-lookup"><span data-stu-id="175af-132">Requirements</span></span>



| <span data-ttu-id="175af-133">Требование</span><span class="sxs-lookup"><span data-stu-id="175af-133">Requirement</span></span> | <span data-ttu-id="175af-134">Значение</span><span class="sxs-lookup"><span data-stu-id="175af-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="175af-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="175af-135">Minimum supported client</span></span><br/> | <span data-ttu-id="175af-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="175af-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="175af-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="175af-137">Minimum supported server</span></span><br/> | <span data-ttu-id="175af-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="175af-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="175af-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="175af-139">End of client support</span></span><br/>    | <span data-ttu-id="175af-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="175af-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="175af-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="175af-141">Product</span></span><br/>                  | <span data-ttu-id="175af-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="175af-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="175af-143">Header</span><span class="sxs-lookup"><span data-stu-id="175af-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="175af-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="175af-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="175af-145">IID</span><span class="sxs-lookup"><span data-stu-id="175af-145">IID</span></span><br/>                      | <span data-ttu-id="175af-146">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="175af-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="175af-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="175af-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175af-148">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="175af-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

