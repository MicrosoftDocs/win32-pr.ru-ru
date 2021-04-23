---
description: В MSP-конференциях для управления участниками реализовано несколько интерфейсов, зависящих от поставщика. Эти интерфейсы предоставляются на объекте Call, если этот MSP связан с вызовом.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Интерфейсы MSP Ипконф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155890"
---
# <a name="ipconf-msp-interfaces"></a><span data-ttu-id="f04e7-104">Интерфейсы MSP Ипконф</span><span class="sxs-lookup"><span data-stu-id="f04e7-104">IPConf MSP Interfaces</span></span>

<span data-ttu-id="f04e7-105">\[ Интерфейсы MSP Ипконф недоступны для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f04e7-105">\[ The IPConf MSP Interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f04e7-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f04e7-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f04e7-107">В MSP-конференциях для управления участниками реализовано несколько интерфейсов, зависящих от поставщика.</span><span class="sxs-lookup"><span data-stu-id="f04e7-107">The IP conferencing MSP implements several provider-specific interfaces for participant control.</span></span> <span data-ttu-id="f04e7-108">Эти интерфейсы предоставляются на объекте Call, если этот MSP связан с вызовом.</span><span class="sxs-lookup"><span data-stu-id="f04e7-108">These interfaces are exposed on the call object, if this MSP is associated with the call.</span></span>

<span data-ttu-id="f04e7-109">Интерфейсы [**итпартиЦипантевент**](itparticipantevent.md) и [**иенумпартиЦипант**](ienumparticipant.md) являются изолированными объектами и перечисляются для удобства.</span><span class="sxs-lookup"><span data-stu-id="f04e7-109">The [**ITParticipantEvent**](itparticipantevent.md) and [**IEnumParticipant**](ienumparticipant.md) interfaces are stand-alone objects, and are listed here for reference convenience.</span></span>



| <span data-ttu-id="f04e7-110">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f04e7-110">Interface</span></span>                                            | <span data-ttu-id="f04e7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f04e7-111">Description</span></span>                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f04e7-112">**имултикастконтрол**</span><span class="sxs-lookup"><span data-stu-id="f04e7-112">**IMulticastControl**</span></span>](imulticastcontrol.md)       | <span data-ttu-id="f04e7-113">Позволяет приложению устанавливать и получать режим замыкания на себя ( [**\_ \_ режим многоадресной рассылки**](multicast-loopback-mode.md)) для объекта конференции многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="f04e7-113">Allows an application to set and get the loopback mode ( [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md)) for a multicast conference object.</span></span> |
| [<span data-ttu-id="f04e7-114">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="f04e7-114">**ITParticipant**</span></span>](itparticipant.md)               | <span data-ttu-id="f04e7-115">Позволяет приложению получать сведения о участниках Конференции и получать указатели на потоки, связанные с этими участниками.</span><span class="sxs-lookup"><span data-stu-id="f04e7-115">Allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>             |
| [<span data-ttu-id="f04e7-116">**итпартиЦипантконтрол**</span><span class="sxs-lookup"><span data-stu-id="f04e7-116">**ITParticipantControl**</span></span>](itparticipantcontrol.md) | <span data-ttu-id="f04e7-117">Позволяет приложению извлекать указатели на участников Конференции.</span><span class="sxs-lookup"><span data-stu-id="f04e7-117">Allows an application to retrieve pointers to the participants in a conference.</span></span>                                                                           |
| [<span data-ttu-id="f04e7-118">**итпартиЦипантевент**</span><span class="sxs-lookup"><span data-stu-id="f04e7-118">**ITParticipantEvent**</span></span>](itparticipantevent.md)     | <span data-ttu-id="f04e7-119">Позволяет приложению получать сведения о событиях, касающихся участника конференции.</span><span class="sxs-lookup"><span data-stu-id="f04e7-119">Allows an application to retrieve event information concerning a conference participant.</span></span>                                                                  |
| [<span data-ttu-id="f04e7-120">**иенумпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="f04e7-120">**IEnumParticipant**</span></span>](ienumparticipant.md)         | <span data-ttu-id="f04e7-121">Перечисляет [**итпартиЦипант**](itparticipant.md).</span><span class="sxs-lookup"><span data-stu-id="f04e7-121">Enumerates [**ITParticipant**](itparticipant.md).</span></span>                                                                                                        |



 

 

 



