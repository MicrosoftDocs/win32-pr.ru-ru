---
title: Свойство ProcessorSpeed Ивмхостинфо (Впккоминтерфацес. h)
description: Скорость хост-процессора в мегагерцах (МГц) или ГГц.
ms.assetid: 2d5e3f2e-8e81-4527-bd7f-52bf5b1f56ef
keywords:
- ProcessorSpeed свойство Virtual PC
- ProcessorSpeed свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство ProcessorSpeed
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeed
- IVMHostInfo.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28fc890392db5f61a7819fa1d4b4a11d2b3de312
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071069"
---
# <a name="ivmhostinfoprocessorspeed-property"></a><span data-ttu-id="3e625-106">Ивмхостинфо: свойство Роцессорспид:P</span><span class="sxs-lookup"><span data-stu-id="3e625-106">IVMHostInfo::ProcessorSpeed property</span></span>

<span data-ttu-id="3e625-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e625-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e625-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e625-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e625-109">Возвращает скорость хост-процессора в мегагерцах (МГц) или ГГц.</span><span class="sxs-lookup"><span data-stu-id="3e625-109">Retrieves the speed of the host processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="3e625-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3e625-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e625-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e625-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="3e625-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3e625-112">Property value</span></span>

<span data-ttu-id="3e625-113">Скорость процессора в мегагерцах или в ГГц.</span><span class="sxs-lookup"><span data-stu-id="3e625-113">The processor speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e625-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3e625-114">Error codes</span></span>



| <span data-ttu-id="3e625-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="3e625-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3e625-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3e625-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3e625-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e625-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3e625-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3e625-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3e625-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="3e625-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3e625-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e625-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3e625-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3e625-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3e625-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3e625-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3e625-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3e625-123">Requirements</span></span>



| <span data-ttu-id="3e625-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3e625-124">Requirement</span></span> | <span data-ttu-id="3e625-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3e625-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e625-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e625-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e625-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3e625-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e625-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e625-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e625-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3e625-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e625-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3e625-130">End of client support</span></span><br/>    | <span data-ttu-id="3e625-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e625-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e625-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="3e625-132">Product</span></span><br/>                  | <span data-ttu-id="3e625-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e625-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e625-134">Header</span><span class="sxs-lookup"><span data-stu-id="3e625-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e625-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e625-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e625-136">IID</span><span class="sxs-lookup"><span data-stu-id="3e625-136">IID</span></span><br/>                      | <span data-ttu-id="3e625-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="3e625-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3e625-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e625-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e625-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="3e625-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

