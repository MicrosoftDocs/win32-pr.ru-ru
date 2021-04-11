---
title: Основные сведения
description: Компонент Microsoft Active Accessibility oleacc.dll создает прокси-объекты, реализующие IAccessible от имени стандартных элементов управления Windows.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132882"
---
# <a name="background-information"></a><span data-ttu-id="9ec33-103">Основные сведения</span><span class="sxs-lookup"><span data-stu-id="9ec33-103">Background Information</span></span>

<span data-ttu-id="9ec33-104">Компонент Microsoft Active Accessibility oleacc.dll создает прокси-объекты, реализующие [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) от имени стандартных элементов управления Windows.</span><span class="sxs-lookup"><span data-stu-id="9ec33-104">The Microsoft Active Accessibility component, oleacc.dll, creates proxy objects that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) on behalf of standard Windows controls.</span></span> <span data-ttu-id="9ec33-105">Так как эти прокси-серверы используют стандартные сообщения Windows и интерфейсы API для конкретного элемента управления для получения сведений о каждом элементе управления, не существовал прямой механизм для настройки сведений, предоставляемых этими прокси-серверами через **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="9ec33-105">Because these proxies use standard Windows messages and control-specific APIs to collect information about each control, there has been no direct mechanism for customizing the information these proxies expose through **IAccessible**.</span></span>

<span data-ttu-id="9ec33-106">Сейчас можно настроить существующую реализацию [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , используя методы подкласса и оболочки.</span><span class="sxs-lookup"><span data-stu-id="9ec33-106">Currently, you can customize an existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation using subclassing and wrapping techniques.</span></span> <span data-ttu-id="9ec33-107">Однако эти методы являются утомительными и подвержены ошибкам.</span><span class="sxs-lookup"><span data-stu-id="9ec33-107">However, these techniques are tedious and error-prone.</span></span> <span data-ttu-id="9ec33-108">Фактически, большая часть кода, написанного для переопределения одного или двух свойств, связана с реализацией подкласса и упаковки. только небольшая дробь выполняет реальную задачу переопределения информации.</span><span class="sxs-lookup"><span data-stu-id="9ec33-108">In fact, the majority of the code written to override one or two properties is concerned with implementing subclassing and wrapping; only a small fraction carries out the real task of overriding information.</span></span> <span data-ttu-id="9ec33-109">Динамическая Аннотация улучшает ситуацию, предоставляя аналогичные возможности без необходимости написания подклассов или переноса кода.</span><span class="sxs-lookup"><span data-stu-id="9ec33-109">Dynamic Annotation improves the situation by providing similar capabilities without requiring you to write subclassing or wrapping code.</span></span> <span data-ttu-id="9ec33-110">Вместо этого вы можете сосредоточиться на предоставлении кода, предоставляющего правильные сведения.</span><span class="sxs-lookup"><span data-stu-id="9ec33-110">Instead, you can focus on providing code that supplies the correct information.</span></span> <span data-ttu-id="9ec33-111">Динамическая Аннотация позволяет разработчикам передавать подсказки и другие полезные сведения для ОЛЕАКК для настройки предоставляемой им информации.</span><span class="sxs-lookup"><span data-stu-id="9ec33-111">Dynamic Annotation allows developers to pass hints and other useful information to OLEACC to customize the information it exposes.</span></span> <span data-ttu-id="9ec33-112">Эта возможность позволяет снизить затраты на поддержку Active Accessibility Майкрософт и позволить разработчикам значительно повысить доступность своих пользовательских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="9ec33-112">This capability alone will reduce the cost of supporting Microsoft Active Accessibility and allow developers to greatly improve the accessibility of their user interfaces.</span></span>

 

 




