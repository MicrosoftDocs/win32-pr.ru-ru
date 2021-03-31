---
title: Системмонитор. Датапоинткаунт, свойство
description: Возвращает или задает количество точек данных, отображаемых в линейном графе.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Сисмон свойство Датапоинткаунт
- Свойство Датапоинткаунт Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, свойство Датапоинткаунт
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988426"
---
# <a name="systemmonitordatapointcount-property"></a><span data-ttu-id="199de-106">Системмонитор. Датапоинткаунт, свойство</span><span class="sxs-lookup"><span data-stu-id="199de-106">SystemMonitor.DataPointCount property</span></span>

<span data-ttu-id="199de-107">Возвращает или задает количество точек данных, отображаемых в линейном графе.</span><span class="sxs-lookup"><span data-stu-id="199de-107">Retrieves or sets the number of data points displayed in a line graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="199de-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="199de-108">Syntax</span></span>


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a><span data-ttu-id="199de-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="199de-109">Property value</span></span>

<span data-ttu-id="199de-110">Количество точек данных, отображаемых в представлении для линейного графика.</span><span class="sxs-lookup"><span data-stu-id="199de-110">Number of data points displayed in the view for a line graph.</span></span> <span data-ttu-id="199de-111">Значение по умолчанию — 100 точек данных.</span><span class="sxs-lookup"><span data-stu-id="199de-111">The default value is 100 data points.</span></span> <span data-ttu-id="199de-112">Допустимый диапазон значений: от 2 до 1 000.</span><span class="sxs-lookup"><span data-stu-id="199de-112">The valid range of values is 2 to 1,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="199de-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="199de-113">Remarks</span></span>

<span data-ttu-id="199de-114">Это свойство используется только в том случае, если [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) является **сисмонкуррентактивити**.</span><span class="sxs-lookup"><span data-stu-id="199de-114">This property is used only if [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is **sysmonCurrentActivity**.</span></span>

## <a name="requirements"></a><span data-ttu-id="199de-115">Требования</span><span class="sxs-lookup"><span data-stu-id="199de-115">Requirements</span></span>



| <span data-ttu-id="199de-116">Требование</span><span class="sxs-lookup"><span data-stu-id="199de-116">Requirement</span></span> | <span data-ttu-id="199de-117">Значение</span><span class="sxs-lookup"><span data-stu-id="199de-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="199de-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="199de-118">Minimum supported client</span></span><br/> | <span data-ttu-id="199de-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="199de-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="199de-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="199de-120">Minimum supported server</span></span><br/> | <span data-ttu-id="199de-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="199de-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="199de-122">DLL</span><span class="sxs-lookup"><span data-stu-id="199de-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="199de-123"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="199de-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





