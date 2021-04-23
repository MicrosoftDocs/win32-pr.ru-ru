---
title: Свойство Фисикалпроцессоркаунт Ивмхостинфо (Впккоминтерфацес. h)
description: Возвращает число физических процессоров на размещающем компьютере.
ms.assetid: b8f805a6-2962-4a48-94e9-bd76220974f0
keywords:
- Фисикалпроцессоркаунт свойство Virtual PC
- Фисикалпроцессоркаунт свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Фисикалпроцессоркаунт
topic_type:
- apiref
api_name:
- IVMHostInfo.PhysicalProcessorCount
- IVMHostInfo.get_PhysicalProcessorCount
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b161795a8430b6006d1f6a8aa87e91225430016c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135046"
---
# <a name="ivmhostinfophysicalprocessorcount-property"></a><span data-ttu-id="226ab-106">Ивмхостинфо: свойство Хисикалпроцессоркаунт:P</span><span class="sxs-lookup"><span data-stu-id="226ab-106">IVMHostInfo::PhysicalProcessorCount property</span></span>

<span data-ttu-id="226ab-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="226ab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="226ab-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="226ab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="226ab-109">Возвращает число физических процессоров на размещающем компьютере.</span><span class="sxs-lookup"><span data-stu-id="226ab-109">Retrieves the number of physical processors in the host machine.</span></span>

<span data-ttu-id="226ab-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="226ab-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="226ab-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="226ab-111">Syntax</span></span>


```C++
HRESULT get_PhysicalProcessorCount(
  [out, retval] long *processorCount
);
```



## <a name="property-value"></a><span data-ttu-id="226ab-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="226ab-112">Property value</span></span>

<span data-ttu-id="226ab-113">Число физических процессоров.</span><span class="sxs-lookup"><span data-stu-id="226ab-113">The number of physical processors.</span></span>

## <a name="error-codes"></a><span data-ttu-id="226ab-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="226ab-114">Error codes</span></span>



| <span data-ttu-id="226ab-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="226ab-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="226ab-116">Значение</span><span class="sxs-lookup"><span data-stu-id="226ab-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="226ab-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="226ab-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="226ab-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="226ab-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="226ab-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="226ab-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="226ab-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="226ab-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="226ab-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="226ab-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="226ab-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="226ab-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="226ab-123">Требования</span><span class="sxs-lookup"><span data-stu-id="226ab-123">Requirements</span></span>



| <span data-ttu-id="226ab-124">Требование</span><span class="sxs-lookup"><span data-stu-id="226ab-124">Requirement</span></span> | <span data-ttu-id="226ab-125">Значение</span><span class="sxs-lookup"><span data-stu-id="226ab-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="226ab-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="226ab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="226ab-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="226ab-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="226ab-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="226ab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="226ab-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="226ab-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="226ab-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="226ab-130">End of client support</span></span><br/>    | <span data-ttu-id="226ab-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="226ab-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="226ab-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="226ab-132">Product</span></span><br/>                  | <span data-ttu-id="226ab-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="226ab-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="226ab-134">Header</span><span class="sxs-lookup"><span data-stu-id="226ab-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="226ab-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="226ab-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="226ab-136">IID</span><span class="sxs-lookup"><span data-stu-id="226ab-136">IID</span></span><br/>                      | <span data-ttu-id="226ab-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="226ab-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="226ab-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="226ab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="226ab-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="226ab-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

