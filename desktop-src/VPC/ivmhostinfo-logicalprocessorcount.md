---
title: Свойство Логикалпроцессоркаунт Ивмхостинфо (Впккоминтерфацес. h)
description: Возвращает число логических процессоров на размещающем компьютере.
ms.assetid: bf978a80-9a21-426a-ac18-109f20d38cbb
keywords:
- Логикалпроцессоркаунт свойство Virtual PC
- Логикалпроцессоркаунт свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Логикалпроцессоркаунт
topic_type:
- apiref
api_name:
- IVMHostInfo.LogicalProcessorCount
- IVMHostInfo.get_LogicalProcessorCount
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7668bb4332a41b1cae809c6c2f29a8eac99bade
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691767"
---
# <a name="ivmhostinfologicalprocessorcount-property"></a><span data-ttu-id="4fb76-106">Свойство Ивмхостинфо:: Логикалпроцессоркаунт</span><span class="sxs-lookup"><span data-stu-id="4fb76-106">IVMHostInfo::LogicalProcessorCount property</span></span>

<span data-ttu-id="4fb76-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4fb76-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4fb76-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4fb76-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4fb76-109">Возвращает число логических процессоров на размещающем компьютере.</span><span class="sxs-lookup"><span data-stu-id="4fb76-109">Retrieves the number of logical processors in the host machine.</span></span>

<span data-ttu-id="4fb76-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4fb76-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb76-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fb76-111">Syntax</span></span>


```C++
HRESULT get_LogicalProcessorCount(
  [out, retval] long *processorCount
);
```



## <a name="property-value"></a><span data-ttu-id="4fb76-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4fb76-112">Property value</span></span>

<span data-ttu-id="4fb76-113">Число логических процессоров.</span><span class="sxs-lookup"><span data-stu-id="4fb76-113">The number of logical processors.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4fb76-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4fb76-114">Error codes</span></span>



| <span data-ttu-id="4fb76-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="4fb76-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4fb76-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4fb76-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4fb76-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4fb76-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4fb76-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4fb76-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4fb76-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="4fb76-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4fb76-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4fb76-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="4fb76-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4fb76-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4fb76-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4fb76-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4fb76-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4fb76-123">Requirements</span></span>



| <span data-ttu-id="4fb76-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4fb76-124">Requirement</span></span> | <span data-ttu-id="4fb76-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4fb76-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb76-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fb76-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb76-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4fb76-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4fb76-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fb76-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb76-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4fb76-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4fb76-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4fb76-130">End of client support</span></span><br/>    | <span data-ttu-id="4fb76-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4fb76-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4fb76-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="4fb76-132">Product</span></span><br/>                  | <span data-ttu-id="4fb76-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4fb76-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4fb76-134">Header</span><span class="sxs-lookup"><span data-stu-id="4fb76-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fb76-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fb76-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4fb76-136">IID</span><span class="sxs-lookup"><span data-stu-id="4fb76-136">IID</span></span><br/>                      | <span data-ttu-id="4fb76-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="4fb76-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4fb76-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fb76-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb76-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="4fb76-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

