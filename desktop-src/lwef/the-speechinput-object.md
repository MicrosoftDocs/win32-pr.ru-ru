---
title: Объект Спичинпут
description: Объект Спичинпут
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986630"
---
# <a name="the-speechinput-object"></a><span data-ttu-id="12475-103">Объект Спичинпут</span><span class="sxs-lookup"><span data-stu-id="12475-103">The SpeechInput Object</span></span>

<span data-ttu-id="12475-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12475-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="12475-105">Объект [**спичинпут**](https://www.bing.com/search?q=**SpeechInput**) предоставляет доступ к свойствам речевого ввода, поддерживаемым сервером агента.</span><span class="sxs-lookup"><span data-stu-id="12475-105">The [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) object provides access to the speech input properties maintained by the Agent server.</span></span> <span data-ttu-id="12475-106">Свойства доступны только для чтения в клиентских приложениях, но пользователь может изменить их на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="12475-106">The properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="12475-107">Сервер возвращает значения только в том случае, если установлен и включен совместимый обработчик речи.</span><span class="sxs-lookup"><span data-stu-id="12475-107">The server returns values only if a compatible speech engine has been installed and is enabled.</span></span>

<span data-ttu-id="12475-108">Свойства [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**)и [**Language**](https://www.bing.com/search?q=**Language**) больше не поддерживаются, но (для обратной совместимости) возвращает значения NULL при запросе.</span><span class="sxs-lookup"><span data-stu-id="12475-108">The [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**), and [**Language**](https://www.bing.com/search?q=**Language**) properties are no longer supported, but (for backward compatibility) return null values if queried.</span></span> <span data-ttu-id="12475-109">Чтобы запросить или задать режим распознавания речи, используйте свойство [**срмодеид**](srmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="12475-109">To query or set a speech recognition's mode, use the [**SRModeID**](srmodeid-property.md) property.</span></span>

-   [<span data-ttu-id="12475-110">Свойства Спичинпут</span><span class="sxs-lookup"><span data-stu-id="12475-110">SpeechInput Properties</span></span>](speechinput-properties.md)

 

 




