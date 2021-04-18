---
title: Метод Иделиверйоптимизатионфиле метода stats (Deliveryoptimization. h)
description: Возвращает статистику загрузки и передачи для указанного файла.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats - метод
- Метод stats, интерфейс Иделиверйоптимизатионфиле
- Интерфейс Иделиверйоптимизатионфиле, метод метода stats
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415964"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a><span data-ttu-id="c05b9-106">Метод Иделиверйоптимизатионфиле:: stats</span><span class="sxs-lookup"><span data-stu-id="c05b9-106">IDeliveryOptimizationFile::GetStats method</span></span>

<span data-ttu-id="c05b9-107">Возвращает статистику загрузки и передачи для указанного файла.</span><span class="sxs-lookup"><span data-stu-id="c05b9-107">Returns download and upload stats for a specific file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c05b9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c05b9-108">Syntax</span></span>


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a><span data-ttu-id="c05b9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c05b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c05b9-110">*свармстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c05b9-110">*swarmStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c05b9-111">Возвращает статистику загрузки и передачи для указанного файла.</span><span class="sxs-lookup"><span data-stu-id="c05b9-111">Returns download and upload stats for a specific file.</span></span> <span data-ttu-id="c05b9-112">Дополнительные сведения см. в разделе Структура [**досвармстатс**](doswarmstats.md) .</span><span class="sxs-lookup"><span data-stu-id="c05b9-112">See the [**DOSwarmStats**](doswarmstats.md) structure for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c05b9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c05b9-113">Return value</span></span>

<span data-ttu-id="c05b9-114">Этот метод должен возвращать **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="c05b9-114">This method should return **S_OK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c05b9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c05b9-115">Requirements</span></span>



| <span data-ttu-id="c05b9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c05b9-116">Requirement</span></span> | <span data-ttu-id="c05b9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c05b9-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c05b9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c05b9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c05b9-119">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="c05b9-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c05b9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c05b9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c05b9-121">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="c05b9-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c05b9-122">Header</span><span class="sxs-lookup"><span data-stu-id="c05b9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c05b9-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c05b9-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c05b9-124">IDL</span><span class="sxs-lookup"><span data-stu-id="c05b9-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c05b9-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c05b9-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c05b9-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c05b9-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c05b9-127"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c05b9-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c05b9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c05b9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c05b9-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c05b9-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c05b9-130">IID</span><span class="sxs-lookup"><span data-stu-id="c05b9-130">IID</span></span><br/>                      | <span data-ttu-id="c05b9-131">IID_IDeliveryOptimizationFile определен как B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="c05b9-131">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c05b9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c05b9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c05b9-133">**иделиверйоптимизатионфиле**</span><span class="sxs-lookup"><span data-stu-id="c05b9-133">**IDeliveryOptimizationFile**</span></span>](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





