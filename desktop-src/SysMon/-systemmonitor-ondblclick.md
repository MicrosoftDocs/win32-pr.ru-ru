---
title: Системмонитор. Ондблкликк, событие
description: Уведомляет вас, когда пользователь дважды щелкает линию графа, гистограмму или элемент отчета с помощью левой кнопки мыши.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Сисмон события Ондблкликк
- Ондблкликк Event Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, событие Ондблкликк
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136003"
---
# <a name="systemmonitorondblclick-event"></a><span data-ttu-id="82af7-106">Системмонитор. Ондблкликк, событие</span><span class="sxs-lookup"><span data-stu-id="82af7-106">SystemMonitor.OnDblClick event</span></span>

<span data-ttu-id="82af7-107">Уведомляет вас, когда пользователь дважды щелкает линию графа, гистограмму или элемент отчета с помощью левой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="82af7-107">Notifies you when a user double-clicks the graph line, histogram bar, or report item with the left mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="82af7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82af7-108">Syntax</span></span>


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="82af7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="82af7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82af7-110">*индекс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="82af7-110">*index* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="82af7-111">Индекс выбранного счетчика в объекте коллекции [**счетчиков**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="82af7-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span> <span data-ttu-id="82af7-112">Если счетчик не выбран, возвращается значение индекса 0. в противном случае возвращается индекс выбранного счетчика.</span><span class="sxs-lookup"><span data-stu-id="82af7-112">An index value of 0 is returned if no counter was selected; otherwise, the index of the selected counter is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82af7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82af7-113">Return value</span></span>

<span data-ttu-id="82af7-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="82af7-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82af7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82af7-115">Remarks</span></span>

<span data-ttu-id="82af7-116">При срабатывании этого события счетчик, выбранный пользователем в линейном графике и гистограмме, также выбирается в области условные обозначения.</span><span class="sxs-lookup"><span data-stu-id="82af7-116">When this event is triggered, the counter that the user selected in the line graph and histogram is also selected in the Legend pane.</span></span> <span data-ttu-id="82af7-117">Это упрощает пользователю системного монитора, какой счетчик выбран при отображении нескольких значений счетчиков.</span><span class="sxs-lookup"><span data-stu-id="82af7-117">This makes it easier for the user of the System Monitor to see which counter is selected when several counter values are displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="82af7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="82af7-118">Requirements</span></span>



| <span data-ttu-id="82af7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="82af7-119">Requirement</span></span> | <span data-ttu-id="82af7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="82af7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82af7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82af7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="82af7-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82af7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="82af7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82af7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="82af7-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82af7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82af7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="82af7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82af7-126"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="82af7-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





