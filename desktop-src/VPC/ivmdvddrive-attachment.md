---
title: Свойство вложения Ивмдвддриве (Впккоминтерфацес. h)
description: Возвращает тип носителя, подключенного к DVD-дисководу в виртуальной машине.
ms.assetid: 7ae1714d-e5e9-4f6a-85a6-c0b3c4d21820
keywords:
- Свойство вложения Virtual PC
- Свойство вложения Virtual PC, интерфейс Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, свойство вложения
topic_type:
- apiref
api_name:
- IVMDVDDrive.Attachment
- IVMDVDDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5c7801e11534249da899797b73b632a7eda307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892305"
---
# <a name="ivmdvddriveattachment-property"></a><span data-ttu-id="1f677-106">Свойство Ивмдвддриве:: вложение</span><span class="sxs-lookup"><span data-stu-id="1f677-106">IVMDVDDrive::Attachment property</span></span>

<span data-ttu-id="1f677-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1f677-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1f677-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1f677-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1f677-109">Возвращает тип носителя, подключенного к DVD-дисководу в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="1f677-109">Retrieves the type of media attached to the DVD drive within the virtual machine.</span></span>

<span data-ttu-id="1f677-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1f677-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f677-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f677-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMDVDDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="1f677-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1f677-112">Property value</span></span>

<span data-ttu-id="1f677-113">Тип подключенного носителя.</span><span class="sxs-lookup"><span data-stu-id="1f677-113">The attached media type.</span></span> <span data-ttu-id="1f677-114">Список значений см. в разделе [**вмдвддривеаттачменттипе**](vmdvddriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="1f677-114">For a list of values, see [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f677-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="1f677-115">Error codes</span></span>



| <span data-ttu-id="1f677-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="1f677-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="1f677-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1f677-117">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="1f677-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1f677-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="1f677-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1f677-119">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="1f677-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="1f677-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="1f677-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f677-121">The parameter is **NULL**.</span></span><br/>                  |
| <dl> <span data-ttu-id="1f677-122"><dt>Д \_ Сбой</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="1f677-122"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="1f677-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1f677-123">An unexpected error has occurred.</span></span><br/>           |
| <dl> <span data-ttu-id="1f677-124"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1f677-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="1f677-125">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="1f677-125">The virtual machine could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="1f677-126"><dt>Виртуальная машина \_ \_Диск E \_ Недопустимый</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="1f677-126"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="1f677-127">Недопустимое расположение шины для этого диска.</span><span class="sxs-lookup"><span data-stu-id="1f677-127">The bus location for this drive is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="1f677-128"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1f677-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="1f677-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1f677-129">An unexpected error has occurred.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="1f677-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1f677-130">Requirements</span></span>



| <span data-ttu-id="1f677-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1f677-131">Requirement</span></span> | <span data-ttu-id="1f677-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1f677-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f677-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f677-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1f677-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1f677-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f677-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f677-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1f677-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1f677-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1f677-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1f677-137">End of client support</span></span><br/>    | <span data-ttu-id="1f677-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1f677-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1f677-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="1f677-139">Product</span></span><br/>                  | <span data-ttu-id="1f677-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1f677-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1f677-141">Header</span><span class="sxs-lookup"><span data-stu-id="1f677-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f677-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f677-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1f677-143">IID</span><span class="sxs-lookup"><span data-stu-id="1f677-143">IID</span></span><br/>                      | <span data-ttu-id="1f677-144">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="1f677-144">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1f677-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f677-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f677-146">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="1f677-146">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

