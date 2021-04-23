---
description: ATM применяется как к окружениям локальной сети, так и к глобальной сети.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Приложение Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711376"
---
# <a name="winsock-atm-annex"></a><span data-ttu-id="8194d-103">Приложение Winsock ATM</span><span class="sxs-lookup"><span data-stu-id="8194d-103">Winsock ATM Annex</span></span>

<span data-ttu-id="8194d-104">ATM применяется как к окружениям локальной сети, так и к глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="8194d-104">ATM is applicable to both LAN and WAN environments.</span></span> <span data-ttu-id="8194d-105">ATM-сеть одновременно транспортают широкий спектр сетевых трафика — голоса, данных, изображений и видео.</span><span class="sxs-lookup"><span data-stu-id="8194d-105">An ATM network simultaneously transports a wide variety of network traffic — voice, data, image, and video.</span></span> <span data-ttu-id="8194d-106">Она предоставляет пользователям гарантированное качество обслуживания для каждого виртуального канала (VC).</span><span class="sxs-lookup"><span data-stu-id="8194d-106">It provides users with a guaranteed quality of service on a per-virtual channel (VC) basis.</span></span>



| <span data-ttu-id="8194d-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="8194d-107">Element</span></span>          | <span data-ttu-id="8194d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8194d-108">Description</span></span>                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8194d-109">Имена протоколов</span><span class="sxs-lookup"><span data-stu-id="8194d-109">Protocol name(s)</span></span> | <span data-ttu-id="8194d-110">АТМПРОТО \_ AAL5, атмпрото \_ аалусер</span><span class="sxs-lookup"><span data-stu-id="8194d-110">ATMPROTO\_AAL5, ATMPROTO\_AALUSER</span></span>                                                                                                                           |
| <span data-ttu-id="8194d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8194d-111">Description</span></span>      | <span data-ttu-id="8194d-112">ATM AAL5 предоставляет транспортную службу, ориентированную на соединение, сохранение границ сообщений и гарантированное качество обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8194d-112">ATM AAL5 provides a transport service that is connection oriented, message-boundary preserved, and QOS guaranteed.</span></span> <span data-ttu-id="8194d-113">АТМПРОТО \_ аалусер — это определяемый пользователем AAL.</span><span class="sxs-lookup"><span data-stu-id="8194d-113">ATMPROTO\_AALUSER is a user-defined AAL.</span></span> |
| <span data-ttu-id="8194d-114">Семейство адресов</span><span class="sxs-lookup"><span data-stu-id="8194d-114">Address family</span></span>   | <span data-ttu-id="8194d-115">AF \_ ATM</span><span class="sxs-lookup"><span data-stu-id="8194d-115">AF\_ATM</span></span>                                                                                                                                                     |
| <span data-ttu-id="8194d-116">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="8194d-116">Header file</span></span>      | <span data-ttu-id="8194d-117">Ws2atm. h</span><span class="sxs-lookup"><span data-stu-id="8194d-117">Ws2atm.h</span></span>                                                                                                                                                    |



 

<span data-ttu-id="8194d-118">В этом разделе описываются расширения асинхронной пересылки (ATM), необходимые для поддержки собственных служб ATM, как предоставленные и указанные в спецификации сетевого интерфейса пользователя (UNI) ATM Forum версии 3. x (3,0 и 3,1).</span><span class="sxs-lookup"><span data-stu-id="8194d-118">This section describes the Asynchronous Transfer Mode (ATM)-specific extensions needed to support the native ATM services as exposed and specified in the ATM Forum User Network Interface (UNI) specification version 3.x (3.0 and 3.1).</span></span> <span data-ttu-id="8194d-119">Этот документ поддерживает тип AAL 5 (режим сообщения) и определяемый пользователем AAL.</span><span class="sxs-lookup"><span data-stu-id="8194d-119">This document supports AAL type 5 (message mode) and user-defined AAL.</span></span> <span data-ttu-id="8194d-120">Будущие версии этого документа будут поддерживать другие типы AAL, а также UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="8194d-120">Future versions of this document will support other types of AAL as well as UNI 4.0.</span></span>

 

 



