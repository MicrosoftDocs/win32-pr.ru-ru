---
description: Содержит Рейтинг достоверности, возвращенный анализатором рукописного ввода журнала для Инкворд.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Элемент достоверности
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143474"
---
# <a name="confidence-element"></a><span data-ttu-id="bafe7-103">Элемент достоверности</span><span class="sxs-lookup"><span data-stu-id="bafe7-103">Confidence Element</span></span>

<span data-ttu-id="bafe7-104">Содержит Рейтинг достоверности, возвращенный анализатором рукописного ввода журнала для [**инкворд**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="bafe7-104">Contains the confidence rating returned by the Journal ink analyzer for the [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="bafe7-105">Определение</span><span class="sxs-lookup"><span data-stu-id="bafe7-105">Definition</span></span>

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="bafe7-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bafe7-106">Parent Elements</span></span>

[<span data-ttu-id="bafe7-107">**инкворд**</span><span class="sxs-lookup"><span data-stu-id="bafe7-107">**InkWord**</span></span>](inkword-element.md)

## <a name="values"></a><span data-ttu-id="bafe7-108">Значения</span><span class="sxs-lookup"><span data-stu-id="bafe7-108">Values</span></span>

<span data-ttu-id="bafe7-109">Допустимые значения для этого поля: "0", "1" и "2".</span><span class="sxs-lookup"><span data-stu-id="bafe7-109">Valid values for this field include "0", "1", and "2".</span></span> <span data-ttu-id="bafe7-110">0 означает высокую достоверность, 1 означает промежуточную уверенность, а 2 — низкую уверенность.</span><span class="sxs-lookup"><span data-stu-id="bafe7-110">0 indicates Strong confidence, 1 indicates Intermediate confidence, and 2 indicates Poor confidence.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bafe7-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bafe7-111">Child Elements</span></span>

<span data-ttu-id="bafe7-112">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="bafe7-112">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="bafe7-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bafe7-113">Attributes</span></span>

<span data-ttu-id="bafe7-114">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="bafe7-114">None.</span></span>

## <a name="element-information"></a><span data-ttu-id="bafe7-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bafe7-115">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="bafe7-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="bafe7-116">Element type</span></span> | <span data-ttu-id="bafe7-117">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="bafe7-117">**xs:string**</span></span>                              |
| <span data-ttu-id="bafe7-118">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bafe7-118">Namespace</span></span>    | <span data-ttu-id="bafe7-119">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="bafe7-119">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="bafe7-120">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="bafe7-120">Schema name</span></span>  | <span data-ttu-id="bafe7-121">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="bafe7-121">Journal Reader</span></span>                             |



 

 

 



