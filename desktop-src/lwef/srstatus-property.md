---
title: Срстатус, свойство
description: Срстатус, свойство
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068642"
---
# <a name="srstatus-property"></a><span data-ttu-id="b3fe1-103">Срстатус, свойство</span><span class="sxs-lookup"><span data-stu-id="b3fe1-103">SRStatus Property</span></span>

<span data-ttu-id="b3fe1-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b3fe1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b3fe1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="b3fe1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b3fe1-106">Возвращает, можно ли начать речевой ввод для символа.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-106">Returns whether speech input can be started for the character.</span></span>

</dd> <dt>

<span data-ttu-id="b3fe1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="b3fe1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b3fe1-108">*Субагент. ***Символы ("*** чарактерид \* \* *"). срстатус**</span><span class="sxs-lookup"><span data-stu-id="b3fe1-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").SRStatus**</span></span>



| <span data-ttu-id="b3fe1-109">Значение</span><span class="sxs-lookup"><span data-stu-id="b3fe1-109">Value</span></span> | <span data-ttu-id="b3fe1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b3fe1-110">Description</span></span>                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3fe1-111">0</span><span class="sxs-lookup"><span data-stu-id="b3fe1-111">0</span></span>     | <span data-ttu-id="b3fe1-112">Условия поддерживают ввод речи.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="b3fe1-113">1</span><span class="sxs-lookup"><span data-stu-id="b3fe1-113">1</span></span>     | <span data-ttu-id="b3fe1-114">В этой системе нет доступных звуковых устройств ввода.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="b3fe1-115">(Обратите внимание, что это не обнаруживает, установлен ли микрофон; он может только определить, имеет ли пользователь правильно установленную звуковую карту с поддержкой ввода, с рабочим драйвером.)</span><span class="sxs-lookup"><span data-stu-id="b3fe1-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="b3fe1-116">2</span><span class="sxs-lookup"><span data-stu-id="b3fe1-116">2</span></span>     | <span data-ttu-id="b3fe1-117">Другой клиент является активным клиентом этого символа, или текущий символ не является самым верхним.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="b3fe1-118">3</span><span class="sxs-lookup"><span data-stu-id="b3fe1-118">3</span></span>     | <span data-ttu-id="b3fe1-119">Потоковый вход или выход в данный момент занят, приложение использует аудио.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-119">The audio input or output channel is currently busy, an application is using audio.</span></span>                                                                                                                                                       |
| <span data-ttu-id="b3fe1-120">4</span><span class="sxs-lookup"><span data-stu-id="b3fe1-120">4</span></span>     | <span data-ttu-id="b3fe1-121">В процессе инициализации подсистемы распознавания речи произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="b3fe1-122">Это включает в себя возможность отсутствия подсистемы распознавания речи, соответствующей языковому параметру символа.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="b3fe1-123">5</span><span class="sxs-lookup"><span data-stu-id="b3fe1-123">5</span></span>     | <span data-ttu-id="b3fe1-124">Пользователь отключил речевой ввод в расширенных параметрах символов.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-124">The user has disabled speech input in the Advanced Character Options.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="b3fe1-125">6</span><span class="sxs-lookup"><span data-stu-id="b3fe1-125">6</span></span>     | <span data-ttu-id="b3fe1-126">Произошла ошибка при проверке состояния звука, но причина ошибки не была возвращена системой.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3fe1-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3fe1-127">Remarks</span></span>

<span data-ttu-id="b3fe1-128">Это свойство возвращает условия, необходимые для поддержки речевого ввода, включая состояние звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-128">This property returns the conditions necessary to support speech input, including the status of the audio device.</span></span> <span data-ttu-id="b3fe1-129">Это свойство можно проверить перед вызовом метода [**Listen**](listen-method.md) , чтобы обеспечить его успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-129">You can check this property before you call the [**Listen**](listen-method.md) method to better ensure its success.</span></span>

<span data-ttu-id="b3fe1-130">При включении речевого ввода на странице свойств агента (дополнительные параметры символов) при запросе этого свойства будет загружена связанная подсистема, если он еще не загружен, и запущены службы речи.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-130">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying this property will load the associated engine, if it is not already loaded, and start speech services.</span></span> <span data-ttu-id="b3fe1-131">Это значит, что ключ прослушивания доступен, а TIP прослушивания автоматически воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-131">That is, the Listening key is available, and the Listening Tip is automatically displayable.</span></span> <span data-ttu-id="b3fe1-132">(Ключ прослушивания и TIP прослушивания включаются только в том случае, если они также включены в дополнительных параметрах символов.) Однако если вы запрашиваете свойство, когда речь отключена, сервер не запускает речевые службы.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-132">(The Listening key and Listening Tip are only enabled if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="b3fe1-133">Это свойство применимо только к использованию в клиентском приложении символа. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-133">This property only applies to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3fe1-134">См. также:</span><span class="sxs-lookup"><span data-stu-id="b3fe1-134">See Also</span></span>

[<span data-ttu-id="b3fe1-135">**Метод Listen**</span><span class="sxs-lookup"><span data-stu-id="b3fe1-135">**Listen method**</span></span>](listen-method.md)


 

 




