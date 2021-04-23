---
title: Рекомендации по проектированию прокси-объектов
description: Проектирование объектов прокси и специальных возможностей зависит от структуры элементов пользовательского интерфейса сервера. Независимо от проекта элемент пользовательского интерфейса должен уведомлять свой прокси-объект до его уничтожения, чтобы объект прокси-сервера обрабатывал вызовы от клиентов соответствующим образом.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067562"
---
# <a name="design-considerations-for-proxy-objects"></a><span data-ttu-id="1f7e5-104">Рекомендации по проектированию прокси-объектов</span><span class="sxs-lookup"><span data-stu-id="1f7e5-104">Design Considerations for Proxy Objects</span></span>

<span data-ttu-id="1f7e5-105">Проектирование объектов прокси и специальных возможностей зависит от структуры элементов пользовательского интерфейса сервера.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-105">Proxy and accessible object design depends on the design of the server UI elements.</span></span> <span data-ttu-id="1f7e5-106">Независимо от проекта элемент пользовательского интерфейса должен уведомлять свой прокси-объект до его уничтожения, чтобы объект прокси-сервера обрабатывал вызовы от клиентов соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-106">Regardless of the design, a UI element must notify its proxy object right before it is destroyed so that the proxy object handles calls from clients appropriately.</span></span>

<span data-ttu-id="1f7e5-107">В следующем списке описаны две возможности проектирования:</span><span class="sxs-lookup"><span data-stu-id="1f7e5-107">The following list describes two design possibilities:</span></span>

-   <span data-ttu-id="1f7e5-108">Поместите код, реализующий интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , в тот же модуль, что и код, реализующий элемент пользовательского интерфейса, если код пользовательского интерфейса легко расширяем.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-108">Place the code that implements the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface in the same module as the code that implements the user interface element if the user interface code is easily extensible.</span></span> <span data-ttu-id="1f7e5-109">В этом случае прокси-сервер «упрощен» в том смысле, что все они отслеживают жизненный цикл доступного объекта, перенаправляют вызовы к доступному объекту и возвращают результаты.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-109">In this case, the proxy is "lightweight" in the sense that all it does is monitor the life span of the accessible object, forward calls to the accessible object, and return the results.</span></span>
-   <span data-ttu-id="1f7e5-110">Поместите код, реализующий метод [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , в тот же модуль, что и код, реализующий прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-110">Place the code that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in the same module as the code that implements the proxy object.</span></span> <span data-ttu-id="1f7e5-111">В этом случае доступный объект использует внутренние функции для получения сведений об элементе пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-111">In this case, the accessible object uses internal functions to obtain information about the UI element.</span></span>

## <a name="trackbar-controls"></a><span data-ttu-id="1f7e5-112">Элементы управления TrackBar</span><span class="sxs-lookup"><span data-stu-id="1f7e5-112">Trackbar Controls</span></span>

<span data-ttu-id="1f7e5-113">При реализации элементов управления TrackBar используйте для **изменения стиля TrackBar \_ , чтобы** предоставить более значимую информацию.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-113">When implementing trackbar controls, use the trackbar style **TBS\_REVERSED** to provide more meaningful information.</span></span> <span data-ttu-id="1f7e5-114">Этот стиль меняет масштаб, используемый методом [**IAccessible:: Get \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="1f7e5-114">This style reverses the scale used by [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="1f7e5-115">Для вертикальных линейки прокрутки без этого стиля метод [**IAccessible:: Get \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) возвращает ноль (0), если ползунок TrackBar находится в верхней части элемента управления; значения увеличиваются по мере прокрутки бегунка к концу.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-115">For vertical trackbars without this style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns zero (0) when the trackbar thumb is at the top of the control; the values increase as you slide the thumb toward the bottom.</span></span> <span data-ttu-id="1f7e5-116">При **\_ обращении к TBS** , метод **IAccessible:: Get \_ акквалуе** возвращает 100 (100), когда бегунок линейки находится вверху; числа уменьшаются по мере перемещения ползунка TrackBar в нижнюю сторону.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-116">With the **TBS\_REVERSED** style, **IAccessible::get\_accValue** returns one hundred (100) when the trackbar thumb is at the top; the numbers decrease as you move the trackbar thumb toward the bottom.</span></span>

<span data-ttu-id="1f7e5-117">Для горизонтальных значений TrackBar без этого стиля возвращается ноль (0), если ползунок TrackBar находится в левом конце элемента управления. значения увеличиваются при перемещении бегунка TrackBar вправо.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-117">For horizontal trackbars without this style, zero (0) is returned when the trackbar thumb is at the left end of the control; the values increase as you move the trackbar thumb to the right.</span></span> <span data-ttu-id="1f7e5-118">При **\_ обращении к TBS** , метод [**IAccessible:: Get \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) возвращает 100 (100), когда ползунок TrackBar находится слева; значения уменьшаются по мере перемещения бегунка TrackBar вправо.</span><span class="sxs-lookup"><span data-stu-id="1f7e5-118">With the **TBS\_REVERSED** style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns one hundred (100) when the trackbar thumb is at the left; the values decrease as you move the trackbar thumb to the right.</span></span>

 

 




