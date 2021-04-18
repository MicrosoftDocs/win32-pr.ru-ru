---
description: В примере кода Структуредкуерисампле показано, как считывать строки из консоли, анализировать их с помощью системной схемы и отображать результирующие деревья условий.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: структуредкуерисампле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692191"
---
# <a name="structuredquerysample"></a>структуредкуерисампле

В примере кода Структуредкуерисампле показано, как считывать строки из консоли, анализировать их с помощью системной схемы и отображать результирующие деревья условий.

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
| GitHub        | [структуредкуерисампле](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.

## <a name="building-the-sample"></a>Построение образца

1. Откройте проводник Windows и перейдите в каталог проекта **структуредкуерисампле** .
2. Дважды щелкните значок файла Структуредкуерисампле. sln, чтобы открыть проект в Visual Studio.

    > [!NOTE]  
    > Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия. Это не повлияет на поведение образца.

3. В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1. Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.
2. В командной строке введите `StructuredQuerySample.exe` или в проводнике Windows дважды щелкните значок StructuredQuerySample.exe.

## <a name="related-topics"></a>См. также

### <a name="reference"></a>Справочник

[**икондитион**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[**ICondition2**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[**икондитионфактори**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[**IConditionFactory2**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[**икондитионженератор**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[**икуерипарсер**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[**икуерипарсерманажер**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[**икуерисолутион**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a>Другие примеры

[Поиск примеров кода](-search-samples-ovw.md)
