---
title: Каунтеритем. Selected, свойство
description: Возвращает или задает значение, указывающее, выбран ли счетчик.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Выбранное свойство Сисмон
- Выбранное свойство Сисмон, объект Каунтеритем
- Объект Сисмон, выбранное свойство Каунтеритем
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988758"
---
# <a name="counteritemselected-property"></a><span data-ttu-id="def44-106">Каунтеритем. Selected, свойство</span><span class="sxs-lookup"><span data-stu-id="def44-106">CounterItem.Selected property</span></span>

<span data-ttu-id="def44-107">Возвращает или задает значение, указывающее, выбран ли счетчик.</span><span class="sxs-lookup"><span data-stu-id="def44-107">Retrieves or sets a value that indicates if the counter is selected.</span></span>

<span data-ttu-id="def44-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="def44-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="def44-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="def44-109">Syntax</span></span>


```VB
Property Selected As Boolean
```



## <a name="property-value"></a><span data-ttu-id="def44-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="def44-110">Property value</span></span>

<span data-ttu-id="def44-111">Значение true, если счетчик выбран. в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="def44-111">True if the counter is selected; otherwise, false.</span></span>

## <a name="remarks"></a><span data-ttu-id="def44-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="def44-112">Remarks</span></span>

<span data-ttu-id="def44-113">Можно выбрать один или несколько счетчиков из коллекции счетчиков.</span><span class="sxs-lookup"><span data-stu-id="def44-113">You can select one or more counters from the collection of counters.</span></span> <span data-ttu-id="def44-114">Выбор счетчика, выбор счетчика в условных обозначениях, делает счетчик видимым в условных обозначениях и создает событие [**онкаунтерселектед**](-systemmonitor-oncounterselected.md) .</span><span class="sxs-lookup"><span data-stu-id="def44-114">Selecting a counter, selects the counter in the Legend, makes the counter visible in the Legend, and generates an [**OnCounterSelected**](-systemmonitor-oncounterselected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="def44-115">Требования</span><span class="sxs-lookup"><span data-stu-id="def44-115">Requirements</span></span>



| <span data-ttu-id="def44-116">Требование</span><span class="sxs-lookup"><span data-stu-id="def44-116">Requirement</span></span> | <span data-ttu-id="def44-117">Значение</span><span class="sxs-lookup"><span data-stu-id="def44-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="def44-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="def44-118">Minimum supported client</span></span><br/> | <span data-ttu-id="def44-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="def44-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="def44-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="def44-120">Minimum supported server</span></span><br/> | <span data-ttu-id="def44-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="def44-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="def44-122">DLL</span><span class="sxs-lookup"><span data-stu-id="def44-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="def44-123"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="def44-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def44-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="def44-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def44-125">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="def44-125">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





