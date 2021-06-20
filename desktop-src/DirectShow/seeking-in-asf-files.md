---
description: Узнайте, как читатель WM ASF может выполнять очень точную повременное Поиск содержимого на основе Windows Media с временным индексом в DirectShow.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Поиск в файлах ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ffc570536463b86a88e1f26be338bd748c790c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405587"
---
# <a name="seeking-in-asf-files-directshow"></a>Поиск в файлах ASF (DirectShow)

[Средство чтения WM ASF](wm-asf-reader-filter.md)через его интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) может выполнять очень точное временное Поиск содержимого на основе Windows Media с временным индексом. (Все индексируемые фреймы содержимого также содержат временный индекс). Гарантируется, что поиск в точно-ориентированном поиске не поддерживается напрямую в модуле чтения WM ASF, но существует способ сделать это, если требуется эта функция. Во-первых, используйте пакет SDK для формата Windows Media, чтобы создать экземпляр синхронного объекта Reader, открыть файл, получить метку времени, связанную с указанным кадром, а затем использовать интерфейс DirectShow **имедиасикинг** для поиска в это время. Интерфейс [**ивидеофраместеп**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) не поддерживает точное Поиск содержимого на основе Windows Media.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



