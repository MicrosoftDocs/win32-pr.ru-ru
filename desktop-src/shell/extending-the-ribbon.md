---
description: Узнайте, как расширить ленту проводника Windows.
title: Расширение ленты
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540455"
---
# <a name="extending-the-ribbon"></a><span data-ttu-id="caaa9-103">Расширение ленты</span><span class="sxs-lookup"><span data-stu-id="caaa9-103">Extending the Ribbon</span></span>

<span data-ttu-id="caaa9-104">В проводнике Windows лента помогает сделать распространенные действия по управлению файлами конечными пользователями простыми и более обнаруживаемыми, но изменения занимающимся для разработчиков приложений.</span><span class="sxs-lookup"><span data-stu-id="caaa9-104">In Windows Explorer, the Ribbon helps make common end-user file management activities easier and more discoverable, but there are changes afoot for app developers.</span></span> <span data-ttu-id="caaa9-105">Например, Старая панель команд была свободно расширяемой, но в настоящее время лента в ней больше ограничена.</span><span class="sxs-lookup"><span data-stu-id="caaa9-105">For example, the old command bar was freely extensible but the Ribbon is more restricted at this time.</span></span> <span data-ttu-id="caaa9-106">Кроме того, лента не отображается по умолчанию для всех расширений пространства имен, поэтому необходимо принять участие в получении ленты. в противном случае вы получаете более раннюю панель команд.</span><span class="sxs-lookup"><span data-stu-id="caaa9-106">Also, the Ribbon is not shown by default for all namespace extensions, so you have to opt in to get the Ribbon; otherwise, you get the older command bar.</span></span>

<span data-ttu-id="caaa9-107">Действия, доступные пользователям на ленте, делятся на три категории расширяемости:</span><span class="sxs-lookup"><span data-stu-id="caaa9-107">Actions available to users on the Ribbon fall into three extensibility categories:</span></span>

-   <span data-ttu-id="caaa9-108">Расширяемость не требуется.</span><span class="sxs-lookup"><span data-stu-id="caaa9-108">Extensibility is not needed.</span></span> <span data-ttu-id="caaa9-109">Примеры: копирование, вставка, удаление.</span><span class="sxs-lookup"><span data-stu-id="caaa9-109">Examples: Copy, Paste, Delete.</span></span> <span data-ttu-id="caaa9-110">Windows обрабатывает эти команды.</span><span class="sxs-lookup"><span data-stu-id="caaa9-110">Windows handles these verbs for you.</span></span>
-   <span data-ttu-id="caaa9-111">В настоящее время расширяемость не разрешена: примеры: ZIP, закрыть сеанс и другие настраиваемые действия.</span><span class="sxs-lookup"><span data-stu-id="caaa9-111">Extensibility is not currently allowed: Examples: Zip, Close Session, and other custom actions.</span></span> <span data-ttu-id="caaa9-112">Используйте контекстное меню, чтобы охватить эти сценарии.</span><span class="sxs-lookup"><span data-stu-id="caaa9-112">Use the context menu to cover these scenarios.</span></span>
-   <span data-ttu-id="caaa9-113">Расширяемость встроена в само действие.</span><span class="sxs-lookup"><span data-stu-id="caaa9-113">Extensibility is built into the action itself.</span></span> <span data-ttu-id="caaa9-114">Примеры: Поиск, электронная почта, печать, новый элемент.</span><span class="sxs-lookup"><span data-stu-id="caaa9-114">Examples: Search, Email, Print, New Item.</span></span> <span data-ttu-id="caaa9-115">Чтобы включить приложение или формат файла на ленту, необходимо зарегистрироваться для получения этих команд.</span><span class="sxs-lookup"><span data-stu-id="caaa9-115">You need to register for these verbs to include your app or file format in the Ribbon .</span></span>

<span data-ttu-id="caaa9-116">В этом документе описывается, как можно принять участие в ленте и как зарегистрироваться для работы с конкретными командами ленты.</span><span class="sxs-lookup"><span data-stu-id="caaa9-116">This document describes how you can opt-in to get the Ribbon, and how to register to handle specific Ribbon verbs.</span></span>

## <a name="opting-in-to-the-ribbon"></a><span data-ttu-id="caaa9-117">Включение на ленту</span><span class="sxs-lookup"><span data-stu-id="caaa9-117">Opting in to the Ribbon</span></span>

<span data-ttu-id="caaa9-118">Чтобы принять участие в ленте, ваша реализация [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) должна указать **\_ ленту EP** в [**иексплорерпаневисибилити:: жетпанестате**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) и вернуть **EPS \_ Force** \| **EPS \_ по умолчанию \_ в**.</span><span class="sxs-lookup"><span data-stu-id="caaa9-118">To opt in to the Ribbon, your [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) implementation should specify **EP\_Ribbon** in [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) and return **EPS\_FORCE** \| **EPS\_DEFAULT\_ON**.</span></span>

## <a name="extending-the-ribbon-for-file-extensions"></a><span data-ttu-id="caaa9-119">Расширение ленты для расширений файлов</span><span class="sxs-lookup"><span data-stu-id="caaa9-119">Extending the Ribbon for File Extensions</span></span>

<span data-ttu-id="caaa9-120">Эти кнопки на ленте расширяются на основе расширений файлов:</span><span class="sxs-lookup"><span data-stu-id="caaa9-120">These Ribbon buttons are extensible based on file extensions:</span></span>

-   <span data-ttu-id="caaa9-121">Извлечь все</span><span class="sxs-lookup"><span data-stu-id="caaa9-121">Extract All</span></span>
-   <span data-ttu-id="caaa9-122">Подключить \| запись (ISO-образ)</span><span class="sxs-lookup"><span data-stu-id="caaa9-122">Mount \| Burn (an ISO)</span></span>
-   <span data-ttu-id="caaa9-123">Воспроизвести \| все \| Добавление в список воспроизведения (команда: поставить в очередь)</span><span class="sxs-lookup"><span data-stu-id="caaa9-123">Play \| Play All \| Add to Playlist (verb: Enqueue)</span></span>
-   <span data-ttu-id="caaa9-124">Открыть</span><span class="sxs-lookup"><span data-stu-id="caaa9-124">Open</span></span>
-   <span data-ttu-id="caaa9-125">Изменить</span><span class="sxs-lookup"><span data-stu-id="caaa9-125">Edit</span></span>
-   <span data-ttu-id="caaa9-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="caaa9-126">Properties</span></span>

<span data-ttu-id="caaa9-127">При регистрации для статической обработки соответствующих команд для новых типов файлов лента обрабатывает команды соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="caaa9-127">When you register to statically handle the relevant verbs for new file types, the Ribbon handles the verbs appropriately.</span></span> <span data-ttu-id="caaa9-128">Вы регистрируетесь точно так же, как для команд контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="caaa9-128">You register just as you would for context menu verbs.</span></span> <span data-ttu-id="caaa9-129">Дополнительные сведения о сопоставлении файлов и регистрации для команд см. в разделе [глаголы и сопоставления файлов](fa-verbs.md) и [Создание обработчиков контекстного меню](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="caaa9-129">For more information about file associations and registering for verbs, see [Verbs and File Associations](fa-verbs.md) and [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="registering-as-a-default-handler-for-actionids"></a><span data-ttu-id="caaa9-130">Регистрация в качестве обработчика по умолчанию для Актионидс</span><span class="sxs-lookup"><span data-stu-id="caaa9-130">Registering as a Default Handler for ActionIds</span></span>

<span data-ttu-id="caaa9-131">Сначала Зарегистрируйте идентификатор ProgId в соответствующем подразделе Ассокактионид.</span><span class="sxs-lookup"><span data-stu-id="caaa9-131">First, register your ProgId under the appropriate AssocActionId subkey.</span></span> <span data-ttu-id="caaa9-132">Каждый подраздел Ассокактионид представляет команду или действие, которые пользователи могут вызывать из ленты.</span><span class="sxs-lookup"><span data-stu-id="caaa9-132">Each AssocActionId subkey represents a verb or action that users can invoke from the Ribbon.</span></span> <span data-ttu-id="caaa9-133">В этом примере приложение регистрируется для Зипселектион ActionID, чтобы расширить кнопку "извлечь все" на ленте.</span><span class="sxs-lookup"><span data-stu-id="caaa9-133">In this example, the app registers for the ZipSelection ActionID to extend the "Extract All" button on the Ribbon.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

<span data-ttu-id="caaa9-134">После завершения регистрации необходимо зарегистрироваться для работы с протоколами так же, как обычно, как описано в разделе [программы по умолчанию](default-programs.md).</span><span class="sxs-lookup"><span data-stu-id="caaa9-134">Once that registration is complete, you must then register to handle protocols just as you normally would, as described in [Default Programs](default-programs.md).</span></span>

 

 



