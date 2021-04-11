---
title: Категоризация по возможностям контейнеров
description: Компоненты часто нуждаются в определенных функциональных возможностях контейнера и не будут работать с контейнером, который не обеспечивает поддержку.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068542"
---
# <a name="categorizing-by-container-capabilities"></a><span data-ttu-id="7ddef-103">Категоризация по возможностям контейнеров</span><span class="sxs-lookup"><span data-stu-id="7ddef-103">Categorizing by Container Capabilities</span></span>

<span data-ttu-id="7ddef-104">Компоненты часто нуждаются в определенных функциональных возможностях контейнера и не будут работать с контейнером, который не обеспечивает поддержку.</span><span class="sxs-lookup"><span data-stu-id="7ddef-104">Components often require certain functionality from the container and will not work with a container that does not provide the support.</span></span> <span data-ttu-id="7ddef-105">Пользовательский интерфейс должен отфильтровать компоненты, для которых требуются функции, которые не поддерживаются контейнером.</span><span class="sxs-lookup"><span data-stu-id="7ddef-105">The user interface should filter out components that require functionality the container does not support.</span></span> <span data-ttu-id="7ddef-106">Для этого компоненты можно классифицировать по требуемым функциональным возможностям контейнера.</span><span class="sxs-lookup"><span data-stu-id="7ddef-106">To accomplish this, components can be categorized by the required container functionality.</span></span>

<span data-ttu-id="7ddef-107">Пример компонентов, которые нуждаются в функциональных возможностях из контейнера и не работают в контейнерах, которые не поддерживают эту функциональность, — это простые элементы управления Frame OLE.</span><span class="sxs-lookup"><span data-stu-id="7ddef-107">An example of components that require functionality from the container and do not work in containers that do not support that functionality are simple frame OLE controls.</span></span> <span data-ttu-id="7ddef-108">Классификация по возможностям контейнеров выполняется с помощью дополнительного раздела реестра в ключе CLSID компонента:</span><span class="sxs-lookup"><span data-stu-id="7ddef-108">Categorizing by container capabilities is accomplished by an additional registry key within the component's CLSID key:</span></span>

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

<span data-ttu-id="7ddef-109">Как показано в этом примере, компонент может принадлежать к категориям компонентов, которые указывают на поддерживаемые функциональные возможности, а также к категориям компонентов, которые указывают на требуемую функциональность.</span><span class="sxs-lookup"><span data-stu-id="7ddef-109">As shown in this example, a component can belong to component categories that indicate supported functionality as well as to component categories that indicate required functionality.</span></span>

<span data-ttu-id="7ddef-110">В следующем примере элемент управления "Кнопка" является универсальным элементом управления OLE, который не поддерживает никаких дополнительных функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="7ddef-110">In the following example, the button control is a generic OLE control that supports no additional functionality.</span></span> <span data-ttu-id="7ddef-111">Он будет работать в любом контейнере управления OLE.</span><span class="sxs-lookup"><span data-stu-id="7ddef-111">It will work in any OLE control container.</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

<span data-ttu-id="7ddef-112">Сравните предыдущий пример со следующим примером, в котором Мидбконтрол может использовать Visual Basic привязки данных, если контейнер поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="7ddef-112">Compare the preceding example with the next example in which the MyDBControl can use Visual Basic data binding if the container supports it.</span></span> <span data-ttu-id="7ddef-113">Однако он определен таким образом, что он будет работать в контейнерах, которые не поддерживают Visual Basic привязки данных (возможно, с помощью другого API базы данных):</span><span class="sxs-lookup"><span data-stu-id="7ddef-113">However, it has been defined so that it will work in containers that do not support Visual Basic data binding (perhaps by a different database API):</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

<span data-ttu-id="7ddef-114">Элемент управления GroupBox — это простой элемент управления Frame.</span><span class="sxs-lookup"><span data-stu-id="7ddef-114">The GroupBox control is a simple frame control.</span></span> <span data-ttu-id="7ddef-115">Он основывается на контейнере, реализующем интерфейс [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) , и будет работать правильно только в таких контейнерах:</span><span class="sxs-lookup"><span data-stu-id="7ddef-115">It relies on the container implementing the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface and will work correctly only in such containers:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

<span data-ttu-id="7ddef-116">Контейнер, поддерживающий Visual Basic привязанные к данным элементы управления, но не поддерживающий простые элементы управления Frame, будет указывать CATID \_ элемента управления и CATID \_ вбдатабаунд в пользовательском интерфейсе элемента управления INSERT.</span><span class="sxs-lookup"><span data-stu-id="7ddef-116">A container that supports Visual Basic data bound controls but does not support simple frame controls would specify CATID\_Control and CATID\_VBDatabound to the insert control user interface.</span></span> <span data-ttu-id="7ddef-117">Список элементов управления, отображаемых для пользователя, будет содержать \_ кнопку CLSID и \_ мидбконтрол CLSID.</span><span class="sxs-lookup"><span data-stu-id="7ddef-117">The list of controls displayed to the user would contain the CLSID\_Button and CLSID\_MyDBControl.</span></span> <span data-ttu-id="7ddef-118">\_Группа CLSID не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="7ddef-118">CLSID\_GroupBox would not be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ddef-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7ddef-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ddef-120">Связывание значков с категорией</span><span class="sxs-lookup"><span data-stu-id="7ddef-120">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="7ddef-121">Категоризация по возможностям компонентов</span><span class="sxs-lookup"><span data-stu-id="7ddef-121">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="7ddef-122">Классы и ассоциации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7ddef-122">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="7ddef-123">Определение категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="7ddef-123">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="7ddef-124">Диспетчер категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="7ddef-124">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




