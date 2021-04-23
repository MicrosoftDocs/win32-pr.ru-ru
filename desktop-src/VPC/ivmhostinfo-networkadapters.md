---
title: Свойство адаптера Ивмхостинфо (Впккоминтерфацес. h)
description: Получает перечисляемую коллекцию сетевых адаптеров на размещающем компьютере.
ms.assetid: 17393d7a-c883-4d67-826b-83b886c0d7a6
keywords:
- Адаптера свойство Virtual PC
- Адаптера свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство адаптера
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAdapters
- IVMHostInfo.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeff5c6d459fb8f6999f896c3c13fcd980bf70ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988160"
---
# <a name="ivmhostinfonetworkadapters-property"></a><span data-ttu-id="c6b88-106">Свойство Ивмхостинфо:: адаптера</span><span class="sxs-lookup"><span data-stu-id="c6b88-106">IVMHostInfo::NetworkAdapters property</span></span>

<span data-ttu-id="c6b88-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c6b88-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c6b88-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c6b88-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c6b88-109">Получает перечисляемую коллекцию сетевых адаптеров на размещающем компьютере.</span><span class="sxs-lookup"><span data-stu-id="c6b88-109">Retrieves an enumerable collection of NICs in the host machine.</span></span>

<span data-ttu-id="c6b88-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c6b88-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6b88-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6b88-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] VARIANT *hostNICs
);
```



## <a name="property-value"></a><span data-ttu-id="c6b88-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c6b88-112">Property value</span></span>

<span data-ttu-id="c6b88-113">Коллекция сетевых интерфейсных карт.</span><span class="sxs-lookup"><span data-stu-id="c6b88-113">A collection of network interface cards.</span></span> <span data-ttu-id="c6b88-114">Это массив значений **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="c6b88-114">This is an array of **BSTR** values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c6b88-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c6b88-115">Error codes</span></span>



| <span data-ttu-id="c6b88-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="c6b88-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c6b88-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c6b88-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c6b88-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c6b88-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c6b88-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c6b88-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c6b88-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c6b88-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c6b88-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c6b88-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c6b88-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c6b88-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c6b88-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c6b88-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c6b88-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c6b88-124">Requirements</span></span>



| <span data-ttu-id="c6b88-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c6b88-125">Requirement</span></span> | <span data-ttu-id="c6b88-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c6b88-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b88-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6b88-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b88-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c6b88-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6b88-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6b88-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b88-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c6b88-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c6b88-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c6b88-131">End of client support</span></span><br/>    | <span data-ttu-id="c6b88-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6b88-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c6b88-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="c6b88-133">Product</span></span><br/>                  | <span data-ttu-id="c6b88-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c6b88-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c6b88-135">Header</span><span class="sxs-lookup"><span data-stu-id="c6b88-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b88-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b88-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c6b88-137">IID</span><span class="sxs-lookup"><span data-stu-id="c6b88-137">IID</span></span><br/>                      | <span data-ttu-id="c6b88-138">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="c6b88-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c6b88-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6b88-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b88-140">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="c6b88-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

