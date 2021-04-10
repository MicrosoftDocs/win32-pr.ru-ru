---
title: Свойство дочерний osminorversion Ивмхостинфо (Впккоминтерфацес. h)
description: Извлекает дополнительный номер версии операционной системы, работающей на размещающем компьютере.
ms.assetid: 12f3ac59-ab7d-40f6-a0e6-fb870d2dff16
keywords:
- Дочерний osminorversion свойство Virtual PC
- Дочерний osminorversion свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство дочерний osminorversion
topic_type:
- apiref
api_name:
- IVMHostInfo.OSMinorVersion
- IVMHostInfo.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3063a752886ebd196f1462ce67572fe62d032f4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135047"
---
# <a name="ivmhostinfoosminorversion-property"></a><span data-ttu-id="c43be-106">Свойство Ивмхостинфо:: дочерний osminorversion</span><span class="sxs-lookup"><span data-stu-id="c43be-106">IVMHostInfo::OSMinorVersion property</span></span>

<span data-ttu-id="c43be-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c43be-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c43be-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c43be-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c43be-109">Извлекает дополнительный номер версии операционной системы, работающей на размещающем компьютере.</span><span class="sxs-lookup"><span data-stu-id="c43be-109">Retrieves the minor version of the operating system running on the host machine.</span></span>

<span data-ttu-id="c43be-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c43be-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43be-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c43be-111">Syntax</span></span>


```C++
HRESULT get_OSMinorVersion(
  [out, retval] long *osMinorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="c43be-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c43be-112">Property value</span></span>

<span data-ttu-id="c43be-113">Дополнительная версия.</span><span class="sxs-lookup"><span data-stu-id="c43be-113">The minor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c43be-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c43be-114">Error codes</span></span>



| <span data-ttu-id="c43be-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="c43be-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c43be-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c43be-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c43be-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c43be-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c43be-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c43be-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c43be-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c43be-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c43be-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c43be-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c43be-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c43be-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c43be-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c43be-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c43be-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c43be-123">Requirements</span></span>



| <span data-ttu-id="c43be-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c43be-124">Requirement</span></span> | <span data-ttu-id="c43be-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c43be-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c43be-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c43be-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c43be-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c43be-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c43be-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c43be-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c43be-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c43be-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c43be-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c43be-130">End of client support</span></span><br/>    | <span data-ttu-id="c43be-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c43be-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c43be-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="c43be-132">Product</span></span><br/>                  | <span data-ttu-id="c43be-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c43be-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c43be-134">Header</span><span class="sxs-lookup"><span data-stu-id="c43be-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c43be-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c43be-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c43be-136">IID</span><span class="sxs-lookup"><span data-stu-id="c43be-136">IID</span></span><br/>                      | <span data-ttu-id="c43be-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="c43be-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c43be-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c43be-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c43be-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="c43be-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

