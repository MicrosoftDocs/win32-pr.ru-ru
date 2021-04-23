---
title: Динамический API аннотации
description: Динамический API Аннотации — это расширение Microsoft Active Accessibility, которое позволяет разработчикам настраивать существующую поддержку IAccessible без использования подверженных ошибкам методов подклассов или оболочек.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986850"
---
# <a name="dynamic-annotation-api"></a><span data-ttu-id="18cda-103">Динамический API аннотации</span><span class="sxs-lookup"><span data-stu-id="18cda-103">Dynamic Annotation API</span></span>

<span data-ttu-id="18cda-104">Динамический API Аннотации — это расширение Microsoft Active Accessibility, которое позволяет разработчикам настраивать существующую поддержку [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) без использования подверженных ошибкам методов подклассов или оболочек.</span><span class="sxs-lookup"><span data-stu-id="18cda-104">The Dynamic Annotation API is an extension to Microsoft Active Accessibility that allows developers to customize existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support without having to use error-prone subclassing or wrapping techniques.</span></span> <span data-ttu-id="18cda-105">Этот механизм также позволяет разработчикам передавать подсказки или другую полезную информацию в Oleacc.dll прокси-серверы.</span><span class="sxs-lookup"><span data-stu-id="18cda-105">This mechanism also allows developers to pass hints or other useful information to the Oleacc.dll proxies.</span></span>

<span data-ttu-id="18cda-106">Динамическая Аннотация обычно используется для исправления или уточнения неточного экземпляра объекта [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , предоставляемого существующим Oleacc.dll прокси.</span><span class="sxs-lookup"><span data-stu-id="18cda-106">Dynamic Annotation is typically used to correct or amend an inaccurate instance of an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object exposed by an existing Oleacc.dll proxy.</span></span> <span data-ttu-id="18cda-107">Например, его можно использовать для переопределения свойств [**имени**](name-property.md) и [**роли**](role-property.md) , предоставляемых прокси-сервером по умолчанию, а также для предоставления свойств [**Description**](description-property.md) и [**Help**](help-property.md) (которые могут не предоставляться прокси-сервером по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="18cda-107">For example, you can use it to override the [**Name**](name-property.md) and [**Role**](role-property.md) properties provided by the default proxy, and to supply [**Description**](description-property.md) and [**Help**](help-property.md) properties (which may not be provided by the default proxy).</span></span>

<span data-ttu-id="18cda-108">В Windows 7 разработчики могут использовать динамический API аннотации, чтобы закомментировать свойства автоматизации пользовательского интерфейса Майкрософт, а также свойства Microsoft Active Accessibility прокси-объектов, которые Oleacc.dll создавать для стандартных элементов управления Windows.</span><span class="sxs-lookup"><span data-stu-id="18cda-108">With Windows 7, developers can use the Dynamic Annotation API to annotate Microsoft UI Automation properties as well as Microsoft Active Accessibility properties of the proxy objects that Oleacc.dll creates for standard Windows controls.</span></span> <span data-ttu-id="18cda-109">Oleacc.dll прокси-объекты служат для клиентов Microsoft Active Accessibility и автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="18cda-109">The Oleacc.dll proxy objects serve both Microsoft Active Accessibility and UI Automation clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="18cda-110">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="18cda-110">In this section</span></span>

-   [<span data-ttu-id="18cda-111">Основные сведения</span><span class="sxs-lookup"><span data-stu-id="18cda-111">Background Information</span></span>](background-information.md)
-   [<span data-ttu-id="18cda-112">Альтернативы динамической аннотации</span><span class="sxs-lookup"><span data-stu-id="18cda-112">Alternatives to Dynamic Annotation</span></span>](alternatives-to-dynamic-annotation.md)
-   [<span data-ttu-id="18cda-113">Типы динамических заметок</span><span class="sxs-lookup"><span data-stu-id="18cda-113">Types of Dynamic Annotation</span></span>](types-of-dynamic-annotation.md)
-   [<span data-ttu-id="18cda-114">Непосредственная Аннотация</span><span class="sxs-lookup"><span data-stu-id="18cda-114">Direct Annotation</span></span>](direct-annotation.md)
-   [<span data-ttu-id="18cda-115">Аннотация схемы значений</span><span class="sxs-lookup"><span data-stu-id="18cda-115">Value Map Annotation</span></span>](value-map-annotation.md)
-   [<span data-ttu-id="18cda-116">Заметки сервера</span><span class="sxs-lookup"><span data-stu-id="18cda-116">Server Annotation</span></span>](server-annotation.md)
-   [<span data-ttu-id="18cda-117">Проблемы и ограничения</span><span class="sxs-lookup"><span data-stu-id="18cda-117">Issues and Limitations</span></span>](issues-and-limitations.md)

 

 




