---
description: Наборы станций, отслеживаемые с помощью сторонней связи, моделируются как линейное устройство и, возможно, связанное телефонное устройство.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Станций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684526"
---
# <a name="stations"></a><span data-ttu-id="d3894-103">Станций</span><span class="sxs-lookup"><span data-stu-id="d3894-103">Stations</span></span>

<span data-ttu-id="d3894-104">Наборы станций, отслеживаемые с помощью сторонней связи, моделируются как линейное устройство и, возможно, связанное телефонное устройство.</span><span class="sxs-lookup"><span data-stu-id="d3894-104">Station sets being monitored through a third-party link are modeled as a line device and possibly an associated phone device.</span></span> <span data-ttu-id="d3894-105">Линейное устройство может иметь несколько адресов, если модель терминала поддерживает несколько номеров каталогов (DN).</span><span class="sxs-lookup"><span data-stu-id="d3894-105">The line device can have multiple addresses, if the modeled terminal supports more than one directory number (DN).</span></span> <span data-ttu-id="d3894-106">Несколько представлений вызовов одного DN можно моделировать как один адрес, поддерживающий несколько вызовов.</span><span class="sxs-lookup"><span data-stu-id="d3894-106">Multiple call appearances on the same DN can be modeled as a single address that supports multiple calls.</span></span>

<span data-ttu-id="d3894-107">Вызовы между двумя станциями в коммутаторе имеют два дескриптора вызова, один из которых предоставляет представление вызовов от первой станции (на устройстве линии), а другой — для представления вызовов со второй станции (на устройстве линии).</span><span class="sxs-lookup"><span data-stu-id="d3894-107">Calls between two stations on the switch have two call handles, one giving the call view from the first station (on its line device), and the other giving the call view from the second station (on its line device).</span></span> <span data-ttu-id="d3894-108">Например, [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) стороннего производителя, размещенного приложением на сервере, перенаправляется на линейное устройство, связанное с станцией, из которой вызывается вызов. в этой строке будет создан маркер вызова по адресу, указанному в [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (таким образом, он обеспечивает контроль над тем, какое различающееся имя используется на телефоне, поддерживающем несколько DNs).</span><span class="sxs-lookup"><span data-stu-id="d3894-108">For example, a third-party [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) placed by an application on the server would be directed to the line device associated with the station from which the call is to be dialed; a call handle would be created on that line, on the address specified in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (thereby giving control over which DN is used on a phone that supports multiple DNs).</span></span> <span data-ttu-id="d3894-109">Когда вызов предлагается конечному адресу, создается новый обработчик вызова, отображающий вызов в состоянии *предложения* . приложения будут иметь представление о том, что он был еще одним вызовом элемента **двкаллид** в [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) , равным обоим вызовам.</span><span class="sxs-lookup"><span data-stu-id="d3894-109">When the call is offered to the destination address, a new call handle showing a call in *offering* state is created; applications would know that it was another view of the same call by the **dwCallID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) being equal for both calls.</span></span> <span data-ttu-id="d3894-110">Оба вызова приведут к *простою* , когда вызов был удален; вызов можно удалить из стороннего приложения, выполнив [**линедроп**](/windows/desktop/api/Tapi/nf-tapi-linedrop) на любом из дескрипторов вызова.</span><span class="sxs-lookup"><span data-stu-id="d3894-110">Both calls would go *idle* when the call was dropped; a call could be dropped from the third-party application by doing a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on either of the call handles.</span></span>

 

 



