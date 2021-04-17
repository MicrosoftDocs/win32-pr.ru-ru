---
description: Событие Реадистатечанже отправляется при изменении свойства ReadyState элемента управления Мсвебдвд.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: реадистатечанже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537688"
---
# <a name="readystatechange"></a><span data-ttu-id="e5355-103">реадистатечанже</span><span class="sxs-lookup"><span data-stu-id="e5355-103">ReadyStateChange</span></span>

> [!Note]  
> <span data-ttu-id="e5355-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e5355-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e5355-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="e5355-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e5355-106">`ReadyStateChange`Событие отправляется при изменении свойства **ReadyState** элемента управления мсвебдвд.</span><span class="sxs-lookup"><span data-stu-id="e5355-106">The `ReadyStateChange` event is sent when the **ReadyState** property of the MSWebDVD control has changed.</span></span>

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a><span data-ttu-id="e5355-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5355-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5355-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span><span class="sxs-lookup"><span data-stu-id="e5355-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span></span>
</dt> <dd>

<span data-ttu-id="e5355-109">Указывает новое значение свойства [**ReadyState**](readystate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="e5355-109">Specifies the new value of the [**ReadyState**](readystate-property.md) property.</span></span>



| <span data-ttu-id="e5355-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e5355-110">Value</span></span> | <span data-ttu-id="e5355-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e5355-111">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="e5355-112">0</span><span class="sxs-lookup"><span data-stu-id="e5355-112">0</span></span>     | <span data-ttu-id="e5355-113">НАЗВАНИЕ READYSTATE не \_ инициализировано</span><span class="sxs-lookup"><span data-stu-id="e5355-113">READYSTATE\_UNINITIALIZED</span></span> |
| <span data-ttu-id="e5355-114">1</span><span class="sxs-lookup"><span data-stu-id="e5355-114">1</span></span>     | <span data-ttu-id="e5355-115">\_Загрузка READYSTATE</span><span class="sxs-lookup"><span data-stu-id="e5355-115">READYSTATE\_LOADING</span></span>       |
| <span data-ttu-id="e5355-116">2</span><span class="sxs-lookup"><span data-stu-id="e5355-116">2</span></span>     | <span data-ttu-id="e5355-117">READYSTATE \_ загружен</span><span class="sxs-lookup"><span data-stu-id="e5355-117">READYSTATE\_LOADED</span></span>        |
| <span data-ttu-id="e5355-118">3</span><span class="sxs-lookup"><span data-stu-id="e5355-118">3</span></span>     | <span data-ttu-id="e5355-119">READYSTATE \_ Interactive</span><span class="sxs-lookup"><span data-stu-id="e5355-119">READYSTATE\_INTERACTIVE</span></span>   |
| <span data-ttu-id="e5355-120">4</span><span class="sxs-lookup"><span data-stu-id="e5355-120">4</span></span>     | <span data-ttu-id="e5355-121">READYSTATE \_ завершен</span><span class="sxs-lookup"><span data-stu-id="e5355-121">READYSTATE\_COMPLETE</span></span>      |



 

</dd> </dl>

 

 



