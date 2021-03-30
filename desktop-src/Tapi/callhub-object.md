---
description: Объект Каллхуб представляет стороннее представление многокомпонентного вызова.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Объект Каллхуб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998866"
---
# <a name="callhub-object"></a><span data-ttu-id="388dc-103">Объект Каллхуб</span><span class="sxs-lookup"><span data-stu-id="388dc-103">CallHub Object</span></span>

<span data-ttu-id="388dc-104">Объект Каллхуб представляет стороннее представление многокомпонентного вызова.</span><span class="sxs-lookup"><span data-stu-id="388dc-104">The CallHub object represents a third-party view of a multiparty call.</span></span> <span data-ttu-id="388dc-105">Связанные интерфейсы и методы получают и задают сведения о концентраторе, например, является ли он активным.</span><span class="sxs-lookup"><span data-stu-id="388dc-105">The associated interfaces and methods get and set information concerning the hub, such as whether it is active.</span></span> <span data-ttu-id="388dc-106">С помощью объекта Каллхуб пользователь с необходимой защитой может обнаруживать и потенциально управлять другими участниками в вызове.</span><span class="sxs-lookup"><span data-stu-id="388dc-106">Using the CallHub object, a user with the required security can discover and potentially control other participants in a call.</span></span>

<span data-ttu-id="388dc-107">Объект Каллхуб не может быть создан напрямую приложением.</span><span class="sxs-lookup"><span data-stu-id="388dc-107">A CallHub object cannot be created directly by an application.</span></span> <span data-ttu-id="388dc-108">Объект Каллхуб создается косвенно при получении входящего вызова через TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="388dc-108">A CallHub object is created indirectly when an incoming call is received through TAPI 3.</span></span>

<span data-ttu-id="388dc-109">TAPI 3 использует поставщики услуг TAPI для предоставления необходимых сведений о вызовах для реализации с помощью объекта Каллхуб.</span><span class="sxs-lookup"><span data-stu-id="388dc-109">TAPI 3 relies on TAPI service providers to provide the necessary information about calls to implement using the CallHub object.</span></span> <span data-ttu-id="388dc-110">Так как не все поставщики услуг предоставляют эти сведения, а не все оборудование поддерживает отслеживание концентратора вызовов, сведения о других пользователях в подключении могут быть ограничены или не существуют.</span><span class="sxs-lookup"><span data-stu-id="388dc-110">Because not all service providers provide this information, and not all hardware supports call hub tracking, the information available about the other users in the connection may be limited or nonexistent.</span></span>

<span data-ttu-id="388dc-111">В примере [создания простого](create-a-simple-conference.md) примера кода конференции показано использование объекта каллхуб.</span><span class="sxs-lookup"><span data-stu-id="388dc-111">The [Create a Simple Conference](create-a-simple-conference.md) code example illustrates use of a CallHub object.</span></span>

<span data-ttu-id="388dc-112">Список всех интерфейсов, связанных с объектом Каллхуб, см. в разделе [интерфейсы объекта каллхуб](callhub-object-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="388dc-112">See [CallHub Object Interfaces](callhub-object-interfaces.md) for a list of all interfaces associated with the CallHub object.</span></span>

 

 



