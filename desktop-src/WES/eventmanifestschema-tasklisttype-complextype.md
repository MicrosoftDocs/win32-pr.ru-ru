---
title: Сложный тип Тасклисттипе
description: Определяет список задач, которые используются для определения компонентов приложения.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- Журнал событий сложных типов Тасклисттипе
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414681"
---
# <a name="tasklisttype-complex-type"></a><span data-ttu-id="bb1d6-104">Сложный тип Тасклисттипе</span><span class="sxs-lookup"><span data-stu-id="bb1d6-104">TaskListType Complex Type</span></span>

<span data-ttu-id="bb1d6-105">Определяет список задач, которые используются для определения компонентов приложения.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-105">Defines a list of tasks that are used to identify the components of an application.</span></span>

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="bb1d6-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bb1d6-106">Child elements</span></span>



| <span data-ttu-id="bb1d6-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="bb1d6-107">Element</span></span>                                                       | <span data-ttu-id="bb1d6-108">Тип</span><span class="sxs-lookup"><span data-stu-id="bb1d6-108">Type</span></span>                                                         | <span data-ttu-id="bb1d6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bb1d6-109">Description</span></span>                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="bb1d6-110">**задачи**</span><span class="sxs-lookup"><span data-stu-id="bb1d6-110">**task**</span></span>](eventmanifestschema-task-tasklisttype-element.md) | [<span data-ttu-id="bb1d6-111">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="bb1d6-111">**TaskType**</span></span>](eventmanifestschema-tasktype-complextype.md) | <span data-ttu-id="bb1d6-112">Определяет компонент или подкомпонент приложения.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-112">Defines a component or subcomponent of an application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bb1d6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bb1d6-113">Requirements</span></span>



| <span data-ttu-id="bb1d6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bb1d6-114">Requirement</span></span> | <span data-ttu-id="bb1d6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bb1d6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb1d6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb1d6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bb1d6-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb1d6-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb1d6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb1d6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bb1d6-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb1d6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





