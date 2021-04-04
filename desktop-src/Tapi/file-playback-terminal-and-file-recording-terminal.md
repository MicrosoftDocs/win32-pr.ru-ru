---
description: Терминал воспроизведения файлов и терминал записи файлов предоставляют интерфейсы Иттерминал и Итмултитракктерминал. Эти объекты также предоставляют интерфейс Итмедиаконтрол, который предоставляет методы для остановки, запуска и навигации по мультимедиа.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Терминал воспроизведения файлов и терминал записи файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998476"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a><span data-ttu-id="7ad1d-104">Терминал воспроизведения файлов и терминал записи файлов</span><span class="sxs-lookup"><span data-stu-id="7ad1d-104">File Playback Terminal and File Recording Terminal</span></span>

<span data-ttu-id="7ad1d-105">Терминал воспроизведения файлов и терминал записи файлов предоставляют интерфейсы [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) и [**итмултитракктерминал**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) .</span><span class="sxs-lookup"><span data-stu-id="7ad1d-105">The File Playback Terminal and File Recording Terminal expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) and [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interfaces.</span></span> <span data-ttu-id="7ad1d-106">Эти объекты также предоставляют интерфейс [**итмедиаконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , который предоставляет методы для остановки, запуска и навигации по мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-106">These objects also expose the [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) interface, which provides methods for stopping, starting, and media navigation.</span></span>

<span data-ttu-id="7ad1d-107">Терминал воспроизведения файлов предоставляет интерфейс [**итмедиаплайбакк**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , который содержит методы, относящиеся к воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-107">The File Playback Terminal exposes the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface, which has playback-specific methods.</span></span>

<span data-ttu-id="7ad1d-108">Терминал записи файлов предоставляет интерфейс [**итмедиарекорд**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , который предоставляет методы записи.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-108">The File Recording Terminal exposes the [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) interface, which provides recording-specific methods.</span></span>

<span data-ttu-id="7ad1d-109">Терминалы записи файлов и терминалы воспроизведения [файлов, каждый](multitrack-terminals.md) [из которых управляет](track-terminals.md)коллекцией терминалов.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-109">As [multitrack terminals](multitrack-terminals.md), File Recording Terminal and File Playback Terminal each manage a collection of [track terminals](track-terminals.md).</span></span>

 

 
