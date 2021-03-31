---
title: Стирание перезаписываемого компакт-диска
description: Стирание перезаписываемого компакт-диска
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Проигрыватель Windows Media, запись компакт-дисков
- Объектная модель проигрывателя Windows Media, запись компакт-дисков
- Объектная модель, запись компакт-диска
- Элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Элемент управления ActiveX, запись компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Проигрыватель Windows Media Mobile, запись компакт-дисков
- Запись компакт-дисков, очистка перезаписываемых компактных дисков
- запись компакт-дисков, очистка перезаписываемых компакт-дисков
- Удаление перезаписываемых компакт-дисков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069568"
---
# <a name="erasing-a-rewritable-cd"></a>Стирание перезаписываемого компакт-диска

Интерфейс [ивмпкдромбурн](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) предоставляет метод для СТИРАНИЯ дисков CD-RW. Перед стиранием компакт-диска необходимо убедиться, что операция поддерживается. Дополнительные сведения см. [в разделе Получение состояния диска и](retrieving-the-drive-and-disc-status.md)диска.

Чтобы начать Стирание содержимого перезаписываемого компакт-диска, вызовите метод [ивмпкдромбурн:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Запись компакт-диска**](burning-a-cd.md)
</dt> <dt>

[**Получение интерфейса записи компакт-дисков**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Запуск процесса записи**](starting-the-burn-process.md)
</dt> <dt>

[**Получение состояния диска и диска**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Получение состояния записи**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




