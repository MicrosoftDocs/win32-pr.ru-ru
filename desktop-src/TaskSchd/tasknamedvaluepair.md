---
title: Объект Таскнамедвалуепаир
description: Объект скрипта, который используется для создания пары "имя-значение", в которой имя связано со значением.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- планировщик задач объекта Таскнамедвалуепаир
- Планировщик задач объекта Таскнамедвалуепаир, описание
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681792"
---
# <a name="tasknamedvaluepair-object"></a><span data-ttu-id="d970c-105">Объект Таскнамедвалуепаир</span><span class="sxs-lookup"><span data-stu-id="d970c-105">TaskNamedValuePair object</span></span>

<span data-ttu-id="d970c-106">Объект скрипта, который используется для создания пары "имя-значение", в которой имя связано со значением.</span><span class="sxs-lookup"><span data-stu-id="d970c-106">Scripting object that is used to create a name-value pair in which the name is associated with the value.</span></span>

## <a name="members"></a><span data-ttu-id="d970c-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d970c-107">Members</span></span>

<span data-ttu-id="d970c-108">Объект **таскнамедвалуепаир** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d970c-108">The **TaskNamedValuePair** object has these types of members:</span></span>

-   [<span data-ttu-id="d970c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d970c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d970c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d970c-110">Properties</span></span>

<span data-ttu-id="d970c-111">Объект **таскнамедвалуепаир** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d970c-111">The **TaskNamedValuePair** object has these properties.</span></span>



| <span data-ttu-id="d970c-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="d970c-112">Property</span></span>                                             | <span data-ttu-id="d970c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d970c-113">Description</span></span>                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="d970c-114">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d970c-114">**Name**</span></span>](tasknamedvaluepair-name.md)<br/>   | <span data-ttu-id="d970c-115">Возвращает или задает имя, связанное со значением в паре "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="d970c-115">Gets or sets the name that is associated with a value in a name-value pair.</span></span><br/> |
| [<span data-ttu-id="d970c-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d970c-116">**Value**</span></span>](tasknamedvaluepair-value.md)<br/> | <span data-ttu-id="d970c-117">Возвращает или задает значение, связанное с именем в паре "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="d970c-117">Gets or sets the value that is associated with a name in a name-value pair.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d970c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d970c-118">Remarks</span></span>

<span data-ttu-id="d970c-119">При чтении или записи собственного XML-кода для задачи пара "имя-значение" указывается с помощью элемента [**валуекуериес**](taskschedulerschema-valuequeries-eventtriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="d970c-119">When reading or writing your own XML for a task, a name-value pair is specified using the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d970c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d970c-120">Requirements</span></span>



| <span data-ttu-id="d970c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d970c-121">Requirement</span></span> | <span data-ttu-id="d970c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d970c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d970c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d970c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d970c-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d970c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d970c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d970c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d970c-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d970c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d970c-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d970c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="d970c-128"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d970c-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d970c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d970c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d970c-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d970c-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d970c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d970c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d970c-132">**таскнамедвалуеколлектион**</span><span class="sxs-lookup"><span data-stu-id="d970c-132">**TaskNamedValueCollection**</span></span>](tasknamedvaluecollection.md)
</dt> </dl>

 

 





