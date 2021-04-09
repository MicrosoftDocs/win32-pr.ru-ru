---
title: Использование функции PlaySound для воспроизведения системных звуков
description: Использование функции PlaySound для воспроизведения системных звуков
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- волна Audio, функция PlaySound
- звуковая волна, воспроизведение системных звуков
- звуковая волна, звуковые события
- Функция PlaySound, воспроизведение системных звуков
- Функция PlaySound, звуковые события
- Воспроизведение звуковых сигналов звуковой системы
- звуковые события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890636"
---
# <a name="using-playsound-to-play-system-sounds"></a><span data-ttu-id="58f73-110">Использование функции PlaySound для воспроизведения системных звуков</span><span class="sxs-lookup"><span data-stu-id="58f73-110">Using PlaySound to Play System Sounds</span></span>

<span data-ttu-id="58f73-111">Функция [**PlaySound**](/previous-versions//dd743680(v=vs.85)) также будет воспроизводить в реестре звуки, на которые ссылается keyName.</span><span class="sxs-lookup"><span data-stu-id="58f73-111">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function will also play sounds referred to by a keyname in the registry.</span></span> <span data-ttu-id="58f73-112">Пользователи могут назначать собственные звуки системным оповещениям и предупреждениям, а также действиям пользователей, например нажатием кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="58f73-112">Users can assign their own sounds to system alerts and warnings, or to user actions, such as a mouse button click.</span></span> <span data-ttu-id="58f73-113">Звуки, связанные с системными предупреждениями и предупреждениями, называются *звуковыми событиями*.</span><span class="sxs-lookup"><span data-stu-id="58f73-113">Sounds that are associated with system alerts and warnings are called *sound events*.</span></span>

<span data-ttu-id="58f73-114">Чтобы воспроизвести звуковое событие, вызовите **PlaySound** с параметром *псзсаунд* , указывающим на строку, содержащую имя записи реестра, определяющей звук.</span><span class="sxs-lookup"><span data-stu-id="58f73-114">To play a sound event, call **PlaySound** with the *pszSound* parameter pointing to a string containing the name of the registry entry that identifies the sound.</span></span> <span data-ttu-id="58f73-115">Например, чтобы воспроизвести звук, связанный с записью "Маусекликк", и подождать завершения воспроизведения звука перед возвратом, используйте следующую инструкцию:</span><span class="sxs-lookup"><span data-stu-id="58f73-115">For example, to play the sound associated with the "MouseClick" entry and to wait for the sound to complete before returning, use the following statement:</span></span>


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



<span data-ttu-id="58f73-116">Если указанная запись реестра или звуковой файл аудио-файла не существует или файл не умещается в доступную память, то значение **PlaySound** воспроизводит системный звук по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="58f73-116">If the specified registry entry or the waveform-audio file it identifies does not exist, or if the file does not fit into the available memory, **PlaySound** plays the default system sound.</span></span>

<span data-ttu-id="58f73-117">События звука, предопределенные системой, могут различаться в зависимости от платформы.</span><span class="sxs-lookup"><span data-stu-id="58f73-117">The sound events that are predefined by the system can vary with the platform.</span></span> <span data-ttu-id="58f73-118">В следующем списке приводятся звуковые события, определенные для всех реализаций API Win32.</span><span class="sxs-lookup"><span data-stu-id="58f73-118">The following list gives the sound events that are defined for all implementations of the Win32 API:</span></span>

-   <span data-ttu-id="58f73-119">системастериск</span><span class="sxs-lookup"><span data-stu-id="58f73-119">SystemAsterisk</span></span>
-   <span data-ttu-id="58f73-120">системекскламатион</span><span class="sxs-lookup"><span data-stu-id="58f73-120">SystemExclamation</span></span>
-   <span data-ttu-id="58f73-121">SystemExit</span><span class="sxs-lookup"><span data-stu-id="58f73-121">SystemExit</span></span>
-   <span data-ttu-id="58f73-122">системханд</span><span class="sxs-lookup"><span data-stu-id="58f73-122">SystemHand</span></span>
-   <span data-ttu-id="58f73-123">системкуестион</span><span class="sxs-lookup"><span data-stu-id="58f73-123">SystemQuestion</span></span>
-   <span data-ttu-id="58f73-124">системстарт</span><span class="sxs-lookup"><span data-stu-id="58f73-124">SystemStart</span></span>

<span data-ttu-id="58f73-125">Если приложение регистрирует собственные события звука, пользователь может настроить событие Sound с помощью стандартного интерфейса панели управления.</span><span class="sxs-lookup"><span data-stu-id="58f73-125">If an application registers its own sound events, the user can configure the sound event by using the standard Control Panel interface.</span></span> <span data-ttu-id="58f73-126">Приложение должно зарегистрировать звуковое событие с помощью стандартных функций реестра. Дополнительные сведения см. в разделе [Реестр](../sysinfo/registry.md).</span><span class="sxs-lookup"><span data-stu-id="58f73-126">The application should register the sound event by using the standard registry functions; for more information, see [Registry](../sysinfo/registry.md).</span></span> <span data-ttu-id="58f73-127">Записи принадлежат к той же позиции в иерархии реестра, что и остальные события звука.</span><span class="sxs-lookup"><span data-stu-id="58f73-127">The entries belong at the same position in the registry hierarchy as the rest of the sound events.</span></span> <span data-ttu-id="58f73-128">Это расположение зависит от реализации Win32.</span><span class="sxs-lookup"><span data-stu-id="58f73-128">This position varies with the Win32 implementation.</span></span> <span data-ttu-id="58f73-129">Соответствующее значение данных также зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="58f73-129">The appropriate data value also varies with the implementation.</span></span>

<span data-ttu-id="58f73-130">Функция [**сндплайсаунд**](/previous-versions//dd798676(v=vs.85)) всегда ищет в реестре *лпсзсаунд* сопоставления keyName перед попыткой загрузить файл с таким именем.</span><span class="sxs-lookup"><span data-stu-id="58f73-130">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function always searches the registry for a keyname matching *lpszSound* before attempting to load a file with this name.</span></span> <span data-ttu-id="58f73-131">Функция [**PlaySound**](/previous-versions//dd743680(v=vs.85)) принимает флаги, указывающие расположение звука.</span><span class="sxs-lookup"><span data-stu-id="58f73-131">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function accepts flags that specify the location of the sound.</span></span>

 

 