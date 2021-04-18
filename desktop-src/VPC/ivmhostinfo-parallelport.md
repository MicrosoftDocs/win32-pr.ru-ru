---
title: Свойство Параллелпорт Ивмхостинфо (Впккоминтерфацес. h)
description: Извлекает параллельный порт узла, который может быть подключен к гостевой системе.
ms.assetid: 4c9486b8-ab66-4874-b467-a7a0ab7934f1
keywords:
- Параллелпорт свойство Virtual PC
- Параллелпорт свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Параллелпорт
topic_type:
- apiref
api_name:
- IVMHostInfo.ParallelPort
- IVMHostInfo.get_ParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0a2050ff505f5ed7a54cf3857ea28661d4d3d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533734"
---
# <a name="ivmhostinfoparallelport-property"></a><span data-ttu-id="43917-106">Ивмхостинфо: свойство Араллелпорт:P</span><span class="sxs-lookup"><span data-stu-id="43917-106">IVMHostInfo::ParallelPort property</span></span>

<span data-ttu-id="43917-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="43917-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="43917-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="43917-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="43917-109">Извлекает параллельный порт узла, который может быть подключен к гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="43917-109">Retrieves the host parallel port that can be attached to the guest.</span></span>

<span data-ttu-id="43917-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="43917-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="43917-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43917-111">Syntax</span></span>


```C++
HRESULT get_ParallelPort(
  [out, retval] BSTR *vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="43917-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="43917-112">Property value</span></span>

<span data-ttu-id="43917-113">Имя параллельного порта.</span><span class="sxs-lookup"><span data-stu-id="43917-113">The name of the parallel port.</span></span>

## <a name="error-codes"></a><span data-ttu-id="43917-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="43917-114">Error codes</span></span>



| <span data-ttu-id="43917-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="43917-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="43917-116">Значение</span><span class="sxs-lookup"><span data-stu-id="43917-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="43917-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43917-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="43917-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="43917-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="43917-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="43917-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="43917-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="43917-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="43917-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="43917-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="43917-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="43917-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="43917-123">Требования</span><span class="sxs-lookup"><span data-stu-id="43917-123">Requirements</span></span>



| <span data-ttu-id="43917-124">Требование</span><span class="sxs-lookup"><span data-stu-id="43917-124">Requirement</span></span> | <span data-ttu-id="43917-125">Значение</span><span class="sxs-lookup"><span data-stu-id="43917-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43917-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43917-126">Minimum supported client</span></span><br/> | <span data-ttu-id="43917-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="43917-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43917-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43917-128">Minimum supported server</span></span><br/> | <span data-ttu-id="43917-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="43917-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="43917-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="43917-130">End of client support</span></span><br/>    | <span data-ttu-id="43917-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43917-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="43917-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="43917-132">Product</span></span><br/>                  | <span data-ttu-id="43917-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="43917-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="43917-134">Header</span><span class="sxs-lookup"><span data-stu-id="43917-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="43917-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="43917-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="43917-136">IID</span><span class="sxs-lookup"><span data-stu-id="43917-136">IID</span></span><br/>                      | <span data-ttu-id="43917-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="43917-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="43917-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43917-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43917-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="43917-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

