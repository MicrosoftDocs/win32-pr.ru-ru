---
description: Поиск в файлах ASF
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Поиск в файлах ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e957fbdf7ed7df1a9cb38b14e39d384b15ab25b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537118"
---
# <a name="seeking-in-asf-files-directshow"></a>Поиск в файлах ASF (DirectShow)

[Средство чтения WM ASF](wm-asf-reader-filter.md)через его интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) может выполнять очень точное временное Поиск содержимого на основе Windows Media с временным индексом. (Все индексируемые фреймы содержимого также содержат временный индекс). Гарантируется, что поиск в точно-ориентированном поиске не поддерживается напрямую в модуле чтения WM ASF, но существует способ сделать это, если требуется эта функция. Во-первых, используйте пакет SDK для формата Windows Media, чтобы создать экземпляр синхронного объекта Reader, открыть файл, получить метку времени, связанную с указанным кадром, а затем использовать интерфейс DirectShow **имедиасикинг** для поиска в это время. Интерфейс [**ивидеофраместеп**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) не поддерживает точное Поиск содержимого на основе Windows Media.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



