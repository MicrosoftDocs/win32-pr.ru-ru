---
title: IWMPEvents4 Синцестиматионкомплете, метод
description: Событие Синцестиматионкомплете возникает при завершении оценки размера, ранее инициированной IWMPSyncDevice3 Естиматесинксизе.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Синцестиматионкомплете метод Windows Media Player
- Синцестиматионкомплете метод проигрывателя Windows Media Player, интерфейс IWMPEvents4
- Интерфейс IWMPEvents4 Windows Media Player, метод Синцестиматионкомплете
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788677"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a><span data-ttu-id="e0997-106">Метод IWMPEvents4:: Синцестиматионкомплете</span><span class="sxs-lookup"><span data-stu-id="e0997-106">IWMPEvents4::SyncEstimationComplete method</span></span>

<span data-ttu-id="e0997-107">Событие **синцестиматионкомплете** возникает при завершении оценки размера, которая ранее была инициирована [**IWMPSyncDevice3:: естиматесинксизе**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize).</span><span class="sxs-lookup"><span data-stu-id="e0997-107">The **SyncEstimationComplete** event occurs when a size estimation, previously initiated by [**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0997-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0997-108">Syntax</span></span>


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a><span data-ttu-id="e0997-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0997-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0997-110">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0997-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0997-111">Указатель на интерфейс [**ивмпсинкдевице**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) , представляющий устройство, для которого была инициирована оценка размера.</span><span class="sxs-lookup"><span data-stu-id="e0997-111">Pointer to the [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) interface that represents the device for which the size estimation was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="e0997-112">*хрресулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0997-112">*hrResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0997-113">Значение, указывающее на успешное или неуспешное выполнение оценки.</span><span class="sxs-lookup"><span data-stu-id="e0997-113">A value that indicates the success or failure of the estimation.</span></span>



| <span data-ttu-id="e0997-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e0997-114">Value</span></span>                                                                                                                                       | <span data-ttu-id="e0997-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e0997-115">Meaning</span></span>                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="e0997-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e0997-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e0997-117">Оценка прошла удачно.</span><span class="sxs-lookup"><span data-stu-id="e0997-117">The estimation succeeded.</span></span><br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <span data-ttu-id="e0997-118"><dt>**\_прервать**</dt></span><span class="sxs-lookup"><span data-stu-id="e0997-118"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="e0997-119">Оценка была прервана.</span><span class="sxs-lookup"><span data-stu-id="e0997-119">The estimation was aborted.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e0997-120">*лестиматедуседспаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0997-120">*lEstimatedUsedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0997-121">Предполагаемое пространство (в байтах), которое будет использоваться на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e0997-121">The estimated space (in bytes) that would be used on the device.</span></span>

</dd> <dt>

<span data-ttu-id="e0997-122">*лестиматедсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0997-122">*lEstimatedSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0997-123">Предполагаемый размер (в байтах) синхронизируемых данных.</span><span class="sxs-lookup"><span data-stu-id="e0997-123">The estimated size (in bytes) of the data to be synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0997-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0997-124">Return value</span></span>

<span data-ttu-id="e0997-125">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e0997-125">This method does not return a value.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0997-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0997-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0997-127">**Интерфейс IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="e0997-127">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[<span data-ttu-id="e0997-128">**IWMPSyncDevice3:: Естиматесинксизе**</span><span class="sxs-lookup"><span data-stu-id="e0997-128">**IWMPSyncDevice3::estimateSyncSize**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





