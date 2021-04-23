---
title: Свойство Сизеингуест Ивмхарддиск (Впккоминтерфацес. h)
description: Получение размера виртуального жесткого диска в гостевой операционной системе.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- Сизеингуест свойство Virtual PC
- Сизеингуест свойство Virtual PC, интерфейс Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, свойство Сизеингуест
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136723"
---
# <a name="ivmharddisksizeinguest-property"></a><span data-ttu-id="7f105-106">Свойство Ивмхарддиск:: Сизеингуест</span><span class="sxs-lookup"><span data-stu-id="7f105-106">IVMHardDisk::SizeInGuest property</span></span>

<span data-ttu-id="7f105-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7f105-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7f105-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7f105-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7f105-109">Получение размера виртуального жесткого диска в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="7f105-109">Retrieves the size of the virtual hard disk in the guest operating system.</span></span>

<span data-ttu-id="7f105-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7f105-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f105-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f105-111">Syntax</span></span>


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="7f105-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7f105-112">Property value</span></span>

<span data-ttu-id="7f105-113">Размер образа жесткого диска (в байтах).</span><span class="sxs-lookup"><span data-stu-id="7f105-113">The size, in bytes, of the hard disk image.</span></span> <span data-ttu-id="7f105-114">Это значение является **разновидностью** типа \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="7f105-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f105-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7f105-115">Error codes</span></span>



| <span data-ttu-id="7f105-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="7f105-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="7f105-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7f105-117">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f105-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f105-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="7f105-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7f105-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="7f105-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="7f105-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="7f105-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7f105-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="7f105-122"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="7f105-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="7f105-123">Не удалось найти текущий файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7f105-123">The current virtual hard disk file could not be found.</span></span><br/>                         |
| <dl> <span data-ttu-id="7f105-124"><dt>Виртуальная машина \_ \_Образ E \_ HD \_ Open \_ Fail</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="7f105-124"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="7f105-125">При попытке открыть текущий файл образа жесткого диска произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="7f105-125">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="7f105-126"><dt>Виртуальная машина \_ 0xA0040681 \_ \_ \_ доступа к образу HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7f105-126"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="7f105-127">Произошла ошибка при попытке доступа к текущему файлу образа жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7f105-127">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="7f105-128"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7f105-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="7f105-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7f105-129">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="7f105-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7f105-130">Requirements</span></span>



| <span data-ttu-id="7f105-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7f105-131">Requirement</span></span> | <span data-ttu-id="7f105-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7f105-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f105-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f105-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7f105-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7f105-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f105-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f105-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7f105-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7f105-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7f105-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7f105-137">End of client support</span></span><br/>    | <span data-ttu-id="7f105-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f105-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7f105-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="7f105-139">Product</span></span><br/>                  | <span data-ttu-id="7f105-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7f105-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7f105-141">Header</span><span class="sxs-lookup"><span data-stu-id="7f105-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f105-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f105-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7f105-143">IID</span><span class="sxs-lookup"><span data-stu-id="7f105-143">IID</span></span><br/>                      | <span data-ttu-id="7f105-144">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="7f105-144">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="7f105-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f105-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f105-146">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="7f105-146">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

