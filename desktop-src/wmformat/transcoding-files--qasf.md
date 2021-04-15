---
title: Перекодирование файлов (КАСФ)
description: Перекодирование файлов (КАСФ)
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- Windows Media Format SDK, перекодирование файлов (КАСФ)
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), файлы для перекодирования (КАСФ)
- ASF (Расширенный системный формат), перекодирование файлов (КАСФ)
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, перекодирование файлов (КАСФ)
- Windows Media Format SDK, КАСФ
- Расширенный системный формат (ASF), КАСФ
- ASF (Расширенный системный формат), КАСФ
- DirectShow, КАСФ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14387a65538d411bcd41b4b907f2adbab2089f71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104555559"
---
# <a name="transcoding-files-qasf"></a><span data-ttu-id="b99b0-114">Перекодирование файлов (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="b99b0-114">Transcoding Files (QASF)</span></span>

<span data-ttu-id="b99b0-115">Вы можете создать граф фильтра для перекодирования файлов с помощью [модуля записи WM ASF](wm-asf-writer-filter.md) различными способами.</span><span class="sxs-lookup"><span data-stu-id="b99b0-115">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="b99b0-116">Самым простым способом является совместное создание, Настройка и Добавление модуля записи WM ASF в граф фильтра, а затем использование метода **играфбуилдер:: renderFile** для автоматической сборки графа.</span><span class="sxs-lookup"><span data-stu-id="b99b0-116">The easiest way is to co-create, configure, and add the WM ASF Writer to the filter graph, and then use the **IGraphBuilder::RenderFile** method to build the graph automatically.</span></span>

<span data-ttu-id="b99b0-117">Другой способ — добавить каждый фильтр на диаграмму вручную и соединить эти контакты.</span><span class="sxs-lookup"><span data-stu-id="b99b0-117">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="b99b0-118">После добавления модуля записи WM ASF настройте его с помощью методов **иконфигасфвритер** , если профиль по умолчанию не подходит, и подключите входные ПИН-коды модуля записи WM ASF к соответствующим выходным контактам в вышестоящем фильтре.</span><span class="sxs-lookup"><span data-stu-id="b99b0-118">After adding the WM ASF Writer, configure it by using the **IConfigAsfWriter** methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="b99b0-119">На следующем рисунке показана типичная конфигурация графа фильтра модуля записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="b99b0-119">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![Типичные графы фильтра перекодировки](images/asf-transcode.png)

 

 




