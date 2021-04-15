---
description: В TAPI 3,1 объект терминала расширен и включает файловый терминал. Файловые терминалы предоставляют простые средства для выполнения стандартных операций, например записи аудиопотока или потоков в файл или последующее воспроизведение записанного звука в поток.
ms.assetid: 397b9b69-edd2-482e-b078-0cc61b489a37
title: Терминалы файловых терминалов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc237565a806e8a0ef4ad9bbbce1c938daadb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682688"
---
# <a name="file-terminals"></a><span data-ttu-id="47122-104">Терминалы файловых терминалов</span><span class="sxs-lookup"><span data-stu-id="47122-104">File Terminals</span></span>

<span data-ttu-id="47122-105">В TAPI 3,1 объект терминала расширен и включает файловый терминал.</span><span class="sxs-lookup"><span data-stu-id="47122-105">In TAPI 3.1, the terminal object is expanded to include a file terminal.</span></span> <span data-ttu-id="47122-106">Файловые терминалы предоставляют простые средства для выполнения стандартных операций, например записи аудиопотока или потоков в файл или последующее воспроизведение записанного звука в поток.</span><span class="sxs-lookup"><span data-stu-id="47122-106">File terminals provide a simple means to perform common operations, for example, recording an audio stream or streams to a file or subsequent playback of recorded audio to a stream.</span></span>

<span data-ttu-id="47122-107">Для работы с файловыми терминалами используются пять базовых объектов:</span><span class="sxs-lookup"><span data-stu-id="47122-107">Five basic objects are used to manipulate file terminals:</span></span>

-   <span data-ttu-id="47122-108">Терминал воспроизведения файлов</span><span class="sxs-lookup"><span data-stu-id="47122-108">File Playback Terminal</span></span>
-   <span data-ttu-id="47122-109">Терминал записи файлов</span><span class="sxs-lookup"><span data-stu-id="47122-109">File Recording Terminal</span></span>
-   <span data-ttu-id="47122-110">Запись о воспроизведении файлов</span><span class="sxs-lookup"><span data-stu-id="47122-110">File Playback Track</span></span>
-   <span data-ttu-id="47122-111">Запись файла</span><span class="sxs-lookup"><span data-stu-id="47122-111">File Recording Track</span></span>
-   <span data-ttu-id="47122-112">Событие файла</span><span class="sxs-lookup"><span data-stu-id="47122-112">File Event</span></span>

<span data-ttu-id="47122-113">Объекты терминала файлов можно рассматривать как абстракцию для хранилища, который обычно является файлом.</span><span class="sxs-lookup"><span data-stu-id="47122-113">The File Terminal objects can be thought of as an abstraction for the storage, which is usually a file.</span></span> <span data-ttu-id="47122-114">Дорожки соответствуют отдельным потокам звуковых данных в этом хранилище, например при записи голоса.</span><span class="sxs-lookup"><span data-stu-id="47122-114">Tracks correspond to the individual audio data streams in that storage, such as when voice is recorded.</span></span>

<span data-ttu-id="47122-115">Дополнительные сведения о файловых терминалах см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="47122-115">For more information about file terminals, see:</span></span>

-   [<span data-ttu-id="47122-116">Терминал воспроизведения файлов и терминал записи файлов</span><span class="sxs-lookup"><span data-stu-id="47122-116">File Playback Terminal and File Recording Terminal</span></span>](file-playback-terminal-and-file-recording-terminal.md)
-   [<span data-ttu-id="47122-117">Мониторинг терминалов</span><span class="sxs-lookup"><span data-stu-id="47122-117">Track Terminals</span></span>](track-terminals.md)

<span data-ttu-id="47122-118">Дополнительные сведения и примеры кода и списки задач, связанные с файловыми терминалами, см. в разделе [Использование файловых терминалов](using-file-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="47122-118">For more information and code samples and task lists related to file terminals, see [Using File Terminals](using-file-terminals.md).</span></span>

 

 



