---
title: Путеводитель по метафайлу Windows Media
description: Путеводитель по метафайлу Windows Media
ms.assetid: d2360a63-f073-44b0-8637-1f22b577f51a
keywords:
- Метафайлы Windows Media, сведения
- Проигрыватель Windows Media, метафайлы
- Проигрыватель Windows Media, метафайлы Windows Media
- Метафайлы, сведения
- Windows Media, метафайлы
- Списки воспроизведения метафайлов Windows Media, сведения
- списки воспроизведения, сведения
- списки воспроизведения метафайлов, сведения
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcf0a4c98ae49d1cdf3b7e36e8a278f184cd4632
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986786"
---
# <a name="windows-media-metafile-guide"></a><span data-ttu-id="8c803-111">Путеводитель по метафайлу Windows Media</span><span class="sxs-lookup"><span data-stu-id="8c803-111">Windows Media Metafile Guide</span></span>

<span data-ttu-id="8c803-112">Метафайл Windows Media может быть простым или сложным по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="8c803-112">A Windows Media metafile can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="8c803-113">Самый простой метафайл Windows Media содержит только универсальный указатель ресурсов (URL-адрес) некоторого мультимедийного содержимого на сервере.</span><span class="sxs-lookup"><span data-stu-id="8c803-113">The most basic Windows Media metafile contains only the Uniform Resource Locator (URL) of some multimedia content on a server.</span></span> <span data-ttu-id="8c803-114">Клиент, проигрыватель Windows Media, анализирует эти сведения, а затем открывает файл мультимедиа или поток, определенный в метафайле Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8c803-114">The client, Windows Media Player, parses this information and then opens the media file or stream defined in the Windows Media metafile.</span></span> <span data-ttu-id="8c803-115">Сложный метафайл может содержать несколько файлов или потоков, расположенных в списке воспроизведения, инструкции по воспроизведению файлов или потоков, текстовых и графических элементов, таких как заголовок, автор и текст авторских прав, персонализированная вставка рекламы в поток Live, гиперссылки, связанные с элементами интерфейса проигрывателя Windows Media, и многое другое.</span><span class="sxs-lookup"><span data-stu-id="8c803-115">A complex metafile can contain multiple files or streams arranged in a playlist, instructions on how to play the files or streams, text and graphic elements such as title, author, and copyright text, personalized ad insertion into a live stream, hyperlinks associated with elements on the Windows Media Player interface, and more.</span></span>

<span data-ttu-id="8c803-116">В следующих разделах содержатся подробные сведения о создании и использовании списков воспроизведения метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8c803-116">The following sections provide detailed information on how to create and use Windows Media metafile playlists.</span></span>



| <span data-ttu-id="8c803-117">Section</span><span class="sxs-lookup"><span data-stu-id="8c803-117">Section</span></span>                                                            | <span data-ttu-id="8c803-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8c803-118">Description</span></span>                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c803-119">Типы списков воспроизведения</span><span class="sxs-lookup"><span data-stu-id="8c803-119">Types of Playlists</span></span>](types-of-playlists.md)                       | <span data-ttu-id="8c803-120">Выводит список доступных расширений имен файлов.</span><span class="sxs-lookup"><span data-stu-id="8c803-120">Lists available file name extensions.</span></span>                                               |
| [<span data-ttu-id="8c803-121">Создание списков воспроизведения метафайлов</span><span class="sxs-lookup"><span data-stu-id="8c803-121">Creating Metafile Playlists</span></span>](creating-metafile-playlists.md)     | <span data-ttu-id="8c803-122">Описание создания списков воспроизведения метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8c803-122">Describes how to create Windows Media metafile playlists.</span></span>                           |
| [<span data-ttu-id="8c803-123">Списки воспроизведения метафайлов</span><span class="sxs-lookup"><span data-stu-id="8c803-123">Metafile Playlists</span></span>](metafile-playlists.md)                       | <span data-ttu-id="8c803-124">Описывает использование списка воспроизведения метафайлов, создание скриптов, метаданные и обработку.</span><span class="sxs-lookup"><span data-stu-id="8c803-124">Describes metafile playlist usage, scripting, metadata, and processing.</span></span>             |
| [<span data-ttu-id="8c803-125">Рекомендации по расширению метафайлов</span><span class="sxs-lookup"><span data-stu-id="8c803-125">Metafile Extension Guidelines</span></span>](metafile-extension-guidelines.md) | <span data-ttu-id="8c803-126">Описывает предпочтительное использование расширений имен файлов для потоковой передачи файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8c803-126">Describes the preferred use of file name extensions for streaming media files.</span></span>      |
| [<span data-ttu-id="8c803-127">Порядок приоритета</span><span class="sxs-lookup"><span data-stu-id="8c803-127">Order of Precedence</span></span>](order-of-precedence.md)                     | <span data-ttu-id="8c803-128">Описывает, как элементы списка воспроизведения метафайлов переопределяют другие элементы списка воспроизведения метафайлов.</span><span class="sxs-lookup"><span data-stu-id="8c803-128">Describes how metafile playlist elements override other metafile playlist elements.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8c803-129">См. также</span><span class="sxs-lookup"><span data-stu-id="8c803-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c803-130">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8c803-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8c803-131">**Метафайлы Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8c803-131">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




