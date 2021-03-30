---
title: Технический обзор
description: Microsoft Active Accessibility улучшает возможности специальных возможностей (специализированные программы, которые помогают людям с ограниченными возможностями использовать компьютеры более эффективно), работают с приложениями, работающими в Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778482"
---
# <a name="technical-overview"></a><span data-ttu-id="15df2-103">Технический обзор</span><span class="sxs-lookup"><span data-stu-id="15df2-103">Technical Overview</span></span>

<span data-ttu-id="15df2-104">Microsoft Active Accessibility улучшает возможности специальных возможностей (специализированные программы, которые помогают людям с ограниченными возможностями использовать компьютеры более эффективно), работают с приложениями, работающими в Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="15df2-104">Microsoft Active Accessibility improves the way accessibility aids (specialized programs that help people with disabilities use computers more effectively) work with applications running on Microsoft Windows.</span></span>

<span data-ttu-id="15df2-105">Microsoft Active Accessibility основан на модели COM, разработанной корпорацией Майкрософт и является отраслевым стандартом, который определяет общий способ обмена данными между приложениями и операционными системами.</span><span class="sxs-lookup"><span data-stu-id="15df2-105">Microsoft Active Accessibility is based on the Component Object Model (COM), which was developed by Microsoft and is an industry standard that defines a common way for applications and operating systems to communicate.</span></span> <span data-ttu-id="15df2-106">Microsoft Active Accessibility состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="15df2-106">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="15df2-107">COM-интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), который предоставляет сведения об элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="15df2-107">The COM interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), which exposes information about UI elements.</span></span> <span data-ttu-id="15df2-108">**IAccessible** также имеет свойства и методы для получения сведений об этом элементе пользовательского интерфейса и управления им.</span><span class="sxs-lookup"><span data-stu-id="15df2-108">**IAccessible** also has properties and methods for obtaining information about and manipulating that UI element.</span></span>
-   <span data-ttu-id="15df2-109">Виневентс — система событий, которая позволяет серверам уведомлять клиентов при изменении объекта со специальными возможностями.</span><span class="sxs-lookup"><span data-stu-id="15df2-109">WinEvents, an event system that allows servers to notify clients when an accessible object changes.</span></span>
-   <span data-ttu-id="15df2-110">Oleacc.dll, поддержка или библиотека DLL времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="15df2-110">Oleacc.dll, a support or run-time DLL.</span></span>

<span data-ttu-id="15df2-111">Библиотека Microsoft Active Accessibility DLL, Oleacc.dll, состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="15df2-111">The Microsoft Active Accessibility DLL, Oleacc.dll, consists of the following components:</span></span>

-   <span data-ttu-id="15df2-112">Функции, которые позволяют клиентам запрашивать указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (например, [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span><span class="sxs-lookup"><span data-stu-id="15df2-112">Functions that allow clients to request an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer (for example, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span></span>
-   <span data-ttu-id="15df2-113">Функции, которые позволяют серверам возвращать указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) клиенту (например, [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span><span class="sxs-lookup"><span data-stu-id="15df2-113">Functions that allow servers to return an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to a client (for example, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span></span>
-   <span data-ttu-id="15df2-114">Функции для получения локализованного текста для кода роли и состояния (например, [**жетролетекст**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) и [**жетстатетекст**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span><span class="sxs-lookup"><span data-stu-id="15df2-114">Functions for getting localized text for the role and state codes (for example, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) and [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span></span>
-   <span data-ttu-id="15df2-115">Некоторые вспомогательные функции ([**акцессиблечилдрен**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span><span class="sxs-lookup"><span data-stu-id="15df2-115">Some helper functions ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span></span>
-   <span data-ttu-id="15df2-116">Код, предоставляющий реализацию класса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) по умолчанию для стандартных элементов управления User и комктл.</span><span class="sxs-lookup"><span data-stu-id="15df2-116">Code that provides the default implementation of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) for standard USER and COMCTL controls.</span></span> <span data-ttu-id="15df2-117">Поскольку они реализуют **IAccessible** от имени системных элементов управления, они называются *прокси-серверами*.</span><span class="sxs-lookup"><span data-stu-id="15df2-117">Because these implement **IAccessible** on behalf of the system controls, they are known as *proxies*.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="15df2-118">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="15df2-118">In this section</span></span>

-   [<span data-ttu-id="15df2-119">Как работает Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="15df2-119">How Active Accessibility Works</span></span>](how-active-accessibility-works.md)
-   [<span data-ttu-id="15df2-120">Основы Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="15df2-120">Active Accessibility Basics</span></span>](active-accessibility-basics.md)
-   [<span data-ttu-id="15df2-121">Рекомендации по серверам</span><span class="sxs-lookup"><span data-stu-id="15df2-121">Server Guidelines</span></span>](server-guidelines.md)
-   [<span data-ttu-id="15df2-122">Рекомендации для клиентов</span><span class="sxs-lookup"><span data-stu-id="15df2-122">Client Guidelines</span></span>](client-guidelines.md)
-   [<span data-ttu-id="15df2-123">Рекомендации по COM и Юникод</span><span class="sxs-lookup"><span data-stu-id="15df2-123">COM and Unicode Guidelines</span></span>](com-and-unicode-guidelines.md)

 

 




