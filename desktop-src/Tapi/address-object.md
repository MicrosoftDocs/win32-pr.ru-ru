---
description: Объект Address представляет сущность, которая может принимать или принимать вызовы.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Объект Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911232"
---
# <a name="address-object"></a><span data-ttu-id="f1727-103">Объект Address</span><span class="sxs-lookup"><span data-stu-id="f1727-103">Address Object</span></span>

<span data-ttu-id="f1727-104">Объект Address представляет сущность, которая может принимать или принимать вызовы.</span><span class="sxs-lookup"><span data-stu-id="f1727-104">The Address object represents an entity that can make or receive calls.</span></span> <span data-ttu-id="f1727-105">Этот объект предоставляет интерфейсы и методы, позволяющие приложению выполнять ряд операций, например:</span><span class="sxs-lookup"><span data-stu-id="f1727-105">This object exposes interfaces and methods that allow an application to perform a number of operations, such as:</span></span>

-   <span data-ttu-id="f1727-106">Определите, может ли указанный адрес поддерживать определенный набор потребностей типа носителя.</span><span class="sxs-lookup"><span data-stu-id="f1727-106">Discover whether a specified address can support a particular set of media type needs.</span></span>
-   <span data-ttu-id="f1727-107">Перечислить вызовы, которые в настоящее время связаны с адресом.</span><span class="sxs-lookup"><span data-stu-id="f1727-107">Enumerate calls currently associated with the address.</span></span>
-   <span data-ttu-id="f1727-108">Создание или переадресация вызовов.</span><span class="sxs-lookup"><span data-stu-id="f1727-108">Create or forward calls.</span></span>
-   <span data-ttu-id="f1727-109">Возвращает имя связанного поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="f1727-109">Get the name of the associated service provider.</span></span>
-   <span data-ttu-id="f1727-110">Если поставщик службы мультимедиа существует, получите указатели интерфейса, которые позволяют выполнять подробные операции терминала.</span><span class="sxs-lookup"><span data-stu-id="f1727-110">If a media service provider exists, get interface pointers that allow detailed terminal manipulation.</span></span>
-   <span data-ttu-id="f1727-111">Получение и задание других сведений, например о том, ожидает ли сообщение.</span><span class="sxs-lookup"><span data-stu-id="f1727-111">Get and set other information, such as whether a message is waiting.</span></span>

<span data-ttu-id="f1727-112">Большинство адресов связаны с терминалом, но это не является единообразно.</span><span class="sxs-lookup"><span data-stu-id="f1727-112">Most addresses are associated with a terminal, but this is not uniformly the case.</span></span> <span data-ttu-id="f1727-113">Например, удаленный TSP, предоставляющий доступ к оборудованию на сервере, будет иметь адрес на локальном компьютере, но не в терминале.</span><span class="sxs-lookup"><span data-stu-id="f1727-113">For example, a remote TSP that provides access to equipment on a server will have an address on the local machine but not a terminal.</span></span> <span data-ttu-id="f1727-114">Модем без динамиков также не имеет терминала, связанного с адресом.</span><span class="sxs-lookup"><span data-stu-id="f1727-114">A speakerless modem also has no terminal associated with its address.</span></span>

<span data-ttu-id="f1727-115">Если у адреса нет связанного терминала, интерфейс [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) не предоставляется в объекте.</span><span class="sxs-lookup"><span data-stu-id="f1727-115">If an address does not have an associated terminal, the [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is not exposed on the object.</span></span>

<span data-ttu-id="f1727-116">В примере кода [Select a Address](select-an-address.md) показан базовый процесс получения указателя на объект адреса.</span><span class="sxs-lookup"><span data-stu-id="f1727-116">The [Select an Address](select-an-address.md) code example shows the basic process for acquiring an address object pointer.</span></span>

<span data-ttu-id="f1727-117">Список всех интерфейсов, связанных с объектом Address, см. в разделе [интерфейсы объекта адреса](address-object-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="f1727-117">See [Address Object Interfaces](address-object-interfaces.md) for a list of all interfaces associated with the Address object.</span></span>

 

 
