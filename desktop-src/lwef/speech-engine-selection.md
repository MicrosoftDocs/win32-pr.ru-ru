---
title: Выбор обработчика речи
description: Выбор обработчика речи
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888215"
---
# <a name="speech-engine-selection"></a><span data-ttu-id="46f5f-103">Выбор обработчика речи</span><span class="sxs-lookup"><span data-stu-id="46f5f-103">Speech Engine Selection</span></span>

<span data-ttu-id="46f5f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46f5f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="46f5f-105">Параметр идентификатора языка символа определяет используемый по умолчанию язык речевого ввода. Microsoft Agent запрашивает SAPI для установленного ядра, соответствующего этому языку.</span><span class="sxs-lookup"><span data-stu-id="46f5f-105">A character's language ID setting determines its default speech input language; Microsoft Agent requests SAPI for an installed engine that matches that language.</span></span> <span data-ttu-id="46f5f-106">Если клиентское приложение не указывает предпочтение языка, то Microsoft Agent попытается найти подсистему распознавания речи, соответствующую пользовательскому ИДЕНТИФИКАТОРу языка по умолчанию (с использованием основного идентификатора языка, а затем вспомогательного идентификатора языка).</span><span class="sxs-lookup"><span data-stu-id="46f5f-106">If a client application does not specify a language preference, Microsoft Agent will attempt to find a speech recognition engine that matches the user default language ID (using the major language ID, then the minor language ID).</span></span> <span data-ttu-id="46f5f-107">Если подсистема, соответствующая этому языку, недоступна, распознавание речи для этого символа отключено.</span><span class="sxs-lookup"><span data-stu-id="46f5f-107">If no engine is available matching this language, speech is disabled for that character.</span></span>

<span data-ttu-id="46f5f-108">Можно также запросить конкретный модуль распознавания речи, указав идентификатор своего режима (с помощью свойства character [**срмодеид**](srmodeid-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="46f5f-108">You can also request a specific speech recognition engine by specifying its mode ID (using the character [**SRModeID**](srmodeid-property.md) property).</span></span> <span data-ttu-id="46f5f-109">Однако если идентификатор языка для этого идентификатора режима не совпадает с языковым параметром клиента, вызов завершится неудачей (вызовет ошибку в элементе управления).</span><span class="sxs-lookup"><span data-stu-id="46f5f-109">However, if the language ID for that mode ID does not match the client's language setting, the call will fail (raise an error in the control).</span></span> <span data-ttu-id="46f5f-110">Модуль распознавания речи будет оставаться последним успешно установленным ядром клиента или, если нет, подсистемой, которая соответствует ИДЕНТИФИКАТОРу текущего языка системы.</span><span class="sxs-lookup"><span data-stu-id="46f5f-110">The speech recognition engine will then remain the last successfully set engine by the client, or if none, the engine that matches the current system language ID.</span></span> <span data-ttu-id="46f5f-111">Если сопоставление по-прежнему отсутствует, речевой ввод для этого клиента недоступен.</span><span class="sxs-lookup"><span data-stu-id="46f5f-111">If there is still no match, speech input is not available for that client.</span></span>

<span data-ttu-id="46f5f-112">Microsoft Agent автоматически загружает модуль распознавания речи, когда пользователь нажимает клавишу «Listen» или «input-Active» вызывает метод [**Listen**](listen-method.md) .</span><span class="sxs-lookup"><span data-stu-id="46f5f-112">Microsoft Agent automatically loads a speech recognition engine when speech input is initiated by a user pressing the Listening hotkey or the input-active client calls the [**Listen**](listen-method.md) method.</span></span> <span data-ttu-id="46f5f-113">Однако подсистема также может быть загружена при установке или запросе идентификатора режима, при установке или запросе свойств окна голосовых команд, при запросе [**срстатус**](srstatus-property.md)или при включенной функции распознавания речи, а также при отображении речевого ввода на странице «Дополнительные параметры символов».</span><span class="sxs-lookup"><span data-stu-id="46f5f-113">However, an engine may also be loaded when setting or querying its mode ID, setting or querying the properties of the Voice Commands Window, querying [**SRStatus**](srstatus-property.md), or when speech is enabled and the user displays the Speech Input page of the Advanced Character Options.</span></span> <span data-ttu-id="46f5f-114">Тем не менее, агент Microsoft Agent хранит только загруженные обработчики речи, которые используются клиентами.</span><span class="sxs-lookup"><span data-stu-id="46f5f-114">However, Microsoft Agent only keeps loaded the speech engines that clients are using.</span></span>

 

 




