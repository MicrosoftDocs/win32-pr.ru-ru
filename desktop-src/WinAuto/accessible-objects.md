---
title: Доступные объекты
description: С помощью Microsoft Active Accessibility элементы пользовательского интерфейса предоставляются клиентам как объекты модели COM.
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411366"
---
# <a name="accessible-objects"></a><span data-ttu-id="fe969-103">Доступные объекты</span><span class="sxs-lookup"><span data-stu-id="fe969-103">Accessible Objects</span></span>

<span data-ttu-id="fe969-104">С помощью Microsoft Active Accessibility элементы пользовательского интерфейса предоставляются клиентам как объекты модели COM.</span><span class="sxs-lookup"><span data-stu-id="fe969-104">With Microsoft Active Accessibility, UI elements are exposed to clients as Component Object Model (COM) objects.</span></span> <span data-ttu-id="fe969-105">Эти *объекты со специальными возможностями* сохраняют части информации, называемые *свойствами*, которые описывают имя объекта, расположение экрана и другие сведения, необходимые для вспомогательных функций.</span><span class="sxs-lookup"><span data-stu-id="fe969-105">These *accessible objects* maintain pieces of information, called *properties*, which describe the object's name, screen location, and other information needed by accessibility aids.</span></span> <span data-ttu-id="fe969-106">Объекты со специальными возможностями также предоставляют *методы* , которые вызываются клиентами для выполнения некоторых действий объектом.</span><span class="sxs-lookup"><span data-stu-id="fe969-106">Accessible objects also provide *methods* that clients call to cause the object to perform some action.</span></span> <span data-ttu-id="fe969-107">Доступные объекты, имеющие простые элементы, связанные с ними, также называются *родителями* или *контейнерами*.</span><span class="sxs-lookup"><span data-stu-id="fe969-107">Accessible objects that have simple elements associated with them are also called *parents*, or *containers*.</span></span>

<span data-ttu-id="fe969-108">Доступные объекты реализуются с помощью интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) на основе COM Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="fe969-108">Accessible objects are implemented using Microsoft Active Accessibility's COM-based [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="fe969-109">Методы и свойства **IAccessible** позволяют клиентским приложениям получать сведения о элементах пользовательского интерфейса, необходимых пользователям.</span><span class="sxs-lookup"><span data-stu-id="fe969-109">The **IAccessible** methods and properties enable client applications to get information about UI elements needed by users.</span></span> <span data-ttu-id="fe969-110">Например, метод [**IAccessible:: Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) возвращает указатель интерфейса на родительский объект доступного объекта, а метод [**IAccessible:: аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) предоставляет клиентам возможность получать сведения о других объектах в контейнере.</span><span class="sxs-lookup"><span data-stu-id="fe969-110">For example, [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) returns an interface pointer to an accessible object's parent, and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) provides a means for clients to get information about other objects within a container.</span></span>

<span data-ttu-id="fe969-111">Дополнительные сведения о взаимосвязи между доступными объектами и простыми элементами см. в разделе [простые элементы](simple-elements.md).</span><span class="sxs-lookup"><span data-stu-id="fe969-111">For more information about how accessible objects and simple elements are related, see [Simple Elements](simple-elements.md).</span></span>

 

 




