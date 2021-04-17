---
title: Свойство файла Ивмхарддиск (Впккоминтерфацес. h)
description: Получает полный путь к файлу виртуального жесткого диска.
ms.assetid: 8c1f028a-32e6-4b70-b19c-bed7c2d53de1
keywords:
- Свойство файла Virtual PC
- Свойство файла Virtual PC, интерфейс Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, свойство File
topic_type:
- apiref
api_name:
- IVMHardDisk.File
- IVMHardDisk.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b2a83b92bb5d02049066f9be90543a34a2fe7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691925"
---
# <a name="ivmharddiskfile-property"></a><span data-ttu-id="edb3e-106">Ивмхарддиск:: File, свойство</span><span class="sxs-lookup"><span data-stu-id="edb3e-106">IVMHardDisk::File property</span></span>

<span data-ttu-id="edb3e-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edb3e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="edb3e-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="edb3e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="edb3e-109">Получает полный путь к файлу виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="edb3e-109">Retrieves the full path name of the virtual hard disk file.</span></span>

<span data-ttu-id="edb3e-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="edb3e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb3e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edb3e-111">Syntax</span></span>


```C++
HRESULT get_File(
  [out, retval] BSTR *hardDiskfile
);
```



## <a name="property-value"></a><span data-ttu-id="edb3e-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="edb3e-112">Property value</span></span>

<span data-ttu-id="edb3e-113">Полный путь к текущему файлу образа жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="edb3e-113">The full path name of the current hard disk image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="edb3e-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="edb3e-114">Error codes</span></span>



| <span data-ttu-id="edb3e-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="edb3e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="edb3e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="edb3e-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="edb3e-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="edb3e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="edb3e-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="edb3e-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="edb3e-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="edb3e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="edb3e-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="edb3e-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="edb3e-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="edb3e-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="edb3e-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="edb3e-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="edb3e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="edb3e-123">Requirements</span></span>



| <span data-ttu-id="edb3e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="edb3e-124">Requirement</span></span> | <span data-ttu-id="edb3e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="edb3e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="edb3e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edb3e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="edb3e-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="edb3e-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="edb3e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edb3e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="edb3e-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="edb3e-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="edb3e-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="edb3e-130">End of client support</span></span><br/>    | <span data-ttu-id="edb3e-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="edb3e-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="edb3e-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="edb3e-132">Product</span></span><br/>                  | <span data-ttu-id="edb3e-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="edb3e-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="edb3e-134">Header</span><span class="sxs-lookup"><span data-stu-id="edb3e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="edb3e-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="edb3e-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="edb3e-136">IID</span><span class="sxs-lookup"><span data-stu-id="edb3e-136">IID</span></span><br/>                      | <span data-ttu-id="edb3e-137">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="edb3e-137">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="edb3e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edb3e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb3e-139">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="edb3e-139">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

