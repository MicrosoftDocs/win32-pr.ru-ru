---
description: В примере кода Дсеарч показано, как создать класс для статического консольного приложения, чтобы запросить Поиск Windows с помощью сборки Microsoft. Search. Interop для Исеарчкуерихелпер.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: дсеарч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692195"
---
# <a name="dsearch"></a>дсеарч

В примере кода Дсеарч показано, как создать класс для статического консольного приложения, чтобы запросить Поиск Windows с помощью сборки Microsoft. Search. Interop для [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).

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

| Расположение      | URL-адрес пути                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Пример Дсеарч](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.

## <a name="building-the-sample"></a>Построение образца

1. Откройте проводник Windows и перейдите в каталог проекта **дсеарч** .
2. Дважды щелкните значок файла Дсеарч. sln, чтобы открыть проект в Visual Studio.
  
    > [!NOTE]  
    > Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия. Это не повлияет на поведение образца.

3. В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1. Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.
2. В командной строке введите `DSearch.exe` или в проводнике Windows дважды щелкните значок DSearch.exe.

## <a name="related-topics"></a>См. также

### <a name="reference"></a>Справочник

[**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a>Другие примеры

[Поиск примеров кода](-search-samples-ovw.md)
