---
title: иажентспичинпутпропертиес
description: иажентспичинпутпропертиес
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410572"
---
# <a name="iagentspeechinputproperties"></a><span data-ttu-id="8bceb-103">иажентспичинпутпропертиес</span><span class="sxs-lookup"><span data-stu-id="8bceb-103">IAgentSpeechInputProperties</span></span>

<span data-ttu-id="8bceb-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8bceb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="8bceb-105">Иажентспичинпутпропертиес предоставляет доступ к свойствам речевого ввода, поддерживаемым сервером.</span><span class="sxs-lookup"><span data-stu-id="8bceb-105">IAgentSpeechInputProperties provides access to the speech input properties maintained by the server.</span></span> <span data-ttu-id="8bceb-106">Большинство свойств доступно только для чтения в клиентских приложениях, но пользователь может изменить их на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8bceb-106">Most of the properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="8bceb-107">Сервер Microsoft Agent возвращает значения только в том случае, если установлен и включен совместимый обработчик речи.</span><span class="sxs-lookup"><span data-stu-id="8bceb-107">The Microsoft Agent server returns values only if a compatible speech engine has been installed and is enabled.</span></span> <span data-ttu-id="8bceb-108">Запрос этих свойств пытается запустить модуль распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="8bceb-108">Querying these properties attempts to start the speech engine.</span></span>

<span data-ttu-id="8bceb-109">**Методы в порядке таблицы Vtable**</span><span class="sxs-lookup"><span data-stu-id="8bceb-109">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="8bceb-110">Методы Иажентспичинпутпропертиес</span><span class="sxs-lookup"><span data-stu-id="8bceb-110">IAgentSpeechInputProperties Methods</span></span>                                     | <span data-ttu-id="8bceb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8bceb-111">Description</span></span>                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="8bceb-112">**GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="8bceb-112">**GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)           | <span data-ttu-id="8bceb-113">Возвращает значение, указывающее, включен ли модуль распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="8bceb-113">Returns whether the speech recognition engine is enabled.</span></span> |
| [<span data-ttu-id="8bceb-114">**Сочетание клавиш**</span><span class="sxs-lookup"><span data-stu-id="8bceb-114">**GetHotKey**</span></span>](iagentspeechinputproperties--gethotkey.md)             | <span data-ttu-id="8bceb-115">Возвращает текущее назначение ключа прослушивания.</span><span class="sxs-lookup"><span data-stu-id="8bceb-115">Returns the current key assignment of the Listening key.</span></span>  |
| [<span data-ttu-id="8bceb-116">**жетлистенингтип**</span><span class="sxs-lookup"><span data-stu-id="8bceb-116">**GetListeningTip**</span></span>](iagentspeechinputproperties--getlisteningtip.md) | <span data-ttu-id="8bceb-117">Возвращает значение, указывающее, включен ли tip Listen.</span><span class="sxs-lookup"><span data-stu-id="8bceb-117">Returns whether the Listening Tip is enabled.</span></span>             |



 

<span data-ttu-id="8bceb-118">Для обеспечения обратной [](https://www.bing.com/search?q=**GetLCID**)совместимости по- [](https://www.bing.com/search?q=**GetEngine**)прежнему поддерживаются методы [](https://www.bing.com/search?q=**SetEngine**) [**, реализованные в предыдущих**](https://www.bing.com/search?q=**GetInstalled**)версиях Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8bceb-118">[**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**), and [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) methods (supported in earlier versions of Microsoft Agent) are still supported for backward compatibility.</span></span> <span data-ttu-id="8bceb-119">Однако методы не создана и не возвращают полезные значения.</span><span class="sxs-lookup"><span data-stu-id="8bceb-119">However, the methods are not stubbed and do not return useful values.</span></span> <span data-ttu-id="8bceb-120">Используйте [**жетсрмодеид**](https://www.bing.com/search?q=**GetSRModeID**) и [**сетсрмодеид**](https://www.bing.com/search?q=**SetSRModeID**) для запроса и настройки обработчика распознавания речи для использования с символом.</span><span class="sxs-lookup"><span data-stu-id="8bceb-120">Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) and [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) to query and set the speech recognition engine to be used with the character.</span></span> <span data-ttu-id="8bceb-121">Помните, что подсистема должна соответствовать текущему языковому параметру символа.</span><span class="sxs-lookup"><span data-stu-id="8bceb-121">Keep in mind that the engine must match the character's current language setting.</span></span>

 

 




