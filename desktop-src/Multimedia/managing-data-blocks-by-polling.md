---
title: Управление блоками данных путем опроса
description: Управление блоками данных путем опроса
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- звуковая волна, опрос блоков данных
- звуковые блоки данных, опрос
- Опрос блоков звуковых данных
- Структура ВАВЕХДР
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069865"
---
# <a name="managing-data-blocks-by-polling"></a><span data-ttu-id="40f90-107">Управление блоками данных путем опроса</span><span class="sxs-lookup"><span data-stu-id="40f90-107">Managing Data Blocks by Polling</span></span>

<span data-ttu-id="40f90-108">Помимо использования функции обратного вызова, можно опросить элемент **dwFlags** структуры [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , чтобы определить, когда звуковое устройство завершается с блоком данных.</span><span class="sxs-lookup"><span data-stu-id="40f90-108">In addition to using a callback function, you can poll the **dwFlags** member of a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to determine when an audio device is finished with a data block.</span></span> <span data-ttu-id="40f90-109">Иногда лучше опросить **dwFlags** , чем ожидать, пока другой механизм получит сообщения от драйверов.</span><span class="sxs-lookup"><span data-stu-id="40f90-109">Sometimes it is better to poll **dwFlags** than to wait for another mechanism to receive messages from the drivers.</span></span> <span data-ttu-id="40f90-110">Например, после вызова функции [**вавеаутресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) для освобождения незавершенных блоков данных можно сразу же опросить, чтобы убедиться, что блоки данных были освобождены до вызова [**вавеаутунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) и освободить память для блока данных.</span><span class="sxs-lookup"><span data-stu-id="40f90-110">For example, after you call the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function to release pending data blocks, you can immediately poll to be sure that the data blocks have been released before calling [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) and freeing the memory for the data block.</span></span>

<span data-ttu-id="40f90-111">\_Для проверки элемента **dwFlags** можно использовать флаг вхдр Done.</span><span class="sxs-lookup"><span data-stu-id="40f90-111">You can use the WHDR\_DONE flag to test the **dwFlags** member.</span></span> <span data-ttu-id="40f90-112">Как только \_ флаг вхдр Done задается в элементе **DwFlags** структуры **вавехдр** , драйвер завершается с блоком данных.</span><span class="sxs-lookup"><span data-stu-id="40f90-112">As soon as the WHDR\_DONE flag is set in the **dwFlags** member of the **WAVEHDR** structure, the driver is finished with the data block.</span></span>

 

 