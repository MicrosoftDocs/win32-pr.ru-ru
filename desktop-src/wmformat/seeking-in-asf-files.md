---
title: Поиск в файлах ASF (пакет SDK для Windows Media Format 11)
description: Поиск в файлах ASF
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, поиск в файлах ASF
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), Поиск
- ASF (Расширенный системный формат), Поиск
- DirectShow, поиск в файлах ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18389ded80f0202564cba0ce6384b5ff02d26fdd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070949"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Поиск в файлах ASF (пакет SDK для Windows Media Format 11)

[Средство чтения WM ASF](wm-asf-reader-filter.md)через его интерфейс **имедиасикинг** может выполнять очень точное временное Поиск содержимого на основе Windows Media с временным индексом. (Все индексируемые фреймы содержимого также содержат временный индекс). Гарантируется, что поиск в точно-ориентированном поиске не поддерживается напрямую в модуле чтения WM ASF, но существует способ сделать это, если требуется эта функция. Во-первых, используйте пакет SDK для формата Windows Media, чтобы создать экземпляр синхронного объекта Reader, открыть файл, получить метку времени, связанную с указанным кадром, а затем использовать интерфейс DirectShow **имедиасикинг** для поиска в это время. Интерфейс DirectShow **ивидеофраместеп** не поддерживает точное Поиск содержимого на основе Windows Media. Пример Дссикфм в пакете SDK для формата Windows Media демонстрирует, как выполнять поиск с точностью в виде кадров с помощью средства чтения WM ASF.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Фильтр чтения WM ASF**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




