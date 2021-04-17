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
# <a name="starting-the-rip-process"></a>Запуск процесса копирования

После получения интерфейса копирования, как описано в предыдущем разделе, запустите процесс копирования, вызвав [ивмпкдромрип:: стартрип](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



Можно прерывать операцию копирования путем вызова [ивмпкдромрип:: стоприп](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Копирование компакт-диска**](ripping-a-cd.md)
</dt> <dt>

[**Получение интерфейса копирования данных с компакт-диска**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Получение состояния копирования**](retrieving-the-rip-status.md)
</dt> <dt>

[**Выбор элементов для копирования**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




