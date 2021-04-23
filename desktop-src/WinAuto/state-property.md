---
title: Свойство State
description: Свойство State описывает состояние объекта в данный момент времени. Все объекты поддерживают свойство State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889096"
---
# <a name="state-property"></a><span data-ttu-id="c7296-104">Свойство State</span><span class="sxs-lookup"><span data-stu-id="c7296-104">State Property</span></span>

<span data-ttu-id="c7296-105">Свойство **State** описывает состояние объекта в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="c7296-105">The **State** property describes an object's status at a moment in time.</span></span> <span data-ttu-id="c7296-106">Все объекты поддерживают свойство **State** .</span><span class="sxs-lookup"><span data-stu-id="c7296-106">All objects support the **State** property.</span></span>

<span data-ttu-id="c7296-107">Свойство **State** извлекается путем вызова метода [**IAccessible:: Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span><span class="sxs-lookup"><span data-stu-id="c7296-107">The **State** property is retrieved by calling [**IAccessible::get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span></span>

<span data-ttu-id="c7296-108">Microsoft Active Accessibility предоставляет [константы состояния объектов](object-state-constants.md), определенные в олеакк. h, которые объединяются для определения состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="c7296-108">Microsoft Active Accessibility provides [object state constants](object-state-constants.md), defined in oleacc.h, that are combined to identify an object's state.</span></span> <span data-ttu-id="c7296-109">Рекомендуется, чтобы разработчики сервера использовали эти стандартные значения состояния.</span><span class="sxs-lookup"><span data-stu-id="c7296-109">It is recommended that server developers use these predefined state values.</span></span> <span data-ttu-id="c7296-110">Если возвращаются стандартные значения состояния, клиенты используют [**жетстатетекст**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) для получения локализованной строки, описывающей состояние.</span><span class="sxs-lookup"><span data-stu-id="c7296-110">If predefined state values are returned, clients use [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) to retrieve a localized string that describes the state.</span></span>

<span data-ttu-id="c7296-111">В графиках, которые иногда анимированы, свойство **State** должно иметь значение [**\_ \_ анимированная система состояния**](object-state-constants.md) , а свойство [**Role**](role-property.md) — [**\_ \_ график системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="c7296-111">Graphics that are occasionally animated should have the **State** property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md) and the [**Role**](role-property.md) property set to [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

 

 




