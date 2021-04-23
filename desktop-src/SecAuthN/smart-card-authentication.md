---
description: Проверка подлинности смарт-карты
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Проверка подлинности смарт-карты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651050"
---
# <a name="smart-card-authentication"></a><span data-ttu-id="fa822-103">Проверка подлинности смарт-карты</span><span class="sxs-lookup"><span data-stu-id="fa822-103">Smart Card Authentication</span></span>

<span data-ttu-id="fa822-104">Основные компоненты [*подсистемы смарт-карт*](../secgloss/s-gly.md) основаны на стандартах PC/SC (см. спецификации в [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ).</span><span class="sxs-lookup"><span data-stu-id="fa822-104">The basic parts of the [*smart card subsystem*](../secgloss/s-gly.md) are based on PC/SC standards (see the specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)).</span></span> <span data-ttu-id="fa822-105">Ниже перечислены основные компоненты.</span><span class="sxs-lookup"><span data-stu-id="fa822-105">These basic parts include:</span></span>

-   <span data-ttu-id="fa822-106">[*Диспетчер ресурсов*](../secgloss/r-gly.md) , использующий API Windows.</span><span class="sxs-lookup"><span data-stu-id="fa822-106">A [*resource manager*](../secgloss/r-gly.md) that uses a Windows API.</span></span>
-   <span data-ttu-id="fa822-107">[*Пользовательский интерфейс*](../secgloss/u-gly.md) , работающий с диспетчером ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa822-107">A [*user interface*](../secgloss/u-gly.md) (UI) that works with the resource manager.</span></span>
-   <span data-ttu-id="fa822-108">Несколько базовых [*поставщиков служб*](../secgloss/s-gly.md) , предоставляющих доступ к конкретным службам.</span><span class="sxs-lookup"><span data-stu-id="fa822-108">Several base [*service providers*](../secgloss/s-gly.md) that provide access to specific services.</span></span> <span data-ttu-id="fa822-109">В отличие от Windows API диспетчера ресурсов, поставщики служб используют модель COM-интерфейса для предоставления служб [*смарт-карт*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fa822-109">In contrast to the resource manager's Windows API, service providers use a COM interface model to provide [*smart card*](../secgloss/s-gly.md) services.</span></span>

<span data-ttu-id="fa822-110">На следующем рисунке показаны связи между этими частями в общей архитектуре смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="fa822-110">The following illustration shows the relationships of these parts in the overall smart card architecture.</span></span>

![Архитектура смарт-карт](images/smartovr2a.png)

<span data-ttu-id="fa822-112">Сведения о том, как [*подсистема смарт-карт*](../secgloss/s-gly.md) работает с другими службами, доступными в Microsoft Internet Security Framework, см. в разделе [отношение к другим службам](relation-to-other-services.md).</span><span class="sxs-lookup"><span data-stu-id="fa822-112">For information about how the [*smart card subsystem*](../secgloss/s-gly.md) works with other services available in the Microsoft Internet Security Framework, see [Relation to Other Services](relation-to-other-services.md).</span></span>

<span data-ttu-id="fa822-113">Дополнительные сведения о проверке подлинности смарт-карт см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="fa822-113">For information about smart card authentication, see the following topics.</span></span>



| <span data-ttu-id="fa822-114">Разделы</span><span class="sxs-lookup"><span data-stu-id="fa822-114">Topics</span></span>                                                                      | <span data-ttu-id="fa822-115">Содержимое</span><span class="sxs-lookup"><span data-stu-id="fa822-115">Contents</span></span>                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa822-116">Основные понятия смарт-карт</span><span class="sxs-lookup"><span data-stu-id="fa822-116">Smart Card Concepts</span></span>](smart-card-concepts.md)<br/>                   | <span data-ttu-id="fa822-117">Основные понятия и описание взаимодействия между пользователями и смарт-картами.</span><span class="sxs-lookup"><span data-stu-id="fa822-117">Basic concepts and description of the interaction between users and smart cards.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="fa822-118">Смарт-карта диспетчер ресурсов</span><span class="sxs-lookup"><span data-stu-id="fa822-118">Smart Card Resource Manager</span></span>](smart-card-resource-manager.md)<br/>   | <span data-ttu-id="fa822-119">Сведения об API диспетчера ресурсов, который управляет доступом к [*читателям*](../secgloss/r-gly.md) и [*смарт-картам*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fa822-119">Information about the resource manager API, which manages the access to [*readers*](../secgloss/r-gly.md) and to [*smart cards*](../secgloss/s-gly.md).</span></span><br/> |
| [<span data-ttu-id="fa822-120">Пользовательский интерфейс смарт-карты</span><span class="sxs-lookup"><span data-stu-id="fa822-120">Smart Card User Interface</span></span>](smart-card-user-interface.md)<br/>       | <span data-ttu-id="fa822-121">Сведения о [*общем диалоговом окне смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fa822-121">Information about the [*smart card common dialog box*](../secgloss/s-gly.md).</span></span><br/>                                                                                   |
| [<span data-ttu-id="fa822-122">Поставщики услуг смарт-карт</span><span class="sxs-lookup"><span data-stu-id="fa822-122">Smart Card Service Providers</span></span>](smart-card-service-providers.md)<br/> | <span data-ttu-id="fa822-123">Сведения о интерфейсах, командах и оболочках, обеспечивающих возможности смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="fa822-123">Information about interfaces, commands, and wrappers that provide smart card capabilities.</span></span><br/>                                                                                                                                              |



 

<span data-ttu-id="fa822-124">Кроме того, текущие разработки смарт-карт Майкрософт можно найти по адресу [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="fa822-124">Additionally, current Microsoft smart card developments can be found at [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx).</span></span>

 

 
