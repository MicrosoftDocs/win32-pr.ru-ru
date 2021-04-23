---
title: Свойство Сизеонхост Ивмхарддиск (Впккоминтерфацес. h)
description: Размер файла виртуального жесткого диска на главном компьютере.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- Сизеонхост свойство Virtual PC
- Сизеонхост свойство Virtual PC, интерфейс Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, свойство Сизеонхост
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071835"
---
# <a name="ivmharddisksizeonhost-property"></a><span data-ttu-id="c750d-106">Свойство Ивмхарддиск:: Сизеонхост</span><span class="sxs-lookup"><span data-stu-id="c750d-106">IVMHardDisk::SizeOnHost property</span></span>

<span data-ttu-id="c750d-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c750d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c750d-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c750d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c750d-109">Получает размер файла виртуального жесткого диска на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c750d-109">Retrieves the size of the virtual hard disk file on the host computer.</span></span>

<span data-ttu-id="c750d-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c750d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c750d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c750d-111">Syntax</span></span>


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="c750d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c750d-112">Property value</span></span>

<span data-ttu-id="c750d-113">Размер файла образа жесткого диска в байтах.</span><span class="sxs-lookup"><span data-stu-id="c750d-113">The size, in bytes, of the hard disk image file.</span></span> <span data-ttu-id="c750d-114">Это значение является **разновидностью** типа **\_ Decimal**.</span><span class="sxs-lookup"><span data-stu-id="c750d-114">This value is a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c750d-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c750d-115">Error codes</span></span>



| <span data-ttu-id="c750d-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="c750d-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="c750d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c750d-117">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="c750d-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c750d-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="c750d-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c750d-119">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="c750d-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c750d-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="c750d-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c750d-121">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="c750d-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c750d-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="c750d-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c750d-123">An unexpected error has occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="c750d-124"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="c750d-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="c750d-125">Файл образа жесткого диска не найден.</span><span class="sxs-lookup"><span data-stu-id="c750d-125">The hard disk image file was not found.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c750d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c750d-126">Requirements</span></span>



| <span data-ttu-id="c750d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c750d-127">Requirement</span></span> | <span data-ttu-id="c750d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c750d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c750d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c750d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c750d-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c750d-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c750d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c750d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c750d-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c750d-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c750d-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c750d-133">End of client support</span></span><br/>    | <span data-ttu-id="c750d-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c750d-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c750d-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="c750d-135">Product</span></span><br/>                  | <span data-ttu-id="c750d-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c750d-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c750d-137">Header</span><span class="sxs-lookup"><span data-stu-id="c750d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c750d-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c750d-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c750d-139">IID</span><span class="sxs-lookup"><span data-stu-id="c750d-139">IID</span></span><br/>                      | <span data-ttu-id="c750d-140">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="c750d-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c750d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c750d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c750d-142">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="c750d-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

