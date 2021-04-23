---
title: Простой тип Рунлевелтипе
description: Определяет возможные значения для элемента RunLevel (ПринЦипалтипе).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- планировщик задач простого типа Рунлевелтипе
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672783"
---
# <a name="runleveltype-simple-type"></a><span data-ttu-id="7b768-104">Простой тип Рунлевелтипе</span><span class="sxs-lookup"><span data-stu-id="7b768-104">runLevelType Simple Type</span></span>

<span data-ttu-id="7b768-105">Определяет возможные значения для элемента [**runlevel (принЦипалтипе)**](taskschedulerschema-runlevel-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7b768-105">Defines the possible values for the [**RunLevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="7b768-106">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="7b768-106">Enumeration values</span></span>

<span data-ttu-id="7b768-107">Простой тип **рунлевелтипе** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7b768-107">The **runLevelType** simple type defines the following values.</span></span>



| <span data-ttu-id="7b768-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7b768-108">Value</span></span>            | <span data-ttu-id="7b768-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7b768-109">Description</span></span>                                               |
|------------------|-----------------------------------------------------------|
| <span data-ttu-id="7b768-110">леастпривилеже</span><span class="sxs-lookup"><span data-stu-id="7b768-110">LeastPrivilege</span></span>   | <span data-ttu-id="7b768-111">Задачи выполняются с наименьшими привилегиями (LUA).</span><span class="sxs-lookup"><span data-stu-id="7b768-111">Tasks are run with the least privileges (LUA).</span></span><br/> |
| <span data-ttu-id="7b768-112">HighestAvailable</span><span class="sxs-lookup"><span data-stu-id="7b768-112">HighestAvailable</span></span> | <span data-ttu-id="7b768-113">Задачи выполняются с самыми высокими привилегиями.</span><span class="sxs-lookup"><span data-stu-id="7b768-113">Tasks are run with the highest privileges.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="7b768-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7b768-114">Requirements</span></span>



| <span data-ttu-id="7b768-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7b768-115">Requirement</span></span> | <span data-ttu-id="7b768-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7b768-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b768-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b768-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b768-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b768-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b768-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b768-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b768-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b768-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





