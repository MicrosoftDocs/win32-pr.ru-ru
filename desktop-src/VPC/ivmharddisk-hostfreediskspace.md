---
title: Свойство Хостфридискспаце Ивмхарддиск (Впккоминтерфацес. h)
description: Получение оставшегося свободного места на диске, доступного на узле для виртуального жесткого диска.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- Хостфридискспаце свойство Virtual PC
- Хостфридискспаце свойство Virtual PC, интерфейс Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, свойство Хостфридискспаце
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137319"
---
# <a name="ivmharddiskhostfreediskspace-property"></a><span data-ttu-id="cb01f-106">Свойство Ивмхарддиск:: Хостфридискспаце</span><span class="sxs-lookup"><span data-stu-id="cb01f-106">IVMHardDisk::HostFreeDiskSpace property</span></span>

<span data-ttu-id="cb01f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cb01f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cb01f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cb01f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cb01f-109">Получение оставшегося свободного места на диске, доступного на узле для виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="cb01f-109">Retrieves the amount of remaining disk space available on the host for the virtual hard disk.</span></span>

<span data-ttu-id="cb01f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cb01f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb01f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb01f-111">Syntax</span></span>


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a><span data-ttu-id="cb01f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cb01f-112">Property value</span></span>

<span data-ttu-id="cb01f-113">Оставшийся объем свободного места на диске на главном компьютере для текущего файла образа жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="cb01f-113">The amount of remaining disk space available on the host computer for the current hard disk image file.</span></span> <span data-ttu-id="cb01f-114">Это значение является **разновидностью** типа \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="cb01f-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb01f-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="cb01f-115">Error codes</span></span>



| <span data-ttu-id="cb01f-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="cb01f-116">Name/value</span></span>                                                                                                                                                                            | <span data-ttu-id="cb01f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cb01f-117">Meaning</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb01f-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cb01f-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                               | <span data-ttu-id="cb01f-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cb01f-119">The operation was successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="cb01f-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="cb01f-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                 | <span data-ttu-id="cb01f-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cb01f-121">The parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="cb01f-122"><dt>Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="cb01f-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl> | <span data-ttu-id="cb01f-123">Недопустимый путь к текущему файлу виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="cb01f-123">The path to the current virtual hard disk file is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="cb01f-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cb01f-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                         | <span data-ttu-id="cb01f-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="cb01f-125">An unexpected error has occurred.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="cb01f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cb01f-126">Requirements</span></span>



| <span data-ttu-id="cb01f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cb01f-127">Requirement</span></span> | <span data-ttu-id="cb01f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cb01f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb01f-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb01f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cb01f-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cb01f-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb01f-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb01f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cb01f-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cb01f-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cb01f-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cb01f-133">End of client support</span></span><br/>    | <span data-ttu-id="cb01f-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb01f-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cb01f-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="cb01f-135">Product</span></span><br/>                  | <span data-ttu-id="cb01f-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cb01f-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cb01f-137">Header</span><span class="sxs-lookup"><span data-stu-id="cb01f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb01f-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb01f-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cb01f-139">IID</span><span class="sxs-lookup"><span data-stu-id="cb01f-139">IID</span></span><br/>                      | <span data-ttu-id="cb01f-140">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="cb01f-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="cb01f-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb01f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb01f-142">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="cb01f-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

