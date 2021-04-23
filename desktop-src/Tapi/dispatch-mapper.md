---
description: Средство сопоставления диспетчеризации создается с помощью CoCreateInstance COM и предоставляет один интерфейс Итдиспатчмаппер.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Сопоставитель диспетчеризации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683420"
---
# <a name="dispatch-mapper"></a><span data-ttu-id="896ee-103">Сопоставитель диспетчеризации</span><span class="sxs-lookup"><span data-stu-id="896ee-103">Dispatch Mapper</span></span>

<span data-ttu-id="896ee-104">Средство сопоставления диспетчеризации создается с помощью **COCREATEINSTANCE** com и предоставляет один интерфейс [**итдиспатчмаппер**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper).</span><span class="sxs-lookup"><span data-stu-id="896ee-104">The Dispatch Mapper is created using COM **CoCreateInstance** and exposes one interface, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper).</span></span> <span data-ttu-id="896ee-105">Этот интерфейс позволяет приложению получить указатель диспетчеризации другого интерфейса объекта, учитывая указатель диспетчеризации одного интерфейса и идентификатор GUID другого.</span><span class="sxs-lookup"><span data-stu-id="896ee-105">This interface allows an application to retrieve the dispatch pointer of another interface on an object, given the dispatch pointer of one interface and the GUID of another.</span></span> <span data-ttu-id="896ee-106">Этот интерфейс предназначен для помощи программистам, использующим сценарии приложений, которые не предоставляют средств для интерактивного опроса интерфейсов на объекте.</span><span class="sxs-lookup"><span data-stu-id="896ee-106">This interface is provided to assist programmers using scripting applications which do not provide a means of readily polling the interfaces on an object.</span></span>

<span data-ttu-id="896ee-107">Средство сопоставления диспетчеризации использует интерфейс **иобжектсафети** объекта, чтобы убедиться в том, что объект является надежным для выполнения скриптов на запрошенном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="896ee-107">The Dispatch Mapper uses an object's **IObjectSafety** interface to make sure the object is safe for scripting on the requested interface.</span></span> <span data-ttu-id="896ee-108">Если объект не реализует **иобжектсафети** или объект не является типобезопасным для данного интерфейса, вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="896ee-108">If the object does not implement **IObjectSafety**, or if the object is not safe on this particular interface, the call will fail.</span></span>

 

 



