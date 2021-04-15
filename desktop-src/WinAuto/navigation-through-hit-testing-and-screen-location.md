---
title: Навигация с помощью проверки попадания и расположения на экране
description: Чтобы найти дочерний объект или определить размер объекта, клиенты могут попасть на тестовые точки на экране.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654231"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a><span data-ttu-id="143f0-103">Навигация с помощью проверки попадания и расположения на экране</span><span class="sxs-lookup"><span data-stu-id="143f0-103">Navigation Through Hit Testing and Screen Location</span></span>

<span data-ttu-id="143f0-104">Чтобы найти дочерний объект или определить размер объекта, клиенты могут попасть на тестовые точки на экране.</span><span class="sxs-lookup"><span data-stu-id="143f0-104">To locate an object's children or to determine an object's size, clients can hit test points on the screen.</span></span> <span data-ttu-id="143f0-105">Доступны два метода:</span><span class="sxs-lookup"><span data-stu-id="143f0-105">Two methods are available:</span></span>

-   [<span data-ttu-id="143f0-106">**IAccessible:: Акчиттест**</span><span class="sxs-lookup"><span data-stu-id="143f0-106">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="143f0-107">**IAccessible:: Акклокатион**</span><span class="sxs-lookup"><span data-stu-id="143f0-107">**IAccessible::accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a><span data-ttu-id="143f0-108">Использование метода IAccessible:: Акчиттест</span><span class="sxs-lookup"><span data-stu-id="143f0-108">Using IAccessible::accHitTest</span></span>

<span data-ttu-id="143f0-109">Чтобы определить, находится ли точка внутри объекта, внутри его дочернего элемента или ни одного, клиенты вызывают метод [**IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) родительского объекта, передавая экранные координаты точки для проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="143f0-109">To identify whether a point is within an object, within its child, or neither, clients call the [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) method of the parent object, passing the screen coordinates of the point to be hit tested.</span></span> <span data-ttu-id="143f0-110">В следующем списке описаны некоторые типичные сценарии.</span><span class="sxs-lookup"><span data-stu-id="143f0-110">The following list describes some typical scenarios:</span></span>

-   <span data-ttu-id="143f0-111">Если дочерние элементы объекта перекрываются в заданной точке, [**IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) извлекает самый верхний дочерний элемент, который визуально занимает пространство.</span><span class="sxs-lookup"><span data-stu-id="143f0-111">If the object's children overlap at a specified point, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) retrieves the topmost child that visually appears to occupy the space.</span></span>
-   <span data-ttu-id="143f0-112">Если окно охватывает дочерний элемент или если дочерний элемент обрезается родительским элементом, проверка попадания в охватываемую точку получает дочерний элемент, даже если он не виден.</span><span class="sxs-lookup"><span data-stu-id="143f0-112">If a window covers a child, or if the child is clipped by the parent, hit testing the covered point retrieves the child even though it is not visible.</span></span>
-   <span data-ttu-id="143f0-113">Если дочерний элемент, найденный в указанной точке, является доступным объектом, а не дочерним элементом, метод возвращает интерфейс [**IDispatch**](idispatch-interface.md) дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="143f0-113">If the child found at the specified point is an accessible object, as opposed to a child element, the method returns the child's [**IDispatch**](idispatch-interface.md) interface.</span></span>

## <a name="using-iaccessibleacclocation"></a><span data-ttu-id="143f0-114">Использование метода IAccessible:: Акклокатион</span><span class="sxs-lookup"><span data-stu-id="143f0-114">Using IAccessible::accLocation</span></span>

<span data-ttu-id="143f0-115">Чтобы получить расположение экрана объекта или одного из его дочерних объектов, клиенты вызывают метод [**IAccessible:: акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span><span class="sxs-lookup"><span data-stu-id="143f0-115">To get the screen location of an object or one of the object's children, clients call [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span></span> <span data-ttu-id="143f0-116">Этот метод возвращает координаты ограничивающего прямоугольника указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="143f0-116">This method returns the coordinates of the specified object's bounding rectangle.</span></span> <span data-ttu-id="143f0-117">Если объект не похож на форму прямоугольника, метод возвращает координаты самого маленького прямоугольника, охватывающего весь объект.</span><span class="sxs-lookup"><span data-stu-id="143f0-117">If the object is not shaped like a rectangle, the method returns the coordinates of the smallest rectangle that encompasses the entire object.</span></span>

<span data-ttu-id="143f0-118">На следующем рисунке показана связь между областью не прямоугольного объекта и ограничивающим его прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="143f0-118">The following illustration shows the relationship between a non-rectangular object's region and its bounding rectangle.</span></span>

![Иллюстрация, демонстрирующая область непрямоугольного объекта (окружность) и его ограничивающий прямоугольник.](images/region.gif)

> [!Note]  
> <span data-ttu-id="143f0-120">[**IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) является более точным, чем [**IAccessible:: акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , так как позволяет клиентам определять расположение объектов на попикселном уровне, а не в ограничивающих прямоугольниках.</span><span class="sxs-lookup"><span data-stu-id="143f0-120">[**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) is more precise than [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because it enables clients to determine the location of objects on a pixel-by-pixel basis rather than with bounding rectangles.</span></span> <span data-ttu-id="143f0-121">Такая точность полезна, например, при сборе данных приложением путем отслеживания расположения указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="143f0-121">This precision is useful, for example, when an application is gathering information by tracking the location of the mouse pointer.</span></span>

 

 

 




