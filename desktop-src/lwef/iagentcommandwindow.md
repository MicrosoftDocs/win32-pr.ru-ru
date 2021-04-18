---
title: иаженткоммандвиндов
description: иаженткоммандвиндов
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700615"
---
# <a name="iagentcommandwindow"></a><span data-ttu-id="d96bd-103">иаженткоммандвиндов</span><span class="sxs-lookup"><span data-stu-id="d96bd-103">IAgentCommandWindow</span></span>

<span data-ttu-id="d96bd-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d96bd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d96bd-105">**Иаженткоммандвиндов** определяет интерфейс, позволяющий приложениям устанавливать и запрашивать свойства окна "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="d96bd-105">**IAgentCommandWindow** defines an interface that allows applications to set and query the properties of the Voice Commands Window.</span></span> <span data-ttu-id="d96bd-106">Окно "Voice Commands" — это общий ресурс, который в основном предназначен для предоставления пользователям возможности просмотра команд с поддержкой голоса.</span><span class="sxs-lookup"><span data-stu-id="d96bd-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="d96bd-107">Если распознавание речи отключено, окно голосовых команд по-прежнему отображается с текстом «речевые входы отключены» (на языке символа).</span><span class="sxs-lookup"><span data-stu-id="d96bd-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="d96bd-108">Если не установлен модуль распознавания речи, соответствующий языковому параметру символа, отображается окно "речевой ввод недоступен".</span><span class="sxs-lookup"><span data-stu-id="d96bd-108">If no speech engine is installed that matches the character's language setting, the window displays, "Speech input not available."</span></span> <span data-ttu-id="d96bd-109">Если клиент ввода-активного не определил параметры голоса для команд и отключил глобальные Voice-команды, в окне отображается «без голосовых команд».</span><span class="sxs-lookup"><span data-stu-id="d96bd-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="d96bd-110">Кроме того, можно запрашивать свойства окна голосовых команд независимо от того, отключен ли речевой ввод или установлен совместимый речевой механизм.</span><span class="sxs-lookup"><span data-stu-id="d96bd-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

<span data-ttu-id="d96bd-111">**Методы в порядке таблицы Vtable**</span><span class="sxs-lookup"><span data-stu-id="d96bd-111">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="d96bd-112">Методы Иаженткоммандвиндов</span><span class="sxs-lookup"><span data-stu-id="d96bd-112">IAgentCommandWindow Methods</span></span>                             | <span data-ttu-id="d96bd-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d96bd-113">Description</span></span>                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d96bd-114">**сетвисибле**</span><span class="sxs-lookup"><span data-stu-id="d96bd-114">**SetVisible**</span></span>](iagentcommandwindow--setvisible.md)   | <span data-ttu-id="d96bd-115">Задает значение свойства [**Visible**](visible-property.md) окна "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="d96bd-115">Sets the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span>    |
| [<span data-ttu-id="d96bd-116">**Во всех видимых**</span><span class="sxs-lookup"><span data-stu-id="d96bd-116">**GetVisible**</span></span>](iagentcommandwindow--getvisible.md)   | <span data-ttu-id="d96bd-117">Возвращает значение свойства [**Visible**](visible-property.md) окна "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="d96bd-117">Returns the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span> |
| [<span data-ttu-id="d96bd-118">**Методом Disposition**</span><span class="sxs-lookup"><span data-stu-id="d96bd-118">**GetPosition**</span></span>](iagentcommandwindow--getposition.md) | <span data-ttu-id="d96bd-119">Возвращает расположение окна "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="d96bd-119">Returns the position of the Voice Commands Window.</span></span>                                                  |
| [<span data-ttu-id="d96bd-120">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="d96bd-120">**GetSize**</span></span>](iagentcommandwindow--getsize.md)         | <span data-ttu-id="d96bd-121">Возвращает размер окна "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="d96bd-121">Returns the size of the Voice Commands Window.</span></span>                                                      |



 

 

 




