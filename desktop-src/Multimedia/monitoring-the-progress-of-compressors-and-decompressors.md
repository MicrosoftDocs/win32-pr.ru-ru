---
title: Мониторинг хода сжатия и распаковки
description: Мониторинг хода сжатия и распаковки
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- Диспетчер сжатия видео (ВКМ), мониторинг
- ВКМ (диспетчер сжатия видео), мониторинг
- Функция Иксетстатуспрок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681462"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a><span data-ttu-id="89ffb-106">Мониторинг хода сжатия и распаковки</span><span class="sxs-lookup"><span data-stu-id="89ffb-106">Monitoring the Progress of Compressors and Decompressors</span></span>

<span data-ttu-id="89ffb-107">Приложение может отслеживать ход выполнения длительной операции, выполняемой программой сжатия или распаковки, отправляя ей адрес функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="89ffb-107">Your application can monitor the progress of a lengthy operation performed by a compressor or decompressor by sending it the address of a callback function.</span></span> <span data-ttu-id="89ffb-108">Для отправки адреса в программу сжатия или распаковку можно использовать функцию [**иксетстатуспрок**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) .</span><span class="sxs-lookup"><span data-stu-id="89ffb-108">You can use the [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) function to send the address to the compressor or decompressor.</span></span> <span data-ttu-id="89ffb-109">Когда программа сжатия или распаковки получает этот адрес, она отправляет в функцию сообщения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="89ffb-109">When the compressor or decompressor receives this address, it sends status messages to the function.</span></span> <span data-ttu-id="89ffb-110">Эти сообщения указывают, что операция запускается, останавливается, выдается или продолжается.</span><span class="sxs-lookup"><span data-stu-id="89ffb-110">These messages indicate whether the operation is starting, stopping, yielding, or proceeding.</span></span>

 

 




