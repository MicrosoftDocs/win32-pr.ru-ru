---
description: В примере кода Ифилтерсампле показано, как создать базовый класс IFilter для реализации интерфейса IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: ифилтерсампле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692194"
---
# <a name="ifiltersample"></a>ифилтерсампле

В примере кода Ифилтерсампле показано, как создать базовый класс IFilter для реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

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
| GitHub        | [ифилтерсампле](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.

## <a name="building-the-sample"></a>Построение образца

1. Откройте проводник Windows и перейдите в каталог проекта **филтербасе** .
2. Дважды щелкните значок файла Филтербасе. sln, чтобы открыть проект в Visual Studio.

    > [!NOTE]  
    > Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия. Это не повлияет на поведение образца.

3. В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1. Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.
2. В командной строке введите `FilterBase.exe` или в проводнике Windows дважды щелкните значок FilterBase.exe.

## <a name="related-topics"></a>См. также

### <a name="reference"></a>Справочник

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a>Основные понятия

[Разработка обработчиков фильтров](-search-ifilter-conceptual.md)

### <a name="other-samples"></a>Другие примеры

[Поиск примеров кода](-search-samples-ovw.md)
