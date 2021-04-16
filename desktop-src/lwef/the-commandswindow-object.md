---
title: Объект Коммандсвиндов
description: Объект Коммандсвиндов
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710258"
---
# <a name="the-commandswindow-object"></a><span data-ttu-id="b7c27-103">Объект Коммандсвиндов</span><span class="sxs-lookup"><span data-stu-id="b7c27-103">The CommandsWindow Object</span></span>

<span data-ttu-id="b7c27-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b7c27-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b7c27-105">Объект [**коммандсвиндов**](/windows/desktop/lwef/the-commandswindow-object) предоставляет доступ к свойствам окна "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="b7c27-105">The [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) object provides access to properties of the Voice Commands Window.</span></span> <span data-ttu-id="b7c27-106">Окно "Voice Commands" — это общий ресурс, который в основном предназначен для предоставления пользователям возможности просмотра команд с поддержкой голоса.</span><span class="sxs-lookup"><span data-stu-id="b7c27-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="b7c27-107">Если распознавание речи отключено, окно голосовых команд по-прежнему отображается с текстом «речевые входы отключены» (на языке символа).</span><span class="sxs-lookup"><span data-stu-id="b7c27-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="b7c27-108">Если не установлено средство распознавания речи, совпадающее с параметром Language, отображаемым в окне, то "речевой ввод недоступен".</span><span class="sxs-lookup"><span data-stu-id="b7c27-108">If no speech engine is installed that matches the character's language setting the window displays, "Speech input not available."</span></span> <span data-ttu-id="b7c27-109">Если клиент ввода-активного не определил параметры голоса для команд и отключил глобальные Voice-команды, в окне отображается «без голосовых команд».</span><span class="sxs-lookup"><span data-stu-id="b7c27-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="b7c27-110">Кроме того, можно запрашивать свойства окна голосовых команд независимо от того, отключен ли речевой ввод или установлен совместимый речевой механизм.</span><span class="sxs-lookup"><span data-stu-id="b7c27-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

-   [<span data-ttu-id="b7c27-111">Свойства Коммандсвиндов</span><span class="sxs-lookup"><span data-stu-id="b7c27-111">CommandsWindow Properties</span></span>](commandswindow-properties.md)

 

 