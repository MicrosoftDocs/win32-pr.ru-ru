---
title: WorkingDirectory (Ексектипе), элемент
description: Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- планировщик задач элемента WorkingDirectory
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682126"
---
# <a name="workingdirectory-exectype-element"></a><span data-ttu-id="3eed6-104">WorkingDirectory (Ексектипе), элемент</span><span class="sxs-lookup"><span data-stu-id="3eed6-104">WorkingDirectory (execType) Element</span></span>

<span data-ttu-id="3eed6-105">Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.</span><span class="sxs-lookup"><span data-stu-id="3eed6-105">Specifies the directory where either the executable or those files used by the executable exists.</span></span>

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

<span data-ttu-id="3eed6-106">Элемент **WorkingDirectory** определяется сложным типом [**ексектипе**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3eed6-106">The **WorkingDirectory** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3eed6-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="3eed6-107">Parent element</span></span>



| <span data-ttu-id="3eed6-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="3eed6-108">Element</span></span>                                                      | <span data-ttu-id="3eed6-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="3eed6-109">Derived from</span></span>                                                 | <span data-ttu-id="3eed6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3eed6-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="3eed6-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="3eed6-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="3eed6-112">**ексектипе**</span><span class="sxs-lookup"><span data-stu-id="3eed6-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="3eed6-113">Указывает действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="3eed6-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3eed6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3eed6-114">Remarks</span></span>

<span data-ttu-id="3eed6-115">Для разработки скриптов рабочий каталог указывается свойством [**ексекактион. WorkingDirectory**](execaction-workingdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="3eed6-115">For script development, the working directory is specified by the [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md) property.</span></span>

<span data-ttu-id="3eed6-116">Для разработки на C++ рабочий каталог определяется свойством [**иексекактион:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .</span><span class="sxs-lookup"><span data-stu-id="3eed6-116">For C++ development, the working directory is specified by the [**IExecAction::WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) property.</span></span>

## <a name="examples"></a><span data-ttu-id="3eed6-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="3eed6-117">Examples</span></span>

<span data-ttu-id="3eed6-118">В следующем коде XML определяется действие выполнения.</span><span class="sxs-lookup"><span data-stu-id="3eed6-118">The following XML defines a execution action.</span></span>


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a><span data-ttu-id="3eed6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3eed6-119">Requirements</span></span>



| <span data-ttu-id="3eed6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3eed6-120">Requirement</span></span> | <span data-ttu-id="3eed6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3eed6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3eed6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3eed6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3eed6-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3eed6-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3eed6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3eed6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3eed6-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3eed6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3eed6-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3eed6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eed6-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="3eed6-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3eed6-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="3eed6-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





