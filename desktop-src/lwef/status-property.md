---
title: Свойство Status
description: Свойство Status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700601"
---
# <a name="status-property"></a><span data-ttu-id="9fc5f-103">Свойство Status</span><span class="sxs-lookup"><span data-stu-id="9fc5f-103">Status Property</span></span>

<span data-ttu-id="9fc5f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9fc5f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9fc5f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="9fc5f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9fc5f-106">Возвращает состояние канала вывода звука.</span><span class="sxs-lookup"><span data-stu-id="9fc5f-106">Returns the status of the audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="9fc5f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9fc5f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9fc5f-108">*агент \* \* *. Аудиуутпут. status**</span><span class="sxs-lookup"><span data-stu-id="9fc5f-108">*agent\*\*\*.AudioOutput.Status*\*</span></span>



| <span data-ttu-id="9fc5f-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9fc5f-109">Value</span></span> | <span data-ttu-id="9fc5f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9fc5f-110">Description</span></span>                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc5f-111">0</span><span class="sxs-lookup"><span data-stu-id="9fc5f-111">0</span></span>     | <span data-ttu-id="9fc5f-112">Канал звукового вывода доступен (не занят).</span><span class="sxs-lookup"><span data-stu-id="9fc5f-112">The audio output channel is available (not busy).</span></span>                                                                 |
| <span data-ttu-id="9fc5f-113">1</span><span class="sxs-lookup"><span data-stu-id="9fc5f-113">1</span></span>     | <span data-ttu-id="9fc5f-114">Звуковые выходные данные не поддерживаются; Например, из-за отсутствия звуковой платы.</span><span class="sxs-lookup"><span data-stu-id="9fc5f-114">There is no support for audio output; for example, because there is no sound card.</span></span>                                |
| <span data-ttu-id="9fc5f-115">2</span><span class="sxs-lookup"><span data-stu-id="9fc5f-115">2</span></span>     | <span data-ttu-id="9fc5f-116">Не удается открыть канал вывода звука (занят); Например, так как другое приложение воспроизводит звук.</span><span class="sxs-lookup"><span data-stu-id="9fc5f-116">The audio output channel can't be opened (is busy); for example, because some other application is playing audio.</span></span> |
| <span data-ttu-id="9fc5f-117">3</span><span class="sxs-lookup"><span data-stu-id="9fc5f-117">3</span></span>     | <span data-ttu-id="9fc5f-118">Канал вывода звука занят, так как сервер обрабатывает речевой ввод пользователя.</span><span class="sxs-lookup"><span data-stu-id="9fc5f-118">The audio output channel is busy because the server is processing user speech input.</span></span>                              |
| <span data-ttu-id="9fc5f-119">4</span><span class="sxs-lookup"><span data-stu-id="9fc5f-119">4</span></span>     | <span data-ttu-id="9fc5f-120">Канал вывода звука занят, так как в настоящий момент символ говорит.</span><span class="sxs-lookup"><span data-stu-id="9fc5f-120">The audio output channel is busy because a character is currently speaking.</span></span>                                       |
| <span data-ttu-id="9fc5f-121">5</span><span class="sxs-lookup"><span data-stu-id="9fc5f-121">5</span></span>     | <span data-ttu-id="9fc5f-122">Канал вывода звука не занят, но ожидает ввода речи пользователем.</span><span class="sxs-lookup"><span data-stu-id="9fc5f-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                    |
| <span data-ttu-id="9fc5f-123">6</span><span class="sxs-lookup"><span data-stu-id="9fc5f-123">6</span></span>     | <span data-ttu-id="9fc5f-124">Возникла другая (неизвестная) проблема при попытке доступа к каналу вывода звука.</span><span class="sxs-lookup"><span data-stu-id="9fc5f-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fc5f-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fc5f-125">Remarks</span></span>

<span data-ttu-id="9fc5f-126">Этот параметр позволяет клиентскому приложению запрашивать канал вывода звука, возвращая целочисленное значение, которое указывает состояние канала вывода звука.</span><span class="sxs-lookup"><span data-stu-id="9fc5f-126">This setting enables your client application to query the audio output channel, returning an Integer value that indicates the status of the audio output channel.</span></span> <span data-ttu-id="9fc5f-127">Его можно использовать, чтобы определить, подходит ли символ для диктовки или нужно ли попытаться включить режим прослушивания (с помощью метода [**Listen**](listen-method.md) ).</span><span class="sxs-lookup"><span data-stu-id="9fc5f-127">You can use this to determine whether it is appropriate to have your character speak or whether it is appropriate to try to turn on Listening mode (using the [**Listen**](listen-method.md) method).</span></span>

## <a name="see-also"></a><span data-ttu-id="9fc5f-128">См. также:</span><span class="sxs-lookup"><span data-stu-id="9fc5f-128">See Also</span></span>

[<span data-ttu-id="9fc5f-129">**Событие Листенкомплете**</span><span class="sxs-lookup"><span data-stu-id="9fc5f-129">**ListenComplete event**</span></span>](listencomplete-event.md)


 

 




