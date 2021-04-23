---
title: Типы поддержки IAccessible
description: Типы поддержки IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776223"
---
# <a name="types-of-iaccessible-support"></a><span data-ttu-id="c5473-103">Типы поддержки IAccessible</span><span class="sxs-lookup"><span data-stu-id="c5473-103">Types of IAccessible Support</span></span>

<span data-ttu-id="c5473-104">Серверы Microsoft Active Accessibility поддерживают два типа поддержки [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : Native и прокси.</span><span class="sxs-lookup"><span data-stu-id="c5473-104">Microsoft Active Accessibility servers have two types of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support: native and proxied.</span></span> <span data-ttu-id="c5473-105">Элементы пользовательского интерфейса, используемые в приложении, определяют, какой тип поддержки подходит.</span><span class="sxs-lookup"><span data-stu-id="c5473-105">The UI elements used in an application determine which type of support is appropriate.</span></span> <span data-ttu-id="c5473-106">Многие серверы, написанные сегодня, используют все преимущества прокси-серверов **IAccessible** и реализуют **IAccessible** для тех элементов управления, которые не являются Oleacc.dll, например безоконные элементы управления и элементы управления с настраиваемым именем класса окна.</span><span class="sxs-lookup"><span data-stu-id="c5473-106">Many servers being written today take full advantage of **IAccessible** proxies and only implement **IAccessible** for those controls that are not proxied by Oleacc.dll, such as windowless controls or controls with a custom window class name.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5473-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="c5473-107">In this section</span></span>

-   [<span data-ttu-id="c5473-108">Реализация собственного Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="c5473-108">Native Active Accessibility Implementation</span></span>](native-active-accessibility-implementation.md)
-   [<span data-ttu-id="c5473-109">Прокси-серверы IAccessible</span><span class="sxs-lookup"><span data-stu-id="c5473-109">IAccessible Proxies</span></span>](iaccessible-proxies.md)

 

 




