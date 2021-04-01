---
title: Свойство типа Ивмхарддиск (Впккоминтерфацес. h)
description: Тип виртуального жесткого диска.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Тип свойства Virtual PC
- Тип свойства Virtual PC, интерфейс Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, тип Property
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071582"
---
# <a name="ivmharddisktype-property"></a><span data-ttu-id="70efc-106">Свойство Ивмхарддиск:: Type</span><span class="sxs-lookup"><span data-stu-id="70efc-106">IVMHardDisk::Type property</span></span>

<span data-ttu-id="70efc-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="70efc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="70efc-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="70efc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="70efc-109">Извлекает тип виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="70efc-109">Retrieves the type of the virtual hard disk.</span></span>

<span data-ttu-id="70efc-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="70efc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="70efc-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70efc-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a><span data-ttu-id="70efc-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="70efc-112">Property value</span></span>

<span data-ttu-id="70efc-113">Тип текущего образа жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="70efc-113">The type of the current hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="70efc-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="70efc-114">Error codes</span></span>



| <span data-ttu-id="70efc-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="70efc-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="70efc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="70efc-116">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70efc-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70efc-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="70efc-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="70efc-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="70efc-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="70efc-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="70efc-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="70efc-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="70efc-121"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="70efc-121"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="70efc-122">Не удалось найти файл образа текущего жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="70efc-122">The current hard disk image file could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="70efc-123"><dt>Виртуальная машина \_ \_Диск E \_ Недопустимый</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="70efc-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="70efc-124">Недопустимый тип текущего образа жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="70efc-124">The type of the current hard disk image is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="70efc-125"><dt>Виртуальная машина \_ \_Образ E \_ HD \_ Open \_ Fail</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="70efc-125"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="70efc-126">При попытке открыть текущий файл образа жесткого диска произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="70efc-126">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="70efc-127"><dt>Виртуальная машина \_ 0xA0040681 \_ \_ \_ доступа к образу HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="70efc-127"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="70efc-128">Произошла ошибка при попытке доступа к текущему файлу образа жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="70efc-128">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="70efc-129"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="70efc-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="70efc-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="70efc-130">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="70efc-131">Требования</span><span class="sxs-lookup"><span data-stu-id="70efc-131">Requirements</span></span>



| <span data-ttu-id="70efc-132">Требование</span><span class="sxs-lookup"><span data-stu-id="70efc-132">Requirement</span></span> | <span data-ttu-id="70efc-133">Значение</span><span class="sxs-lookup"><span data-stu-id="70efc-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="70efc-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70efc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="70efc-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="70efc-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70efc-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70efc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="70efc-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="70efc-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="70efc-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="70efc-138">End of client support</span></span><br/>    | <span data-ttu-id="70efc-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="70efc-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="70efc-140">Продукт</span><span class="sxs-lookup"><span data-stu-id="70efc-140">Product</span></span><br/>                  | <span data-ttu-id="70efc-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="70efc-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="70efc-142">Header</span><span class="sxs-lookup"><span data-stu-id="70efc-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="70efc-143"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="70efc-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="70efc-144">IID</span><span class="sxs-lookup"><span data-stu-id="70efc-144">IID</span></span><br/>                      | <span data-ttu-id="70efc-145">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="70efc-145">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="70efc-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70efc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70efc-147">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="70efc-147">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

