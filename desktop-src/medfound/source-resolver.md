---
description: Сопоставитель источников
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Сопоставитель источников
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344382"
---
# <a name="source-resolver"></a><span data-ttu-id="d810b-103">Сопоставитель источников</span><span class="sxs-lookup"><span data-stu-id="d810b-103">Source Resolver</span></span>

<span data-ttu-id="d810b-104">Средство выбора источника принимает URL-адрес или поток байтов и создает соответствующий источник мультимедиа для этого контента.</span><span class="sxs-lookup"><span data-stu-id="d810b-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="d810b-105">Средство выбора источника является стандартным способом для создания источников мультимедиа в приложениях.</span><span class="sxs-lookup"><span data-stu-id="d810b-105">The source resolver is the standard way for the applications to create media sources.</span></span>

<span data-ttu-id="d810b-106">На внутреннем основе сопоставитель источников использует объекты *обработчика* :</span><span class="sxs-lookup"><span data-stu-id="d810b-106">Internally, the source resolver uses *handler* objects:</span></span>

-   <span data-ttu-id="d810b-107">*Обработчики схем* принимают URL-адрес и создают источник мультимедиа или байтовый поток.</span><span class="sxs-lookup"><span data-stu-id="d810b-107">*Scheme handlers* take a URL and create a media source or a byte stream.</span></span>
-   <span data-ttu-id="d810b-108">*Обработчики байтового потока* принимают байтовый поток и создают источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d810b-108">*Byte stream handlers* take a byte stream and create a media source.</span></span>

<span data-ttu-id="d810b-109">Можно реализовать пользовательский обработчик и добавить его в реестр.</span><span class="sxs-lookup"><span data-stu-id="d810b-109">You can implement a custom handler and add it to the registry.</span></span> <span data-ttu-id="d810b-110">Обработчики схем регистрируются с помощью схемы URL-адресов, а обработчики байтового потока регистрируются по расширению имени файла или типу MIME.</span><span class="sxs-lookup"><span data-stu-id="d810b-110">Scheme handlers are registered by URL scheme, and byte stream handlers are registered by file name extension or MIME type.</span></span>

<span data-ttu-id="d810b-111">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="d810b-111">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d810b-112">Использование сопоставителя источников</span><span class="sxs-lookup"><span data-stu-id="d810b-112">Using the Source Resolver</span></span>](using-the-source-resolver.md)
-   [<span data-ttu-id="d810b-113">Настройка источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d810b-113">Configuring a Media Source</span></span>](configuring-a-media-source.md)
-   [<span data-ttu-id="d810b-114">Обработчики схем и обработчики Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="d810b-114">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="d810b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d810b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d810b-116">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d810b-116">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



