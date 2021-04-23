---
title: Свойство Утктиме Ивмхостинфо (Впккоминтерфацес. h)
description: Извлекает время в формате UTC на размещающем компьютере.
ms.assetid: 07f9b042-0eb6-4cb5-b70b-6fcd3456d46b
keywords:
- Утктиме свойство Virtual PC
- Утктиме свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Утктиме
topic_type:
- apiref
api_name:
- IVMHostInfo.UTCTime
- IVMHostInfo.get_UTCTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcd913db320f24446de6b72dd220f2c67713a16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534247"
---
# <a name="ivmhostinfoutctime-property"></a><span data-ttu-id="d30f9-106">Свойство Ивмхостинфо:: Утктиме</span><span class="sxs-lookup"><span data-stu-id="d30f9-106">IVMHostInfo::UTCTime property</span></span>

<span data-ttu-id="d30f9-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d30f9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d30f9-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d30f9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d30f9-109">Извлекает время в формате UTC на размещающем компьютере.</span><span class="sxs-lookup"><span data-stu-id="d30f9-109">Retrieves the UTC time on the host machine.</span></span>

<span data-ttu-id="d30f9-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d30f9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d30f9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d30f9-111">Syntax</span></span>


```C++
HRESULT get_UTCTime(
  [out, retval] DATE *UTCTime
);
```



## <a name="property-value"></a><span data-ttu-id="d30f9-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d30f9-112">Property value</span></span>

<span data-ttu-id="d30f9-113">Текущее время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="d30f9-113">The current UTC time.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d30f9-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d30f9-114">Error codes</span></span>



| <span data-ttu-id="d30f9-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="d30f9-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d30f9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d30f9-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d30f9-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d30f9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d30f9-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d30f9-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d30f9-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d30f9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d30f9-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d30f9-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d30f9-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d30f9-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d30f9-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d30f9-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d30f9-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d30f9-123">Requirements</span></span>



| <span data-ttu-id="d30f9-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d30f9-124">Requirement</span></span> | <span data-ttu-id="d30f9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d30f9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d30f9-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d30f9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d30f9-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d30f9-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d30f9-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d30f9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d30f9-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d30f9-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d30f9-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d30f9-130">End of client support</span></span><br/>    | <span data-ttu-id="d30f9-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d30f9-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d30f9-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="d30f9-132">Product</span></span><br/>                  | <span data-ttu-id="d30f9-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d30f9-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d30f9-134">Header</span><span class="sxs-lookup"><span data-stu-id="d30f9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d30f9-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d30f9-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d30f9-136">IID</span><span class="sxs-lookup"><span data-stu-id="d30f9-136">IID</span></span><br/>                      | <span data-ttu-id="d30f9-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="d30f9-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d30f9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d30f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d30f9-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="d30f9-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

