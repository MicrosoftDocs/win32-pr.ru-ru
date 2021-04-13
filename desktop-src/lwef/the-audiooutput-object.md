---
title: Объект Аудиуутпут
description: Объект Аудиуутпут
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412958"
---
# <a name="the-audiooutput-object"></a><span data-ttu-id="59931-103">Объект Аудиуутпут</span><span class="sxs-lookup"><span data-stu-id="59931-103">The AudioOutput Object</span></span>

<span data-ttu-id="59931-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="59931-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="59931-105">Этот объект предоставляет доступ к свойствам выходного звука, поддерживаемым сервером.</span><span class="sxs-lookup"><span data-stu-id="59931-105">This object provides access to audio output properties maintained by the server.</span></span> <span data-ttu-id="59931-106">Свойства доступны только для чтения, но пользователь может изменить их на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="59931-106">The properties are read-only, but the user can change them in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="59931-107">При объявлении объектной переменной типа [**иажентктлаудиубжектекс**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**)доступ ко всем свойствам объекта [**аудиуутпут**](/windows/desktop/lwef/the-audiooutput-object) будет невозможен.</span><span class="sxs-lookup"><span data-stu-id="59931-107">If you declare an object variable of type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), you will not be able to access all properties for the [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) object.</span></span> <span data-ttu-id="59931-108">Хотя агент также поддерживает [**иажентктлаудиубжект**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), этот последний интерфейс предоставляется только для обратной совместимости и поддерживает только эти свойства в предыдущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="59931-108">While Agent also supports [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), this latter interface is provided only for backward compatibility and supports only those properties in previous releases.</span></span>

-   [<span data-ttu-id="59931-109">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="59931-109">**Enabled**</span></span>](enabled-property-ao.md)
-   [<span data-ttu-id="59931-110">**саундеффектс**</span><span class="sxs-lookup"><span data-stu-id="59931-110">**SoundEffects**</span></span>](soundeffects-property.md)
-   [<span data-ttu-id="59931-111">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="59931-111">**Status**</span></span>](status-property.md)

 

 