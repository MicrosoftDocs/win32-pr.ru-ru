---
title: Окно "Дополнительные параметры символов" (окно "Voice Commands")
description: Сведения о диалоговом окне "Дополнительные параметры символов", которое предоставляет пользователям возможность изменять их взаимодействие со всеми символами.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404366"
---
# <a name="advanced-character-options-window-voice-commands-window"></a><span data-ttu-id="7fbd2-103">Окно "Дополнительные параметры символов" (окно "Voice Commands")</span><span class="sxs-lookup"><span data-stu-id="7fbd2-103">Advanced Character Options Window (Voice Commands Window)</span></span>

<span data-ttu-id="7fbd2-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7fbd2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7fbd2-105">В окне Дополнительные параметры символов можно настроить параметры взаимодействия пользователей со всеми символами.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-105">The Advanced Character Options window provides options for users to adjust their interaction with all characters.</span></span> <span data-ttu-id="7fbd2-106">Например, пользователи могут отключить речевой ввод или изменить входные параметры.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-106">For example, users can disable speech input or change input parameters.</span></span> <span data-ttu-id="7fbd2-107">Пользователи также могут изменять параметры вывода для всплывающего окна Word.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-107">Users can also change the output settings for the word balloon.</span></span> <span data-ttu-id="7fbd2-108">Эти параметры переопределяют любой набор, заданный клиентским приложением или заданный в качестве части определения символа.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-108">These settings override any set by a client application or set as part of the character definition.</span></span> <span data-ttu-id="7fbd2-109">Приложение не может изменить или отключить эти параметры, так как они применяются к общим предпочтениям пользователя для работы со всеми символами.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-109">Your application cannot change or disable these options, because they apply to the general user preferences for operation of all characters.</span></span> <span data-ttu-id="7fbd2-110">Однако сервер будет уведомлять ваше приложение ([**дефаултчарактерчанже**](defaultcharacterchange-event.md)), когда пользователь изменит и применит параметр.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-110">However, the server will notify your application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) when the user changes and applies an option.</span></span> <span data-ttu-id="7fbd2-111">Можно также отобразить или закрыть окно с помощью свойства [**Visible**](visible-property.md) окна и получить доступ к его расположению через его свойства [**Top**](top-property.md) и [**Left**](left-property.md) .</span><span class="sxs-lookup"><span data-stu-id="7fbd2-111">You can also display or close the window using the window's [**Visible**](visible-property.md) property and access its location through its [**Top**](top-property.md) and [**Left**](left-property.md) properties.</span></span>

<span data-ttu-id="7fbd2-112">Помимо поддержки анимации символа, Microsoft Agent поддерживает звуковые выходные данные для символа.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-112">In addition to supporting the animation of a character, Microsoft Agent supports audio output for the character.</span></span> <span data-ttu-id="7fbd2-113">Сюда входят выходные и звуковые эффекты.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-113">This includes spoken output and sound effects.</span></span> <span data-ttu-id="7fbd2-114">Для выходного выхода сервер автоматически выполняет синхронизацию определенных для символа изображений рот с выходными данными.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-114">For spoken output, the server automatically lip-syncs the character's defined mouth images to the output.</span></span> <span data-ttu-id="7fbd2-115">Можно выбрать синтез текста в речь, записанные аудио-файлы или только текст всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="7fbd2-115">You can choose text-to-speech (TTS) synthesis, recorded audio, or only word balloon text output.</span></span>

 

 




