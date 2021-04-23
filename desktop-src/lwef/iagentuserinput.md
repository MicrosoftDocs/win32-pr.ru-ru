---
title: иажентусеринпут
description: иажентусеринпут
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412882"
---
# <a name="iagentuserinput"></a><span data-ttu-id="51d6d-103">иажентусеринпут</span><span class="sxs-lookup"><span data-stu-id="51d6d-103">IAgentUserInput</span></span>

<span data-ttu-id="51d6d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51d6d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="51d6d-105">Когда сервер уведомляет входной-активный клиент с [**иажентнотифисинк:: Command**](iagentnotifysink--command.md), он возвращает сведения через объект [**иажентусеринпут**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="51d6d-105">When the server notifies the input-active client with [**IAgentNotifySink::Command**](iagentnotifysink--command.md), it returns information through the [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="51d6d-106">**Иажентусеринпут** определяет интерфейс, позволяющий приложениям запрашивать эти значения.</span><span class="sxs-lookup"><span data-stu-id="51d6d-106">**IAgentUserInput** defines an interface that allows applications to query these values.</span></span>

<span data-ttu-id="51d6d-107">**Методы в порядке таблицы Vtable**</span><span class="sxs-lookup"><span data-stu-id="51d6d-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="51d6d-108">Методы Иажентусеринпут</span><span class="sxs-lookup"><span data-stu-id="51d6d-108">IAgentUserInput Methods</span></span>                                         | <span data-ttu-id="51d6d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="51d6d-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d6d-110">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="51d6d-110">**GetCount**</span></span>](iagentuserinput--getcount.md)                   | <span data-ttu-id="51d6d-111">Возвращает количество вариантов команд, возвращаемых в [**командном**](command-event.md) событии.</span><span class="sxs-lookup"><span data-stu-id="51d6d-111">Returns the number of command alternatives returned in a [**Command**](command-event.md) event.</span></span>                                         |
| [<span data-ttu-id="51d6d-112">**жетитемид**</span><span class="sxs-lookup"><span data-stu-id="51d6d-112">**GetItemID**</span></span>](iagentuserinput--getitemid.md)                 | <span data-ttu-id="51d6d-113">Возвращает идентификатор для определенной альтернативной [**команды**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="51d6d-113">Returns the ID for a specific [**Command**](command-event.md) alternative.</span></span>                                                              |
| [<span data-ttu-id="51d6d-114">**жетитемконфиденце**</span><span class="sxs-lookup"><span data-stu-id="51d6d-114">**GetItemConfidence**</span></span>](iagentuserinput--getitemconfidence.md) | <span data-ttu-id="51d6d-115">Возвращает значение свойства [**достоверности**](confidence-property.md) для определенной альтернативной [**команды**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="51d6d-115">Returns the value of the [**Confidence**](confidence-property.md) property for a specific [**Command**](command-event.md) alternative.</span></span> |
| [<span data-ttu-id="51d6d-116">**жетитемтекст**</span><span class="sxs-lookup"><span data-stu-id="51d6d-116">**GetItemText**</span></span>](iagentuserinput--getitemtext.md)             | <span data-ttu-id="51d6d-117">Возвращает значение текста [**голоса**](voice-property.md) для определенной альтернативной [**команды**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="51d6d-117">Returns the value of [**Voice**](voice-property.md) text for a specific [**Command**](command-event.md) alternative.</span></span>                   |
| [<span data-ttu-id="51d6d-118">**жеталлитемдата**</span><span class="sxs-lookup"><span data-stu-id="51d6d-118">**GetAllItemData**</span></span>](iagentuserinput--getallitemdata.md)       | <span data-ttu-id="51d6d-119">Возвращает данные для всех альтернативных [**команд**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="51d6d-119">Returns the data for all [**Command**](command-event.md) alternatives.</span></span>                                                                  |



 

 

 