---
description: Определяет допустимые значения для атрибута Style элемента Линелайаут.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Простой тип Линелайаутстилетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693662"
---
# <a name="linelayoutstyletype-simple-type"></a><span data-ttu-id="fe48c-103">Простой тип Линелайаутстилетипе</span><span class="sxs-lookup"><span data-stu-id="fe48c-103">LineLayoutStyleType Simple Type</span></span>

<span data-ttu-id="fe48c-104">Определяет допустимые значения для атрибута **Style** [элемента линелайаут](linelayout-element.md).</span><span class="sxs-lookup"><span data-stu-id="fe48c-104">Defines the valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md).</span></span>

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="fe48c-105">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="fe48c-105">Patterns</span></span>

<span data-ttu-id="fe48c-106">Простой тип **линелайаутстилетипе** — это строка, которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="fe48c-106">The **LineLayoutStyleType** simple type is a string that is restricted by the following pattern:</span></span>

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a><span data-ttu-id="fe48c-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe48c-107">Remarks</span></span>

<span data-ttu-id="fe48c-108">Допустимые значения атрибута **Style** [элемента линелайаут](linelayout-element.md) :</span><span class="sxs-lookup"><span data-stu-id="fe48c-108">Valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md) are:</span></span>

-   <span data-ttu-id="fe48c-109">Нет</span><span class="sxs-lookup"><span data-stu-id="fe48c-109">None</span></span>
-   <span data-ttu-id="fe48c-110">Сплошная</span><span class="sxs-lookup"><span data-stu-id="fe48c-110">Solid</span></span>
-   <span data-ttu-id="fe48c-111">Штрих</span><span class="sxs-lookup"><span data-stu-id="fe48c-111">Dash</span></span>
-   <span data-ttu-id="fe48c-112">Точки</span><span class="sxs-lookup"><span data-stu-id="fe48c-112">Dot</span></span>
-   <span data-ttu-id="fe48c-113">DashDot</span><span class="sxs-lookup"><span data-stu-id="fe48c-113">DashDot</span></span>
-   <span data-ttu-id="fe48c-114">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="fe48c-114">DashDotDot</span></span>
-   <span data-ttu-id="fe48c-115">Double</span><span class="sxs-lookup"><span data-stu-id="fe48c-115">Double</span></span>

## <a name="requirements"></a><span data-ttu-id="fe48c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fe48c-116">Requirements</span></span>



| <span data-ttu-id="fe48c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fe48c-117">Requirement</span></span> | <span data-ttu-id="fe48c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fe48c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fe48c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe48c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fe48c-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fe48c-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fe48c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe48c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fe48c-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fe48c-122">None supported</span></span><br/>                                     |



 

 




