---
title: Создание прокси-объектов
description: В дополнение к проектированию классов, реализующих свойства и методы IAccessible, разработчикам сервера также может потребоваться разработать прокси-объекты, отслеживающие жизненный интервал доступных объектов.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774090"
---
# <a name="creating-proxy-objects"></a><span data-ttu-id="7a5a6-103">Создание прокси-объектов</span><span class="sxs-lookup"><span data-stu-id="7a5a6-103">Creating Proxy Objects</span></span>

<span data-ttu-id="7a5a6-104">В дополнение к проектированию классов, реализующих свойства и методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , разработчикам сервера также может потребоваться разработать *прокси-* объекты, отслеживающие жизненный интервал доступных объектов.</span><span class="sxs-lookup"><span data-stu-id="7a5a6-104">In addition to designing classes that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods, server developers may also need to design *proxy* objects that monitor the life span of accessible objects.</span></span> <span data-ttu-id="7a5a6-105">Если доступный объект в приложении доступен в течение всего времени выполнения приложения, создание прокси-объекта не требуется.</span><span class="sxs-lookup"><span data-stu-id="7a5a6-105">If an accessible object in an application is available the entire time the application is running, then you do not need to create a proxy object.</span></span> <span data-ttu-id="7a5a6-106">Если можно уничтожить доступный объект во время работы приложения, необходимо создать прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="7a5a6-106">If it is possible to destroy the accessible object while the application is running, then you must create a proxy object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7a5a6-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="7a5a6-107">In this section</span></span>

-   [<span data-ttu-id="7a5a6-108">Что такое прокси-объекты?</span><span class="sxs-lookup"><span data-stu-id="7a5a6-108">What Are Proxy Objects?</span></span>](what-are-proxy-objects.md)
-   [<span data-ttu-id="7a5a6-109">Зачем нужны прокси-объекты</span><span class="sxs-lookup"><span data-stu-id="7a5a6-109">Why Proxy Objects Are Needed</span></span>](why-proxy-objects-are-needed.md)
-   [<span data-ttu-id="7a5a6-110">Рекомендации по проектированию прокси-объектов</span><span class="sxs-lookup"><span data-stu-id="7a5a6-110">Design Considerations for Proxy Objects</span></span>](design-considerations-for-proxy-objects.md)

 

 




