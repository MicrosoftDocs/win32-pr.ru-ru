---
title: Иажентчарактерекс Жетсрстатус
description: Иажентчарактерекс Жетсрстатус
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067788"
---
# <a name="iagentcharacterexgetsrstatus"></a><span data-ttu-id="57c3d-103">Иажентчарактерекс:: Жетсрстатус</span><span class="sxs-lookup"><span data-stu-id="57c3d-103">IAgentCharacterEx::GetSRStatus</span></span>

<span data-ttu-id="57c3d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="57c3d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

<span data-ttu-id="57c3d-105">Возвращает состояние условия, необходимого для поддержки речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="57c3d-105">Retrieves the status of the condition necessary to support speech input.</span></span>

-   <span data-ttu-id="57c3d-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="57c3d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="57c3d-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*плстатус*</span><span class="sxs-lookup"><span data-stu-id="57c3d-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="57c3d-108">Адрес переменной, принимающей одно из следующих значений параметра State:</span><span class="sxs-lookup"><span data-stu-id="57c3d-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="57c3d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="57c3d-109">Value</span></span>                                                                               | <span data-ttu-id="57c3d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="57c3d-110">Description</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57c3d-111">**долговременное состояние беззнакового** **прослушивания \_ \_ канлистен = 0;**</span><span class="sxs-lookup"><span data-stu-id="57c3d-111">**const unsigned long** **LISTEN\_STATUS\_CANLISTEN = 0;**</span></span><br/>               | <span data-ttu-id="57c3d-112">Условия поддерживают ввод речи.</span><span class="sxs-lookup"><span data-stu-id="57c3d-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="57c3d-113">**постоянное состояние беззнакового прослушиваемого неподписанного** **\_ состояния \_ : 1;**</span><span class="sxs-lookup"><span data-stu-id="57c3d-113">**const unsigned long** **LISTEN\_STATUS\_NOAUDIO = 1;**</span></span><br/>                 | <span data-ttu-id="57c3d-114">В этой системе нет доступных звуковых устройств ввода.</span><span class="sxs-lookup"><span data-stu-id="57c3d-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="57c3d-115">(Обратите внимание, что это не обнаруживает, установлен ли микрофон; он может только определить, имеет ли пользователь правильно установленную звуковую карту с поддержкой ввода, с рабочим драйвером.)</span><span class="sxs-lookup"><span data-stu-id="57c3d-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="57c3d-116">**долговременное состояние беззнакового** **прослушивания \_ \_ ноттопмост = 2;**</span><span class="sxs-lookup"><span data-stu-id="57c3d-116">**const unsigned long** **LISTEN\_STATUS\_NOTTOPMOST = 2;**</span></span><br/>              | <span data-ttu-id="57c3d-117">Другой клиент является активным клиентом этого символа, или текущий символ не является самым верхним.</span><span class="sxs-lookup"><span data-stu-id="57c3d-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="57c3d-118">**долговременное состояние беззнакового** **прослушивания \_ \_ кантопенаудио = 3;**</span><span class="sxs-lookup"><span data-stu-id="57c3d-118">**const unsigned long** **LISTEN\_STATUS\_CANTOPENAUDIO = 3;**</span></span><br/>           | <span data-ttu-id="57c3d-119">Канал аудио ввода или вывода сейчас занят, другое приложение использует звук.</span><span class="sxs-lookup"><span data-stu-id="57c3d-119">The audio input or output channel is currently busy, some other application is using audio.</span></span>                                                                                                                                               |
| <span data-ttu-id="57c3d-120">**долговременное состояние беззнакового** **прослушивания \_ \_ каулднтинитиализеспич = 4;**</span><span class="sxs-lookup"><span data-stu-id="57c3d-120">**const unsigned long** **LISTEN\_STATUS\_COULDNTINITIALIZESPEECH = 4;**</span></span><br/> | <span data-ttu-id="57c3d-121">В процессе инициализации подсистемы распознавания речи произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="57c3d-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="57c3d-122">Это включает в себя возможность отсутствия подсистемы распознавания речи, соответствующей языковому параметру символа.</span><span class="sxs-lookup"><span data-stu-id="57c3d-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="57c3d-123">**долговременное состояние беззнакового** **прослушивания \_ \_ спичдисаблед = 5;**</span><span class="sxs-lookup"><span data-stu-id="57c3d-123">**const unsigned long** **LISTEN\_STATUS\_SPEECHDISABLED = 5;**</span></span><br/>          | <span data-ttu-id="57c3d-124">Пользователь отключил речевой ввод в окне "Дополнительные параметры символов".</span><span class="sxs-lookup"><span data-stu-id="57c3d-124">The user has disabled speech input in the Advanced Character Options window.</span></span>                                                                                                                                                              |
| <span data-ttu-id="57c3d-125">**Неподписанное длинное состояние беззнакового** **состояния прослушивания \_ \_ = 6;**</span><span class="sxs-lookup"><span data-stu-id="57c3d-125">**const unsigned long** **LISTEN\_STATUS\_ERROR = 6;**</span></span><br/>                   | <span data-ttu-id="57c3d-126">Произошла ошибка при проверке состояния звука, но причина ошибки не была возвращена системой.</span><span class="sxs-lookup"><span data-stu-id="57c3d-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

<span data-ttu-id="57c3d-127">Эта функция позволяет запрашивать, поддерживают ли текущие условия входные данные распознавания речи, включая состояние звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="57c3d-127">This function enables you to query whether current conditions support speech recognition input, including the status of the audio device.</span></span> <span data-ttu-id="57c3d-128">Если приложение использует метод [**иажентчарактерекс:: Listen**](iagentcharacterex--listen.md) , эту функцию можно использовать, чтобы обеспечить успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="57c3d-128">If your application uses the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method, you can use this function to better ensure that the call will succeed.</span></span> <span data-ttu-id="57c3d-129">Вызов этого метода также загружает модуль распознавания речи, если он еще не загружен.</span><span class="sxs-lookup"><span data-stu-id="57c3d-129">Calling this method also loads the speech engine if it is not already loaded.</span></span> <span data-ttu-id="57c3d-130">Однако он не включает режим прослушивания.</span><span class="sxs-lookup"><span data-stu-id="57c3d-130">However, it does not turn on Listening mode.</span></span>

<span data-ttu-id="57c3d-131">При включении речевого ввода на странице свойств агента (дополнительные параметры символов) запрос состояния приведет к загрузке связанного обработчика (если он еще не загружен) и запуск служб речи.</span><span class="sxs-lookup"><span data-stu-id="57c3d-131">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying the status will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="57c3d-132">Это значит, что ключ прослушивания доступен и подсказка прослушивания доступна для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="57c3d-132">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="57c3d-133">(Ключ прослушивания и TIP прослушивания включены, только если они также включены в дополнительных параметрах символов.) Однако если вы запрашиваете свойство, когда речь отключена, сервер не запускает речевые службы.</span><span class="sxs-lookup"><span data-stu-id="57c3d-133">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="57c3d-134">Эта функция возвращает только параметр для использования символа в клиентском приложении. параметр не отражает другие клиенты символов или другие символы клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="57c3d-134">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

 

 





