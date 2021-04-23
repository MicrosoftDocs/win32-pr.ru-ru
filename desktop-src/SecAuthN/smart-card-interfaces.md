---
description: Интерфейс смарт-карты состоит из предопределенного набора служб, доступных в смарт-карте, протоколов, необходимых для вызова служб, и любых допущений, касающихся контекста служб.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Интерфейсы смарт-карт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816209"
---
# <a name="smart-card-interfaces"></a><span data-ttu-id="0c369-103">Интерфейсы смарт-карт</span><span class="sxs-lookup"><span data-stu-id="0c369-103">Smart Card Interfaces</span></span>

<span data-ttu-id="0c369-104">Интерфейс [*смарт-карты*](../secgloss/s-gly.md) состоит из предопределенного набора служб, доступных в *смарт-карте*, протоколов, необходимых для вызова служб, и любых допущений, касающихся контекста служб.</span><span class="sxs-lookup"><span data-stu-id="0c369-104">A [*smart card*](../secgloss/s-gly.md) interface consists of a predefined set of services available within a *smart card*, the protocols necessary to invoke the services, and any assumptions regarding the context of the services.</span></span>

<span data-ttu-id="0c369-105">В отношении смарт-карт термин "интерфейс" аналогичен использованию в COM, который, в свою очередь, аналогичен идентификатору приложения ISO 7816/5, но с другой областью.</span><span class="sxs-lookup"><span data-stu-id="0c369-105">With respect to smart cards, the term "interface" is similar to how it is used in COM, which in turn is similar in concept to the ISO 7816/5 application identifier but with a different scope.</span></span>

<span data-ttu-id="0c369-106">Каждый интерфейс смарт-карты идентифицируется по идентификатору GUID.</span><span class="sxs-lookup"><span data-stu-id="0c369-106">Each smart card interface is identified by a GUID.</span></span> <span data-ttu-id="0c369-107">Например, может быть определен интерфейс, который предоставляет биорхисм сведения его владельцу.</span><span class="sxs-lookup"><span data-stu-id="0c369-107">For example, an interface might be defined that provides biorhythm information to its holder.</span></span> <span data-ttu-id="0c369-108">Если данная служба поддерживается данной смарт-картой, она может запрашивать поддержку этого GUID интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0c369-108">If a given smart card supports this service, then it may claim to support that interface GUID.</span></span> <span data-ttu-id="0c369-109">Используя идентификаторы GUID интерфейса, приложение может выполнять поиск определенного набора интерфейсов, находя любую карту, поддерживающую этот набор, для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="0c369-109">Using the interface GUIDs, an application may search for a particular set of interfaces, locating any card that supports that set, to complete a task.</span></span>

<span data-ttu-id="0c369-110">Хотя интерфейс имеет один GUID, он может быть реализован по-разному на разных картах.</span><span class="sxs-lookup"><span data-stu-id="0c369-110">Although an interface has one GUID, it might be implemented differently on different cards.</span></span> <span data-ttu-id="0c369-111">Например, интерфейс биорхисм, упомянутый выше, может иметь несколько различных реализаций, но на все они ссылаются с использованием одного и того же идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="0c369-111">For example, the biorhythm interface mentioned above can have several different implementations, yet all are referenced using the same GUID.</span></span> <span data-ttu-id="0c369-112">Разные реализации не изменяют взаимодействие между приложением и смарт-картой. Однако взаимодействие между [*поставщиком службы*](../secgloss/c-gly.md) и смарт-картами может различаться в зависимости от реализации интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0c369-112">The different implementations would not change the interaction between the application and the smart card; however, the interaction between the [*service provider*](../secgloss/c-gly.md) and the smart cards may differ depending on the interface's implementation.</span></span>

<span data-ttu-id="0c369-113">Набор интерфейсов, поддерживаемых смарт-картой, определяется во время введения смарт-карты (см. раздел [введение смарт-карт в систему](introducing-smart-cards-to-the-system.md)).</span><span class="sxs-lookup"><span data-stu-id="0c369-113">The set of interfaces supported by a smart card is defined during smart card introduction (see [Introducing Smart Cards to the System](introducing-smart-cards-to-the-system.md)).</span></span>

 

 
