---
title: Использование OBJID \_ нативеом для предоставления собственного интерфейса для окна
description: Этот метод позволяет клиентам получить пользовательский объект для окна. Серверы могут использовать его для предоставления указателя на пользовательский объект документа для окна.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2c5c6ec194ca643475444feb5839c02d3fa890
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "104412110"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a><span data-ttu-id="b3d80-104">Использование OBJID \_ нативеом для предоставления собственного интерфейса для окна</span><span class="sxs-lookup"><span data-stu-id="b3d80-104">Use OBJID\_NATIVEOM to expose a native interface for a window</span></span>

<span data-ttu-id="b3d80-105">Этот метод позволяет клиентам получить пользовательский объект для окна.</span><span class="sxs-lookup"><span data-stu-id="b3d80-105">This technique allows clients to get a custom object for a window.</span></span> <span data-ttu-id="b3d80-106">Серверы могут использовать его для предоставления указателя на пользовательский объект документа для окна.</span><span class="sxs-lookup"><span data-stu-id="b3d80-106">Servers can use this to expose a pointer to a custom document object for a window.</span></span>

<span data-ttu-id="b3d80-107">**Предоставление собственного интерфейса объектной модели для окна (серверы)**</span><span class="sxs-lookup"><span data-stu-id="b3d80-107">**To expose a native object model interface for a window (servers)**</span></span>

1.  <span data-ttu-id="b3d80-108">Обработайте сообщение [**WM \_ GetObject**](wm-getobject.md) в процедуре окна.</span><span class="sxs-lookup"><span data-stu-id="b3d80-108">Handle the [**WM\_GETOBJECT**](wm-getobject.md) message in the window procedure.</span></span> <span data-ttu-id="b3d80-109">Если значение *lParam* — [**OBJID \_ нативеом**](object-identifiers.md), то возвращается указатель интерфейса на пользовательский объект с помощью [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="b3d80-109">When the *lParam* value is [**OBJID\_NATIVEOM**](object-identifiers.md), return an interface pointer to the custom object using [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span>
2.  <span data-ttu-id="b3d80-110">При необходимости освободите указатель интерфейса после вызова [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="b3d80-110">Release your interface pointer after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), if appropriate.</span></span> <span data-ttu-id="b3d80-111">Дополнительные сведения см. в разделе **функции lresultfromobject**.</span><span class="sxs-lookup"><span data-stu-id="b3d80-111">For more information, see **LresultFromObject**.</span></span>

<span data-ttu-id="b3d80-112">Клиенты могут получить указатель на этот пользовательский объект.</span><span class="sxs-lookup"><span data-stu-id="b3d80-112">Clients can obtain a pointer to this custom object.</span></span>

<span data-ttu-id="b3d80-113">**Получение указателя на пользовательский объект для окна (клиенты)**</span><span class="sxs-lookup"><span data-stu-id="b3d80-113">**To obtain a pointer for a custom object for a window (clients)**</span></span>

-   <span data-ttu-id="b3d80-114">Вызовите [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) и передайте [**OBJID \_ нативеом**](object-identifiers.md) в качестве второго параметра.</span><span class="sxs-lookup"><span data-stu-id="b3d80-114">Call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and pass [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

<span data-ttu-id="b3d80-115">Обратите внимание на следующие вопросы для этого метода:</span><span class="sxs-lookup"><span data-stu-id="b3d80-115">Note the following issues for this technique:</span></span>

-   <span data-ttu-id="b3d80-116">Этот метод аналогичен возврату указателя интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , за исключением того, что используется идентификатор объекта, и тот факт, что [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) возвращает пользовательский объект, а не **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="b3d80-116">This technique is similar to returning an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer except for the object ID used and the fact that [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) returns a custom object instead of **IAccessible**.</span></span>
-   <span data-ttu-id="b3d80-117">Разработчикам сервера может потребоваться опубликовать сведения, позволяющие клиентам уникальным образом определить **HWND** , чтобы они могли найти его перед вызовом [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) в дескрипторе окна.</span><span class="sxs-lookup"><span data-stu-id="b3d80-117">Server developers may need to publish information that allows clients to uniquely identify the **HWND** so that they can find it before calling [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) on its window handle.</span></span>
-   <span data-ttu-id="b3d80-118">Не реализуйте интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для возвращаемого пользовательского объекта.</span><span class="sxs-lookup"><span data-stu-id="b3d80-118">Do not implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the custom object that is returned.</span></span> <span data-ttu-id="b3d80-119">Если сделать это, ОЛЕАКК будет рассматривать его как стандартный **IAccessible** и может препятствовать использованию пользовательских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b3d80-119">If you do, OLEACC will treat it is as a standard **IAccessible** and may prevent the custom interfaces from being used.</span></span>
-   <span data-ttu-id="b3d80-120">Для использования в разных процессах необходимо зарегистрировать интерфейсы в возвращенном объекте с помощью модели COM.</span><span class="sxs-lookup"><span data-stu-id="b3d80-120">In order to be used across processes, the interfaces on the returned object may need to be registered with Component Object Model (COM).</span></span>

<span data-ttu-id="b3d80-121">Этот метод поддерживается несколькими компонентами Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="b3d80-121">This technique is supported by several Microsoft Office components.</span></span> <span data-ttu-id="b3d80-122">Дополнительные сведения см. в разделе [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="b3d80-122">For more information, see [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

 

 




