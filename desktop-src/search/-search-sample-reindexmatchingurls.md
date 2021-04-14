---
description: 'В примере кода Реиндексматчингурлс показано, как предоставить три способа указания файлов для повторного индексирования: URL-адреса, соответствующие типу файла, типу MIME или указанному предложению WHERE.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: реиндексматчингурлс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497067"
---
# <a name="reindexmatchingurls"></a>реиндексматчингурлс

В примере кода Реиндексматчингурлс показано, как предоставить три способа указания файлов для повторного индексирования: URL-адреса, соответствующие типу файла, типу MIME или указанному предложению WHERE.

В этом разделе содержатся следующие подразделы.

- [Требования](#requirements)
- [Загрузка образца](#downloading-the-sample)
- [Создание примера](#building-the-sample)
- [Запуск примера](#running-the-sample)
- [См. также](#related-topics)

## <a name="requirements"></a>Требования

| Продукт     | Версия продукта          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 или 10    |
| Пакет Windows SDK | 7,0 или выше           |

## <a name="downloading-the-sample"></a>Загрузка образца

Этот пример доступен в следующем расположении.

| Расположение      | URL-адрес пути                                                                      |
|---------------|-------------------------------------------------------------------------------|
| GitHub  | [Пример Реиндексматчингурлс](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.

## <a name="building-the-sample"></a>Построение образца

1. Откройте проводник Windows и перейдите в каталог проекта **реиндексматчингурлс** . Например, полный путь установки по умолчанию — `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .
2. Дважды щелкните значок для повторного индексирования файла. sln, чтобы открыть проект в Visual Studio.
  
    > [!NOTE]  
    > Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия. Это не повлияет на поведение образца.

3. В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1. Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.
2. В командной строке введите `Reindex.exe` или в проводнике Windows дважды щелкните значок Reindex.exe.

## <a name="related-topics"></a>См. также

### <a name="reference"></a>Справочник

[**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**исеарчманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[**исеарчвиевчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[**определение приоритетов \_ флагов**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a>Другие примеры

[Поиск примеров кода](-search-samples-ovw.md)
