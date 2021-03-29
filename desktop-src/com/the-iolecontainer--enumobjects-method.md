---
title: Метод Иолеконтаинер Енумобжектс
description: Метод Иолеконтаинер Енумобжектс
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252859"
---
# <a name="the-iolecontainerenumobjects-method"></a><span data-ttu-id="7ef00-103">Метод Иолеконтаинер:: Енумобжектс</span><span class="sxs-lookup"><span data-stu-id="7ef00-103">The IOleContainer::EnumObjects Method</span></span>

<span data-ttu-id="7ef00-104">Этот метод используется для перечисления всех объектов OLE, содержащихся в документе или форме, возвращающего указатель интерфейса для каждого объекта OLE.</span><span class="sxs-lookup"><span data-stu-id="7ef00-104">This method is used to enumerate over all the OLE objects contained in a document or form, returning an interface pointer for each OLE object.</span></span> <span data-ttu-id="7ef00-105">Контейнер должен возвращать указатели на каждый объект OLE, совместно использующий один и тот же контейнер.</span><span class="sxs-lookup"><span data-stu-id="7ef00-105">The container must return pointers to each OLE object that shares the same container.</span></span> <span data-ttu-id="7ef00-106">Вложенные формы и вложенные элементы управления также должны быть перечислены.</span><span class="sxs-lookup"><span data-stu-id="7ef00-106">Nested forms or nested controls must also be enumerated.</span></span>

<span data-ttu-id="7ef00-107">Некоторые контейнеры реализуют расширяющие элементы управления, которые заключают элементы управления, не относящиеся к ActiveX, а затем возвращают указатели на эти элементы управления расширителем при перечислении формы.</span><span class="sxs-lookup"><span data-stu-id="7ef00-107">Some containers implement extender controls, which wrap non-ActiveX controls, and then return pointers to these extender controls as a form is enumerated.</span></span> <span data-ttu-id="7ef00-108">Это поведение позволяет элементам управления ActiveX и контейнерам элементов управления ActiveX хорошо интегрироваться с элементами управления, отличными от ActiveX, и поэтому рекомендуется, но не обязательно.</span><span class="sxs-lookup"><span data-stu-id="7ef00-108">This behavior enables ActiveX controls and ActiveX control containers to integrate well with non-ActiveX controls, and is thus recommended, but not required.</span></span>

 

 




