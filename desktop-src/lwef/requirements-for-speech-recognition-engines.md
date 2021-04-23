---
title: Требования для модулей распознавания речи
description: Требования для модулей распознавания речи
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986727"
---
# <a name="requirements-for-speech-recognition-engines"></a><span data-ttu-id="0b858-103">Требования для модулей распознавания речи</span><span class="sxs-lookup"><span data-stu-id="0b858-103">Requirements for Speech Recognition Engines</span></span>

<span data-ttu-id="0b858-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0b858-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0b858-105">Подсистема распознавания речи также должна быть полностью совместимой командой и контролем (C&C) в соответствии с SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="0b858-105">A speech recognition engine must also be a fully compliant Command and Control (C&C) engine according to SAPI 4.0.</span></span> <span data-ttu-id="0b858-106">Он должен поддерживать несколько грамматик в двоичном формате, описанных в спецификации, и позволяет активировать или деактивировать эти грамматики в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="0b858-106">It must support multiple grammars in the binary format described in the specification and allow those grammars to be activated or deactivated in real time.</span></span>

<span data-ttu-id="0b858-107">Обратите внимание, что SAPI 4,0 требует, чтобы модули распознавания речи поддерживали широкие символы, интерфейсы Юникода.</span><span class="sxs-lookup"><span data-stu-id="0b858-107">Note that SAPI 4.0 requires that speech recognition engines support the wide character, Unicode interfaces.</span></span> <span data-ttu-id="0b858-108">Однако при поддержке этих интерфейсов подсистема не должна зависеть от преобразования данных в Юникоде в ANSI, так как ядро может работать неправильно в некоторых системах.</span><span class="sxs-lookup"><span data-stu-id="0b858-108">However, in supporting these interfaces, the engine should not depend on converting Unicode data to ANSI, as the engine may not function correctly on some systems.</span></span> <span data-ttu-id="0b858-109">Например, японский модуль, преобразующий Юникод в ANSI, может не работать в системе Microsoft Windows 95 на английском языке.</span><span class="sxs-lookup"><span data-stu-id="0b858-109">For example, a Japanese engine that converts Unicode to ANSI may not work on an English-language Microsoft Windows 95 system.</span></span>

<span data-ttu-id="0b858-110">Кроме того, чтобы считаться совместимым с Microsoft Agent, обработчик должен вернуть объекты Results после успешного распознавания фразы (через Исрграмнотифисинкв::P Храсефиниш).</span><span class="sxs-lookup"><span data-stu-id="0b858-110">In addition, to be considered Microsoft Agent-compliant, the engine must return results objects upon the successful recognition of a phrase (through ISRGramNotifySinkW::PhraseFinish).</span></span> <span data-ttu-id="0b858-111">Эти объекты результатов должны поддерживать Исрресбасик в соответствии с требованиями спецификации.</span><span class="sxs-lookup"><span data-stu-id="0b858-111">These results objects must support ISRResBasic, as the specification requires.</span></span> <span data-ttu-id="0b858-112">Кроме того, они должны поддерживать Исрресскоре.</span><span class="sxs-lookup"><span data-stu-id="0b858-112">In addition, they should support ISRResScore.</span></span> <span data-ttu-id="0b858-113">Несмотря на то, что Microsoft Agent работает с ядром, поддерживающей только Исрресбасик, или даже с ядром, которая не возвращает никаких объектов результатов, производительность обычно значительно снижается с учетом таких ядер.</span><span class="sxs-lookup"><span data-stu-id="0b858-113">Although Microsoft Agent will run with an engine that supports only ISRResBasic, or even with an engine that returns no results objects whatsoever, performance will usually be significantly poorer with such engines.</span></span> <span data-ttu-id="0b858-114">Многие приложения используют значения достоверности, предоставляемые ядром, для управления их реакцией на различные команды.</span><span class="sxs-lookup"><span data-stu-id="0b858-114">Many applications use the confidence values provided by the engine to control how they respond to various commands.</span></span>

 

 




