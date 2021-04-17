---
description: Объект Call представляет соединение адресов между локальным адресом и одним или несколькими другими адресами.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Вызвать объект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674477"
---
# <a name="call-object"></a><span data-ttu-id="f3238-103">Вызвать объект</span><span class="sxs-lookup"><span data-stu-id="f3238-103">Call Object</span></span>

<span data-ttu-id="f3238-104">Объект Call представляет соединение адреса между локальным адресом и одним или несколькими другими адресами.</span><span class="sxs-lookup"><span data-stu-id="f3238-104">The Call object represents an address's connection between the local address and one or more other addresses.</span></span> <span data-ttu-id="f3238-105">Все управление вызовами осуществляется через объект call.</span><span class="sxs-lookup"><span data-stu-id="f3238-105">All call control is done through the Call object.</span></span> <span data-ttu-id="f3238-106">[**Итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) и [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) — это наиболее часто используемые интерфейсы для объекта Call.</span><span class="sxs-lookup"><span data-stu-id="f3238-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) are the most frequently used interfaces on the call object.</span></span> <span data-ttu-id="f3238-107">Эти интерфейсы реализуют разнообразные операции и запросы, например получение указателей интерфейса для потоков мультимедиа или получение идентификатора вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="f3238-107">These interfaces implement a variety of operations and queries, such as acquiring interface pointers for media streams or getting the caller ID.</span></span> <span data-ttu-id="f3238-108">Ознакомьтесь с основными обзорными разделами об [операциях сеанса](session-operations-ovr.md) и [сведениях о сеансе](session-information-ovr.md) для проверки, поддерживаемых TAPI.</span><span class="sxs-lookup"><span data-stu-id="f3238-108">See the main overview sections on [Session Operations](session-operations-ovr.md) and [Session Information](session-information-ovr.md) for reviews of those supported by TAPI.</span></span>

<span data-ttu-id="f3238-109">Поставщик служб мультимедиа может реализовывать [интерфейсы, зависящие от поставщика](provider-specific-interfaces.md), которые объединяются по объекту вызова по интерфейсу TAPI.</span><span class="sxs-lookup"><span data-stu-id="f3238-109">A media service provider can implement [provider-specific interfaces](provider-specific-interfaces.md), which are aggregated on a call object by TAPI.</span></span> <span data-ttu-id="f3238-110">Подробные сведения о том, что реализовано поставщиком, см. в документации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="f3238-110">For detailed information on what a provider has implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="f3238-111">Пример [вызова](make-a-call.md) и получения примеров кода [вызова](receive-a-call.md) демонстрирует несколько иллюстраций использования объекта Call.</span><span class="sxs-lookup"><span data-stu-id="f3238-111">The [Make a Call](make-a-call.md) and [Receive a Call](receive-a-call.md) code examples show some illustrations of using a Call object.</span></span>

<span data-ttu-id="f3238-112">Список всех интерфейсов, связанных с объектом Call, см. в разделе [Call Object interfaces](call-object-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="f3238-112">See [Call Object Interfaces](call-object-interfaces.md) for a list of all interfaces associated with the Call object.</span></span>

 

 



