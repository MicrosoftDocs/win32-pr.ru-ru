---
description: DVD-приложения
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: DVD-приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341852"
---
# <a name="dvd-applications"></a>DVD-приложения

DirectShow предоставляет компонент, называемый фильтром источника « [DVD Navigator](dvd-navigator-filter.md) », который упрощает задачи навигации по DVD в C++. DVD-навигатор содержит все возможности, которые можно найти на полнофункциональном автономном DVD-проигрывателе, а также дополнительные возможности для воспроизведения DVD-дисков на персональных компьютерах. С помощью DVD Navigator, C++ и разработчиков сценариев можно создавать полнофункциональные DVD-приложения, не обращаясь к спецификации DVD. Навигатор DVD, в координации с фильтрами декодера, также управляет региональным управлением и защитой авторских прав (CSS и аналоговая защита от копирования), изолируя разработчиков приложений от этих сведений.

Фильтр "Навигатор DVD" работает во всем DVD-Video том, который состоит из файлов в \_ каталоге Video TS. В отличие от большинства фильтров источника DirectShow, работающих с отдельными потоками или файлами, Навигатор DVD использует DVD-Video структуру заголовков, глав и кодов времени. Разработчики, желающие воспроизвести отдельные файлы MPEG-2 в DirectShow, должны использовать [демультиплексор MPEG-2](mpeg-2-demultiplexer.md) вместо фильтра DVD Navigator. Дополнительные сведения см. [в статье поддержка MPEG-2 в DirectShow](mpeg-2-support-in-directshow.md) .

> [!Note]  
> Для воспроизведения DVD пользователь должен иметь декодер MPEG-2.

 

Этот раздел содержит следующие подразделы.

-   [Функции поддержки DVD в DirectShow](dvd-support-features-in-directshow.md)
-   [Основные сведения о DVD](dvd-basics.md)
-   [Создание графа фильтра DVD](building-the-dvd-filter-graph.md)
-   [Получение указателей на DVD-интерфейсах](obtaining-the-dvd-interface-pointers.md)
-   [Команды DVD](dvd-commands.md)
-   [Определение допустимых операций DVD](identifying-valid-dvd-operations.md)
-   [Синхронизация команд DVD](synchronizing-dvd-commands.md)
-   [Поток данных в навигаторе DVD](data-flow-in-the-dvd-navigator.md)
-   [Обработка уведомлений о событиях DVD](handling-dvd-event-notifications.md)
-   [Работа с меню DVD](working-with-dvd-menus.md)
-   [Потоки аудио и субтитров](audio-and-subpicture-streams.md)
-   [Применение уровней родительского управления](enforcing-parental-management-levels.md)
-   [Сохранение и восстановление объектов Двдстате](saving-and-restoring-dvdstate-objects.md)
-   [Работа с текстовыми строками DVD](working-with-dvd-text-strings.md)
-   [Воспроизведение звуковых потоков Караоке](playing-karaoke-audio-streams.md)
-   [Обработка извлечения с диска](handling-disc-ejections.md)
-   [Усовершенствования воспроизведения DVD в Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [Конфигурация графа фильтра DVD](dvd-filter-graph-configuration.md)
-   [Ярлыки на страницы справочника по C++ DVD](shortcuts-to-c-dvd-reference-pages.md)

Ссылки на разработку декодеров DVD/MPEG2 см. [в статье Разработка декодеров DVD в DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование DirectShow](using-directshow.md)
</dt> </dl>

 

 



