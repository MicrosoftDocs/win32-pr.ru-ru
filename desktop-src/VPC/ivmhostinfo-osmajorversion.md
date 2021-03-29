---
title: Свойство дочерний osmajorversion Ивмхостинфо (Впккоминтерфацес. h)
description: Извлекает основной номер версии операционной системы, работающей на размещающем компьютере.
ms.assetid: d0b62d2d-532f-45c7-8622-67176b9b4a8f
keywords:
- Дочерний osmajorversion свойство Virtual PC
- Дочерний osmajorversion свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство дочерний osmajorversion
topic_type:
- apiref
api_name:
- IVMHostInfo.OSMajorVersion
- IVMHostInfo.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf064744d90ede010a7e48e0e23e6a62a19eb4af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414689"
---
# <a name="ivmhostinfoosmajorversion-property"></a><span data-ttu-id="e377a-106">Свойство Ивмхостинфо:: дочерний osmajorversion</span><span class="sxs-lookup"><span data-stu-id="e377a-106">IVMHostInfo::OSMajorVersion property</span></span>

<span data-ttu-id="e377a-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e377a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e377a-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e377a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e377a-109">Извлекает основной номер версии операционной системы, работающей на размещающем компьютере.</span><span class="sxs-lookup"><span data-stu-id="e377a-109">Retrieves the major version of the operating system running on the host machine.</span></span>

<span data-ttu-id="e377a-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e377a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e377a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e377a-111">Syntax</span></span>


```C++
HRESULT get_OSMajorVersion(
  [out, retval] long *osMajorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="e377a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e377a-112">Property value</span></span>

<span data-ttu-id="e377a-113">Основная версия.</span><span class="sxs-lookup"><span data-stu-id="e377a-113">The major version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e377a-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e377a-114">Error codes</span></span>



| <span data-ttu-id="e377a-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="e377a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e377a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e377a-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e377a-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e377a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e377a-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e377a-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e377a-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="e377a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e377a-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e377a-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="e377a-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e377a-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e377a-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e377a-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e377a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e377a-123">Requirements</span></span>



| <span data-ttu-id="e377a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e377a-124">Requirement</span></span> | <span data-ttu-id="e377a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e377a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e377a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e377a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e377a-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e377a-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e377a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e377a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e377a-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e377a-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e377a-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e377a-130">End of client support</span></span><br/>    | <span data-ttu-id="e377a-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e377a-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e377a-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="e377a-132">Product</span></span><br/>                  | <span data-ttu-id="e377a-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e377a-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e377a-134">Header</span><span class="sxs-lookup"><span data-stu-id="e377a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e377a-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e377a-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e377a-136">IID</span><span class="sxs-lookup"><span data-stu-id="e377a-136">IID</span></span><br/>                      | <span data-ttu-id="e377a-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="e377a-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="e377a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e377a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e377a-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="e377a-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

