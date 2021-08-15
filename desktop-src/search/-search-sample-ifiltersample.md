---
description: В примере кода Ифилтерсампле показано, как создать базовый класс IFilter для реализации интерфейса IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: ифилтерсампле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f015166d0366152d07a5fb8d182edcb5422112c66f016219970fef9b889df3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863737"
---
# <a name="ifiltersample"></a>ифилтерсампле

В примере кода Ифилтерсампле показано, как создать базовый класс IFilter для реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

В этом разделе содержатся следующие подразделы.

- [Требования](#requirements)
- [Загрузка образца](#downloading-the-sample)
- [Создание примера](#building-the-sample)
- [Запуск примера](#running-the-sample)
- [Связанные темы](#related-topics)

## <a name="requirements"></a>Requirements (Требования)

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
> для всех версий Windows, включая Windows 7, рекомендуется загружать образцы непосредственно из GitHub для наиболее актуальной версии.

## <a name="building-the-sample"></a>Построение образца

1. откройте обозреватель Windows и перейдите в каталог проекта **филтербасе** .
2. Дважды щелкните значок файла Филтербасе. sln, чтобы открыть проект в Visual Studio.

    > [!NOTE]  
    > файл sln был создан в более ранней версии Visual Studio, поэтому его обновление потребуется при использовании Visual Studio 2012 или более поздних версий. Это не повлияет на поведение образца.

3. В меню **Построение** выберите пункт **Построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1. перейдите в каталог, содержащий новый исполняемый файл, используя окно командной строки или проводник Windows.
2. в командной строке введите `FilterBase.exe` или в Windows Explorer дважды щелкните значок FilterBase.exe.

## <a name="related-topics"></a>Связанные темы

### <a name="reference"></a>Справочник

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a>Основные понятия

[Разработка обработчиков фильтров](-search-ifilter-conceptual.md)

### <a name="other-samples"></a>Другие примеры

[Поиск примеров кода](-search-samples-ovw.md)
