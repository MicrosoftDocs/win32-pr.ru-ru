---
description: Свойство Дисаблеаутомаусепроцессинг включает или отключает функцию обработки мыши объекта Мсвебдвд.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Дисаблеаутомаусепроцессинг, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494397"
---
# <a name="disableautomouseprocessing-property"></a><span data-ttu-id="79575-103">Дисаблеаутомаусепроцессинг, свойство</span><span class="sxs-lookup"><span data-stu-id="79575-103">DisableAutoMouseProcessing Property</span></span>

> [!Note]  
> <span data-ttu-id="79575-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="79575-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="79575-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="79575-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="79575-106">`DisableAutoMouseProcessing`Свойство включает или отключает функцию обработки мыши объекта **мсвебдвд** .</span><span class="sxs-lookup"><span data-stu-id="79575-106">The `DisableAutoMouseProcessing` property enables or disables the **MSWebDVD** object's mouse-processing functionality.</span></span>

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a><span data-ttu-id="79575-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79575-107">Return Value</span></span>

<span data-ttu-id="79575-108">Возвращает логическое значение, указывающее, следует ли отключать обработку мыши по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79575-108">Returns a boolean value indicating whether to disable the default mouse processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="79575-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79575-109">Remarks</span></span>

<span data-ttu-id="79575-110">Это свойство доступно для чтения и записи со значением по умолчанию false.</span><span class="sxs-lookup"><span data-stu-id="79575-110">This property is read/write with a default value of false.</span></span> <span data-ttu-id="79575-111">Объект **мсвебдвд** автоматически обрабатывает действия мыши для экранных меню на DVD-диске по умолчанию. Пользователи могут выделять и активировать кнопки меню без специального программирования приложением.</span><span class="sxs-lookup"><span data-stu-id="79575-111">The **MSWebDVD** object automatically handles mouse actions for DVD on-screen menus by default; users can highlight and activate menu buttons without special programming by the application.</span></span> <span data-ttu-id="79575-112">Приложение может отключить эту функцию обработки мыши по умолчанию, задав этому свойству **значение true**.</span><span class="sxs-lookup"><span data-stu-id="79575-112">An application can turn off this default mouse-handling functionality by setting this property to **true**.</span></span> <span data-ttu-id="79575-113">Если автоматическая обработка мыши отключена, приложение должно использовать различные методы и свойства, связанные с кнопками, для обработки перемещений мыши и щелчков мышью в контекстных меню.</span><span class="sxs-lookup"><span data-stu-id="79575-113">When the automatic mouse processing is turned off, an application must use the various button-related methods and properties to handle mouse moves and mouse clicks on the on-screen menus.</span></span> <span data-ttu-id="79575-114">Кроме того, приложение может использовать методы, связанные с кнопками, для переопределения автоматической обработки мыши, даже если параметр `DisableAutoMouseProcessing` имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="79575-114">Also, an application can use the button-related methods to override the automatic mouse handling even when when `DisableAutoMouseProcessing` is set to **false**.</span></span>

 

 



