---
title: Элемент Command (Ексектипе)
description: Указывает исполняемый файл или документ для запуска.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Элемент Command планировщик задач
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415952"
---
# <a name="command-exectype-element"></a><span data-ttu-id="71b08-104">Элемент Command (Ексектипе)</span><span class="sxs-lookup"><span data-stu-id="71b08-104">Command (execType) Element</span></span>

<span data-ttu-id="71b08-105">Указывает исполняемый файл или документ для запуска.</span><span class="sxs-lookup"><span data-stu-id="71b08-105">Specifies the executable file or document to be run.</span></span>

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

<span data-ttu-id="71b08-106">Элемент **Command** определяется сложным типом [**ексектипе**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="71b08-106">The **Command** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="71b08-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="71b08-107">Parent element</span></span>



| <span data-ttu-id="71b08-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="71b08-108">Element</span></span>                                                      | <span data-ttu-id="71b08-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="71b08-109">Derived from</span></span>                                                 | <span data-ttu-id="71b08-110">Описание</span><span class="sxs-lookup"><span data-stu-id="71b08-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="71b08-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="71b08-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="71b08-112">**ексектипе**</span><span class="sxs-lookup"><span data-stu-id="71b08-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="71b08-113">Указывает действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="71b08-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="71b08-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71b08-114">Remarks</span></span>

<span data-ttu-id="71b08-115">Сведения о разработке на языке C++ см. в описании [**свойства arguments объекта иексекактион**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="71b08-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="71b08-116">Сведения о разработке скриптов см. в разделе [**ексекактион. Arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="71b08-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="71b08-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="71b08-117">Examples</span></span>

<span data-ttu-id="71b08-118">Полный пример XML-кода для задачи, использующей исполняемое действие, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="71b08-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71b08-119">Требования</span><span class="sxs-lookup"><span data-stu-id="71b08-119">Requirements</span></span>



| <span data-ttu-id="71b08-120">Требование</span><span class="sxs-lookup"><span data-stu-id="71b08-120">Requirement</span></span> | <span data-ttu-id="71b08-121">Значение</span><span class="sxs-lookup"><span data-stu-id="71b08-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="71b08-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71b08-122">Minimum supported client</span></span><br/> | <span data-ttu-id="71b08-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71b08-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="71b08-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71b08-124">Minimum supported server</span></span><br/> | <span data-ttu-id="71b08-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71b08-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71b08-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71b08-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b08-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="71b08-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





