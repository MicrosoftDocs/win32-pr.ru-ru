---
description: В примере кода ВССКЛ показано, как взаимодействовать между Microsoft OLE DB и Windows Search с помощью язык SQL (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: всскл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896929"
---
# <a name="wssql"></a>всскл

В примере кода ВССКЛ показано, как взаимодействовать между Microsoft OLE DB и Windows Search с помощью язык SQL (SQL).

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
| GitHub        | [Пример ВССКЛ](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.

## <a name="building-the-sample"></a>Построение образца

1. Откройте проводник Windows и перейдите в каталог проекта **всскл** .
2. Дважды щелкните значок файла ВССКЛ. sln, чтобы открыть проект в Visual Studio.
    > [!NOTE]  
    > Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия. Это не повлияет на поведение образца.

3. В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1. Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.
2. В командной строке введите `WSSQL.exe` или в проводнике Windows дважды щелкните значок WSSQL.exe.

## <a name="related-topics"></a>См. также

### <a name="conceptual"></a>Основные понятия

[Использование синтаксиса SQL для поиска Windows](-search-sql-windowssearch-entry.md)

[Общие сведения о языке запросов](-search-sql-generalqueryinfo.md)

[Общие сведения о программировании OLE DB](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Другие примеры

[Поиск примеров кода](-search-samples-ovw.md)
