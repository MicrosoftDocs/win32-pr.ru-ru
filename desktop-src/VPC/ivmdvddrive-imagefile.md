---
title: Свойство ImageFile Ивмдвддриве (Впккоминтерфацес. h)
description: Получает полный путь к набору файлов изображений для этого устройства.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- Свойство ImageFile Virtual PC
- Свойство ImageFile Virtual PC, интерфейс Ивмдвддриве
- Интерфейс Ивмдвддриве Virtual PC, свойство ImageFile
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892557"
---
# <a name="ivmdvddriveimagefile-property"></a><span data-ttu-id="25298-106">Свойство Ивмдвддриве:: ImageFile</span><span class="sxs-lookup"><span data-stu-id="25298-106">IVMDVDDrive::ImageFile property</span></span>

<span data-ttu-id="25298-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="25298-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="25298-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="25298-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="25298-109">Получает полный путь к набору файлов изображений для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="25298-109">Retrieves the full path of the image file set for this device.</span></span>

<span data-ttu-id="25298-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="25298-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="25298-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25298-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a><span data-ttu-id="25298-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="25298-112">Property value</span></span>

<span data-ttu-id="25298-113">Полный путь к файлу изображения.</span><span class="sxs-lookup"><span data-stu-id="25298-113">The full path to the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="25298-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="25298-114">Error codes</span></span>



| <span data-ttu-id="25298-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="25298-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="25298-116">Значение</span><span class="sxs-lookup"><span data-stu-id="25298-116">Meaning</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25298-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="25298-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="25298-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="25298-118">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="25298-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="25298-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="25298-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="25298-120">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="25298-121"><dt>Д \_ Сбой</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="25298-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="25298-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="25298-122">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="25298-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="25298-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="25298-124">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="25298-124">The virtual machine could not be found.</span></span><br/>                        |
| <dl> <span data-ttu-id="25298-125"><dt>Виртуальная машина \_ \_Диск E \_ Недопустимый</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="25298-125"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="25298-126">Недопустимое расположение шины для этого диска.</span><span class="sxs-lookup"><span data-stu-id="25298-126">The bus location for this drive is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="25298-127"><dt>Виртуальная машина \_ \_ \_ Неверный \_ тип носителя</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="25298-127"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="25298-128">Носитель, записываемый этим DVD-дисководом, не является файлом ISO-образа.</span><span class="sxs-lookup"><span data-stu-id="25298-128">The media captured by this DVD drive is not an ISO image file.</span></span><br/> |
| <dl> <span data-ttu-id="25298-129"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="25298-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="25298-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="25298-130">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="25298-131">Требования</span><span class="sxs-lookup"><span data-stu-id="25298-131">Requirements</span></span>



| <span data-ttu-id="25298-132">Требование</span><span class="sxs-lookup"><span data-stu-id="25298-132">Requirement</span></span> | <span data-ttu-id="25298-133">Значение</span><span class="sxs-lookup"><span data-stu-id="25298-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="25298-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25298-134">Minimum supported client</span></span><br/> | <span data-ttu-id="25298-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="25298-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25298-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25298-136">Minimum supported server</span></span><br/> | <span data-ttu-id="25298-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25298-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="25298-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="25298-138">End of client support</span></span><br/>    | <span data-ttu-id="25298-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="25298-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="25298-140">Продукт</span><span class="sxs-lookup"><span data-stu-id="25298-140">Product</span></span><br/>                  | <span data-ttu-id="25298-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="25298-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="25298-142">Header</span><span class="sxs-lookup"><span data-stu-id="25298-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="25298-143"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="25298-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="25298-144">IID</span><span class="sxs-lookup"><span data-stu-id="25298-144">IID</span></span><br/>                      | <span data-ttu-id="25298-145">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="25298-145">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="25298-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25298-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25298-147">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="25298-147">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

