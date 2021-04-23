---
description: Файловые терминалы можно использовать двумя способами.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Использование файловых терминалов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156771"
---
# <a name="using-file-terminals"></a><span data-ttu-id="6977e-103">Использование файловых терминалов</span><span class="sxs-lookup"><span data-stu-id="6977e-103">Using File Terminals</span></span>

<span data-ttu-id="6977e-104">Файловые терминалы можно использовать двумя способами.</span><span class="sxs-lookup"><span data-stu-id="6977e-104">The file terminals can be used in two ways.</span></span> <span data-ttu-id="6977e-105">Самый простой способ — использовать [**ITBasicCallControl2:: селекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) для выбора файлового терминала (воспроизведения или записи) в ОБЪЕКТЕ вызова TAPI.</span><span class="sxs-lookup"><span data-stu-id="6977e-105">The simplest method is to use [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) to select a file terminal (playback or record) onto a TAPI call object.</span></span> <span data-ttu-id="6977e-106">В этом случае TAPI берет на себя подключение звуковых потоков к терминалам дорожек.</span><span class="sxs-lookup"><span data-stu-id="6977e-106">In this case TAPI takes care of connecting the audio streams to the track terminals.</span></span>

<span data-ttu-id="6977e-107">Второй метод позволяет приложению более точно контролировать сопоставление звуковых потоков с дорожками.</span><span class="sxs-lookup"><span data-stu-id="6977e-107">The second method allows an application to have finer control over the mapping of audio streams to tracks.</span></span> <span data-ttu-id="6977e-108">В этом сценарии приложение перечисляет доступные в вызове потоки, выбирает те, которые записывают (или используют для воспроизведения), создает (или выполняет поиск для воспроизведения) соответствующих дорожек в файле терминала и выбирает записи для потоков вызова.</span><span class="sxs-lookup"><span data-stu-id="6977e-108">In this scenario, the application enumerates the streams available on the call, picks the ones it wants to record (or use for playback), creates (or finds for playback) the corresponding tracks on the file terminal, and selects the tracks on call streams.</span></span>

<span data-ttu-id="6977e-109">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="6977e-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="6977e-110">Простое воспроизведение</span><span class="sxs-lookup"><span data-stu-id="6977e-110">Simple Playback</span></span>](simple-playback.md)
-   [<span data-ttu-id="6977e-111">Воспроизведение с управлением контролем</span><span class="sxs-lookup"><span data-stu-id="6977e-111">Track-Controlled Playback</span></span>](track-controlled-playback.md)
-   [<span data-ttu-id="6977e-112">Простая запись</span><span class="sxs-lookup"><span data-stu-id="6977e-112">Simple Record</span></span>](simple-record.md)
-   [<span data-ttu-id="6977e-113">Запись, контролируемая контролем</span><span class="sxs-lookup"><span data-stu-id="6977e-113">Track-Controlled Record</span></span>](track-controlled-record.md)

 

 



