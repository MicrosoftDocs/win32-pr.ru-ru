---
title: Иажентаудиуутпутпропертиесекс
description: Иажентаудиуутпутпропертиесекс
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380748"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="8d57b-103">Иажентаудиуутпутпропертиесекс::/Status</span><span class="sxs-lookup"><span data-stu-id="8d57b-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="8d57b-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8d57b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="8d57b-105">Получает состояние канала звука.</span><span class="sxs-lookup"><span data-stu-id="8d57b-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="8d57b-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8d57b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8d57b-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*плстатус*</span><span class="sxs-lookup"><span data-stu-id="8d57b-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="8d57b-108">Состояние канала вывода звука, которое может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="8d57b-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="8d57b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="8d57b-109">Value</span></span>                                                                         | <span data-ttu-id="8d57b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8d57b-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d57b-111">**постоянное состояние неподписанного короткого звука const** **\_ \_ = 0;**</span><span class="sxs-lookup"><span data-stu-id="8d57b-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="8d57b-112">Канал звукового вывода доступен (не занят).</span><span class="sxs-lookup"><span data-stu-id="8d57b-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="8d57b-113">**const неподписанное короткое** **звуковое состояние без знака \_ \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="8d57b-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="8d57b-114">Звуковые выходные данные не поддерживаются; Например, из-за отсутствия звуковой платы.</span><span class="sxs-lookup"><span data-stu-id="8d57b-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="8d57b-115">**const неподписанное короткое** **звуковое \_ состояние \_ кантопенаудио = 2;**</span><span class="sxs-lookup"><span data-stu-id="8d57b-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="8d57b-116">Не удается открыть канал вывода звука (занят); Например, так как другое приложение воспроизводит звук.</span><span class="sxs-lookup"><span data-stu-id="8d57b-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="8d57b-117">**const неподписанное короткое** **\_ состояние звука \_ усерспеакинг = 3;**</span><span class="sxs-lookup"><span data-stu-id="8d57b-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="8d57b-118">Канал вывода звука занят, так как сервер обрабатывает речевой ввод пользователя</span><span class="sxs-lookup"><span data-stu-id="8d57b-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="8d57b-119">**const неподписанное короткое** **\_ состояние звука \_ чарактерспеакинг = 4;**</span><span class="sxs-lookup"><span data-stu-id="8d57b-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="8d57b-120">Канал вывода звука занят, так как в настоящий момент символ говорит.</span><span class="sxs-lookup"><span data-stu-id="8d57b-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="8d57b-121">**const неподписанное короткое** **\_ состояние звука \_ сроверридеабле = 5;**</span><span class="sxs-lookup"><span data-stu-id="8d57b-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="8d57b-122">Канал вывода звука не занят, но ожидает ввода речи пользователем.</span><span class="sxs-lookup"><span data-stu-id="8d57b-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="8d57b-123">**const неподписанное короткое** **\_ состояние звука \_ — 6;**</span><span class="sxs-lookup"><span data-stu-id="8d57b-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="8d57b-124">Возникла другая (неизвестная) проблема при попытке доступа к каналу вывода звука.</span><span class="sxs-lookup"><span data-stu-id="8d57b-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="8d57b-125">Этот параметр позволяет клиентскому приложению запрашивать состояние канала вывода звука.</span><span class="sxs-lookup"><span data-stu-id="8d57b-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="8d57b-126">С помощью этого метода можно определить, следует ли говорить, что ваш символ говорит, или попытаться включить режим прослушивания (с помощью **иажентчарактерекс:: Listen**).</span><span class="sxs-lookup"><span data-stu-id="8d57b-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using **IAgentCharacterEx::Listen**).</span></span>

 

 





