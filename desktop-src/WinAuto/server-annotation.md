---
title: Заметки сервера
description: В этом разделе приводятся сведения об использовании серверных заметок.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067584"
---
# <a name="server-annotation"></a><span data-ttu-id="328ab-103">Заметки сервера</span><span class="sxs-lookup"><span data-stu-id="328ab-103">Server Annotation</span></span>

<span data-ttu-id="328ab-104">В этом разделе приводятся сведения об использовании серверных заметок.</span><span class="sxs-lookup"><span data-stu-id="328ab-104">This section provides information about using server annotation.</span></span>

## <a name="summary"></a><span data-ttu-id="328ab-105">Сводка</span><span class="sxs-lookup"><span data-stu-id="328ab-105">Summary</span></span>

<span data-ttu-id="328ab-106">Вы определяете класс, реализующий [**иаккпропсервер**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), создаете его экземпляр и сообщаете системе, что необходимо переопределить определенные свойства в определенных элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="328ab-106">You define a class that implements [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), create an instance of it, and tell the system that you want it to override specific properties on specific UI elements.</span></span> <span data-ttu-id="328ab-107">Когда клиент запрашивает одно из свойств из одного из элементов пользовательского интерфейса, вызывается объект, и ему предоставляется возможность предоставить значение.</span><span class="sxs-lookup"><span data-stu-id="328ab-107">When a client requests one of the properties from one of the UI elements, your object is called and given an opportunity to provide a value.</span></span> <span data-ttu-id="328ab-108">Если объект возвращает значение, это значение передается обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="328ab-108">If your object returns a value, that value is passed back to the client.</span></span> <span data-ttu-id="328ab-109">Если объект не возвращает значение, клиенту возвращается значение по умолчанию для этого элемента пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="328ab-109">If your object does not return a value, the default value for that UI element is returned to the client.</span></span>

## <a name="when-to-use-this-technique"></a><span data-ttu-id="328ab-110">Когда следует использовать этот метод</span><span class="sxs-lookup"><span data-stu-id="328ab-110">When to Use This Technique</span></span>

<span data-ttu-id="328ab-111">Используйте этот метод, если требуется переопределить свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для объекта.</span><span class="sxs-lookup"><span data-stu-id="328ab-111">Use this technique when you want to override the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for an object.</span></span> <span data-ttu-id="328ab-112">Этот метод гораздо проще, чем предыдущие методы **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="328ab-112">This technique is much simpler than previous **IAccessible** techniques.</span></span> <span data-ttu-id="328ab-113">Дополнительные сведения см. [в разделе альтернативы динамической аннотации](alternatives-to-dynamic-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="328ab-113">For more information, see [Alternatives to Dynamic Annotation](alternatives-to-dynamic-annotation.md).</span></span>

<span data-ttu-id="328ab-114">Нельзя использовать заметки сервера для изменения структуры предоставленного объекта.</span><span class="sxs-lookup"><span data-stu-id="328ab-114">You cannot use server annotation to alter the exposed object structure.</span></span> <span data-ttu-id="328ab-115">Чтобы изменить структуру объекта, необходимо реализовать полный указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="328ab-115">To change the structure of an object, you must implement a full [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="328ab-116">Дополнительные сведения о заметках сервера см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="328ab-116">For more information on server annotation, see the following topics:</span></span>

-   [<span data-ttu-id="328ab-117">Использование заметок сервера</span><span class="sxs-lookup"><span data-stu-id="328ab-117">Using Server Annotation</span></span>](using-server-annotation.md)
-   [<span data-ttu-id="328ab-118">Пример аннотации сервера</span><span class="sxs-lookup"><span data-stu-id="328ab-118">Server Annotation Sample</span></span>](server-annotation-sample.md)

 

 




