---
title: Свойства и методы
description: Как и любой объект OLE, элемент управления обеспечивает большую часть его функциональных возможностей посредством набора входящих интерфейсов со свойствами и методами.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067641"
---
# <a name="properties-and-methods"></a><span data-ttu-id="5d7a4-103">Свойства и методы</span><span class="sxs-lookup"><span data-stu-id="5d7a4-103">Properties and Methods</span></span>

<span data-ttu-id="5d7a4-104">Как и любой объект OLE, элемент управления обеспечивает большую часть его функциональных возможностей посредством набора входящих интерфейсов со свойствами и методами.</span><span class="sxs-lookup"><span data-stu-id="5d7a4-104">Like any OLE object, a control provides much of its functionality through a set of incoming interfaces with properties and methods.</span></span>

<span data-ttu-id="5d7a4-105">Элемент управления предоставляет свойства и методы через OLE-автоматизацию, чтобы контейнеры могли обращаться к ним под управлением языка программирования, предоставляемого контейнером.</span><span class="sxs-lookup"><span data-stu-id="5d7a4-105">A control exposes properties and methods through OLE automation so that containers can access them under the control of a container-supplied programming language.</span></span>

<span data-ttu-id="5d7a4-106">Для поддержки доступа к свойствам через пользовательский интерфейс элемент управления предоставляет страницы свойств, поддержку \_ свойств олеиверб, Просмотр свойств и привязку данных посредством изменения свойства нотфикатионс.</span><span class="sxs-lookup"><span data-stu-id="5d7a4-106">To support access to properties through a user interface, a control provides property pages, support for OLEIVERB\_PROPERTIES, per property browsing, and data binding through property change notfications.</span></span>

-   <span data-ttu-id="5d7a4-107">С помощью страниц свойств элемент управления может отображать его свойства независимо от его контейнера, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="5d7a4-107">Through property pages a control can display its properties, independent of its container, if necessary.</span></span>
-   <span data-ttu-id="5d7a4-108">При поддержке \_ свойств олеиверб элемент свойства отображается в меню контейнера.</span><span class="sxs-lookup"><span data-stu-id="5d7a4-108">By supporting OLEIVERB\_PROPERTIES, the Properties item is displayed on the container's menu.</span></span> <span data-ttu-id="5d7a4-109">Затем конечный пользователь может выбрать элемент **Свойства** , чтобы просмотреть страницы свойств элемента управления и изменить свойства.</span><span class="sxs-lookup"><span data-stu-id="5d7a4-109">Then, the end user can select the **Properties** item to view the control's property pages and modify the properties.</span></span>
-   <span data-ttu-id="5d7a4-110">Каждый просмотр свойств поддерживает контейнер, который может отображать свойства элемента управления как часть более крупной страницы свойств, которая может включать свойства из нескольких элементов управления в контейнере.</span><span class="sxs-lookup"><span data-stu-id="5d7a4-110">Per property browsing supports a container that can display the control's properties as part of a larger property sheet that may include properties from several controls in the container.</span></span>
-   <span data-ttu-id="5d7a4-111">С помощью уведомления об изменении свойства элемент управления может уведомлять Клиента о том, что его свойства изменились, позволяя клиенту выполнять все необходимые действия в результате.</span><span class="sxs-lookup"><span data-stu-id="5d7a4-111">Through property change notification, a control can notify a client that its properties have change, allowing the client to take any necessary actions as a result.</span></span>

<span data-ttu-id="5d7a4-112">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="5d7a4-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="5d7a4-113">Свойства элемента управления</span><span class="sxs-lookup"><span data-stu-id="5d7a4-113">Control Properties</span></span>](control-properties.md)
-   [<span data-ttu-id="5d7a4-114">Методы управления</span><span class="sxs-lookup"><span data-stu-id="5d7a4-114">Control Methods</span></span>](control-methods.md)

## <a name="related-topics"></a><span data-ttu-id="5d7a4-115">См. также</span><span class="sxs-lookup"><span data-stu-id="5d7a4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d7a4-116">Элементы управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="5d7a4-116">ActiveX Controls</span></span>](activex-controls.md)
</dt> <dt>

[<span data-ttu-id="5d7a4-117">Страницы свойств и вкладки свойств</span><span class="sxs-lookup"><span data-stu-id="5d7a4-117">Property Pages and Property Sheets</span></span>](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




