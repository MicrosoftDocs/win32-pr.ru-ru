---
title: Метки
description: Метки
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK, маркеры
- Расширенный формат систем (ASF), маркеры
- ASF (Расширенный системный формат), маркеры
- маркеры, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889128"
---
# <a name="markers"></a><span data-ttu-id="d708e-107">Метки</span><span class="sxs-lookup"><span data-stu-id="d708e-107">Markers</span></span>

<span data-ttu-id="d708e-108">Маркеры — это именованные места на временной шкале файла ASF.</span><span class="sxs-lookup"><span data-stu-id="d708e-108">Markers are named places on the timeline of an ASF file.</span></span> <span data-ttu-id="d708e-109">Каждому маркеру присваивается имя и время презентации.</span><span class="sxs-lookup"><span data-stu-id="d708e-109">Each marker has a name and a presentation time that you assign.</span></span> <span data-ttu-id="d708e-110">Можно указать столько маркеров, сколько требуется для файла.</span><span class="sxs-lookup"><span data-stu-id="d708e-110">You can specify as many markers as you need for a file.</span></span>

<span data-ttu-id="d708e-111">Маркеры полезны для разбиения больших файлов ASF на логические части.</span><span class="sxs-lookup"><span data-stu-id="d708e-111">Markers are useful for breaking up large ASF files in to logical pieces.</span></span> <span data-ttu-id="d708e-112">Приложение, использующее объект Reader для воспроизведения файлов ASF, может предоставить пользователю возможность перехода от маркера к маркеру, что упрощает навигацию по цифровым носителям.</span><span class="sxs-lookup"><span data-stu-id="d708e-112">An application that uses the reader object to play ASF files can provide the user with the option to skip from marker to marker, simplifying navigation of digital media.</span></span> <span data-ttu-id="d708e-113">Например, если вы выводите файл ASF из презентации, вы можете разместить маркеры на временной шкале для каждой из основных обсуждаемых разделов.</span><span class="sxs-lookup"><span data-stu-id="d708e-113">For example, if you are making an ASF file out of a presentation, you can put markers in the timeline for each major topic that is discussed.</span></span> <span data-ttu-id="d708e-114">При воспроизведении, вместо того чтобы получать одну длинную временную шкалу и выгадать место для поиска, пользователь может просто выбрать раздел из списка и перейти непосредственно к соответствующей части файла.</span><span class="sxs-lookup"><span data-stu-id="d708e-114">On playback, instead of getting one long timeline and having to guess at the location to seek to, a user can simply pick a topic from a list and go right to the pertinent portion of the file.</span></span>

<span data-ttu-id="d708e-115">Маркеры управляются объектом редактора метаданных.</span><span class="sxs-lookup"><span data-stu-id="d708e-115">Markers are manipulated by the metadata editor object.</span></span> <span data-ttu-id="d708e-116">Можно добавлять, удалять и просматривать маркеры в файле в любое время после его написания.</span><span class="sxs-lookup"><span data-stu-id="d708e-116">You can add, remove, and view the markers in a file at any time after the file has been written.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d708e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d708e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d708e-118">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="d708e-118">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="d708e-119">**Поиск маркеров**</span><span class="sxs-lookup"><span data-stu-id="d708e-119">**To Seek to Markers**</span></span>](to-seek-to-markers.md)
</dt> <dt>

[<span data-ttu-id="d708e-120">**Использование маркеров**</span><span class="sxs-lookup"><span data-stu-id="d708e-120">**Using Markers**</span></span>](using-markers.md)
</dt> </dl>

 

 




