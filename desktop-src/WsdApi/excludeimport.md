---
description: 'Предотвращает создание операторов импорта для указанных целевых объектов с именем в элементе WSDL: Import в WSDL-файле.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: Ексклудеимпорт, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf511a24ad4007deb886900843991364fcf03a5a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380778"
---
# <a name="excludeimport-element"></a><span data-ttu-id="dbcb0-103">Ексклудеимпорт, элемент</span><span class="sxs-lookup"><span data-stu-id="dbcb0-103">excludeImport element</span></span>

<span data-ttu-id="dbcb0-104">Предотвращает создание операторов импорта для указанных целевых объектов в \<wsdl:import> ЭЛЕМЕНТЕ WSDL-файла.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="dbcb0-105">Это можно использовать для того, чтобы Всдкодежен импортировать хорошо известные целевые объекты, такие как спецификации WS-Addressing и WS-Eventing, несмотря на то, что на эти целевые объекты ссылаются в WSDL.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="dbcb0-106">Значение этого элемента должно быть задано для пространства имен, указанного в \<wsdl:import> элементе, который необходимо исключить.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="dbcb0-107">Использование</span><span class="sxs-lookup"><span data-stu-id="dbcb0-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="dbcb0-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="dbcb0-108">Attributes</span></span>

<span data-ttu-id="dbcb0-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="dbcb0-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dbcb0-110">Child elements</span></span>

<span data-ttu-id="dbcb0-111">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="dbcb0-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="dbcb0-112">Parent elements</span></span>



| <span data-ttu-id="dbcb0-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="dbcb0-113">Element</span></span>                         | <span data-ttu-id="dbcb0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="dbcb0-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="dbcb0-115">**файле**</span><span class="sxs-lookup"><span data-stu-id="dbcb0-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="dbcb0-116">Указывает WSDL-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="dbcb0-117">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dbcb0-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="dbcb0-118">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="dbcb0-118">Minimum supported system</span></span><br/> | <span data-ttu-id="dbcb0-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbcb0-119">Windows Vista</span></span> |
| <span data-ttu-id="dbcb0-120">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="dbcb0-120">Can be empty</span></span>                        | <span data-ttu-id="dbcb0-121">Да</span><span class="sxs-lookup"><span data-stu-id="dbcb0-121">Yes</span></span>           |



 

 




