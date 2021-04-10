---
description: Пример кода Всоледб демонстрирует использование библиотеки ATL OLE DB доступ к приложениям Windows Search и демонстрирует два дополнительных метода получения результатов из службы поиска Windows.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: всоледб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896930"
---
# <a name="wsoledb"></a>всоледб

Пример кода Всоледб демонстрирует использование библиотеки ATL OLE DB доступ к приложениям Windows Search и демонстрирует два дополнительных метода получения результатов из службы поиска Windows.

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
| GitHub        | [Пример Всоледб](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.

## <a name="building-the-sample"></a>Построение образца

1. Откройте проводник Windows и перейдите в каталог проекта **всоледб** .
2. Дважды щелкните значок файла Всоледб. sln, чтобы открыть проект в Visual Studio.
  
    > [!NOTE]  
    > Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия. Это не повлияет на поведение образца.

3. В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1. Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.
2. В командной строке введите `WSOleDB.exe` или в проводнике Windows дважды щелкните значок WSOleDB.exe.

## <a name="related-topics"></a>См. также

### <a name="reference"></a>Справочник

[**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**исеарчманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a>Основные понятия

[Общие сведения о программировании OLE DB](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Другие примеры

[Поиск примеров кода](-search-samples-ovw.md)
