---
title: Запуск процесса копирования
description: Запуск процесса копирования
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Проигрыватель Windows Media, копирование компакт-дисков
- Объектная модель проигрывателя Windows Media, копирование компакт-дисков
- Объектная модель, копирование компакт-дисков
- Элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Элемент управления ActiveX, копирование компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Проигрыватель Windows Media Mobile, копирование компакт-дисков
- Копирование компакт-дисков, запуск процесса копирования с диска
- Копирование компакт-дисков, запуск процесса копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691444"
---
# <a name="starting-the-rip-process"></a><span data-ttu-id="53c78-112">Запуск процесса копирования</span><span class="sxs-lookup"><span data-stu-id="53c78-112">Starting the Rip Process</span></span>

<span data-ttu-id="53c78-113">После получения интерфейса копирования, как описано в предыдущем разделе, запустите процесс копирования, вызвав [ивмпкдромрип:: стартрип](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span><span class="sxs-lookup"><span data-stu-id="53c78-113">After you have retrieved the ripping interface as explained in the previous section, start the ripping process by calling [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span>


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



<span data-ttu-id="53c78-114">Можно прерывать операцию копирования путем вызова [ивмпкдромрип:: стоприп](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span><span class="sxs-lookup"><span data-stu-id="53c78-114">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a><span data-ttu-id="53c78-115">См. также</span><span class="sxs-lookup"><span data-stu-id="53c78-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c78-116">**Копирование компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="53c78-116">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="53c78-117">**Получение интерфейса копирования данных с компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="53c78-117">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="53c78-118">**Получение состояния копирования**</span><span class="sxs-lookup"><span data-stu-id="53c78-118">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="53c78-119">**Выбор элементов для копирования**</span><span class="sxs-lookup"><span data-stu-id="53c78-119">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




