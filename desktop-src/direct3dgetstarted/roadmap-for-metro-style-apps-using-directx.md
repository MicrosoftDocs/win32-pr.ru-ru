---
title: Дорожная карта для классических приложений DirectX
description: Ниже приведены основные ресурсы, которые помогут вам приступить к использованию DirectX и C++ для разработки настольных приложений с большим объемом графики, таких как игры.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5940e775de65d6d22a9b244d1bd0b881240cf296b740c9a0be9c38f3ab0725a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983894"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Дорожная карта для классических приложений DirectX

Ниже приведены основные ресурсы, которые помогут вам приступить к использованию DirectX и C++ для разработки настольных приложений с большим объемом графики, таких как игры. Это неполный список всех функций или доступных ресурсов.

## <a name="get-started"></a>Начало работы

Ниже приведены некоторые ключевые темы. настройка проекта DirectX, акклиматинг вас на Windows и примеры приложений.

| Раздел | Описание |
|-|-|
| [создание первого Windows приложения с помощью DirectX](building-your-first-directx-app.md) | Используйте это основное руководство, чтобы приступить к разработке приложений DirectX, а затем воспользуйтесь руководством, чтобы продолжить изучение DirectX. |
| [Начало работы с DirectX для Windows](getting-started-with-a-directx-game.md) | Ознакомьтесь с действиями, которые необходимо предпринять, чтобы начать разработку игры с помощью DirectX и C++. |
| [Полный код для платформы DirectX](complete-code-sample-for-using-a-corewindow-with-directx.md) | Получите код для базовой платформы рендеринга DirectX. |
| [Использование Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | В этом разделе показано, как использовать API Microsoft Direct3D 11 для выполнения нескольких распространенных задач. |
| [Руководство по программированию для Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews) | Руководство по программированию содержит сведения об использовании программируемого конвейера Microsoft Direct3D 11 для создания трехмерной графики в реальном времени для настольных приложений. |
| [Средства для графики DirectX](/windows/desktop/direct3dtools/dx-graphics-tools) | Документация по средствам, используемым для поддержки разработки DirectX. |
| [Новые возможности Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | Разделение всех функций, добавленных в последние версии DirectX и Direct3D (в настоящее время 11,2). |
| [Скачайте Visual Studio 2013](https://msdn.microsoft.com/windows/apps/br229516.aspx) | для создания игр Windows Store необходимо иметь Visual Studio Express 2013 для Windows Desktop. обзор Visual Studio см. в статье [разработка приложений магазина Windows с помощью Visual Studio 2012](/previous-versions/windows/apps/br211384(v=win.10)). сведения о новых возможностях в Visual Studio см. в разделе основные сведения о [продуктах для Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [Где находится пакет SDK для DirectX?](../directx-sdk--august-2009-.md) | Содержит рекомендации для разработчики, желающих перенести свои проекты DirectX в Microsoft Visual Studio. |

## <a name="sample-applications"></a>Примеры приложений

| Раздел | Описание |
|-|-|
| [Пример учебника по Direct3D для Win32](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Пример "базовый" учебник по Direct3D для настольных систем. |
| [Пример подготовки видео DirectX](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Пример, демонстрирующий пользовательскую отрисовку видео с помощью Direct3D. |

## <a name="review-key-direct3d-11-concepts"></a>Ознакомьтесь с основными понятиями Direct3D 11

| Раздел | Описание |
|-|-|
| [Графический конвейер](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Охватывает Базовый конвейер графического процесса Direct3D 11. |
| [Отрисовка](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Охватывает модели отрисовки Direct3D, компоненты, шейдеры и поток вызовов API. |
| [Ресурсы](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Охватывает ресурсы Direct3D, такие как буферы и другие типы ресурсов GPU. |
| [Эффекты](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Охватывает создание экземпляров и эффектов для нескольких шейдеров Direct3D.  |
| [Как создать цепочку буферов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Создание цепочки буферов обмена, используемой для рисования пикселов в области экрана. |
| [Как создать устройство и немедленный контекст](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | Как создать абстракцию устройства Direct3D и немедленный контекст для рисования. |
| [Как создать буфер вершин](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | Создание простого списка вершин сетки для обработки графическим процессором. |
| [Как создать буфер индексов](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Создание буфера индекса, позволяющего шейдеру вершин проанализировать порядок вершин в сетке. |
| [Как создать буфер константы](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Как передавать постоянные (единообразные) данные между ЦП и GPU во время подготовки к просмотру. |
| [Как создать текстуру](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Как создать текстуру или другой буферный ресурс, который может быть выборке GPU. |
| [Как инициализировать текстуру из файла](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | Как загрузить текстуру из файла и обработать ее для использования конвейером шейдера. |
| [Как скомпилировать шейдер](../direct3d11/how-to--compile-a-shader.md) | Как скомпилировать шейдер для использования в графическом приложении. |

## <a name="graphics-apis"></a>Графические API

| Раздел | Описание |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Документация по основным API для виртуализации GPU и его ресурсов, а также для рисования графики с помощью унифицированной модели шейдеров. |
| [HLSL Direct3D](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Справочная документация по языку High-Level шейдера, синтаксису и правилам, используемым для определения программ шейдера, выполняемых как часть графического конвейера в унифицированной модели шейдера. |
| [Графический интерфейс DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Документация по интерфейсам API низкого уровня, используемым для получения интерфейса GPU и системных ресурсов. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Документация по интерфейсам API Direct2D, поддерживающим Рисование двумерных примитивов. Как правило, Direct2D используется для настраиваемых пользовательских интерфейсов, обработки изображений и пакетирования и простых игр. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | документация по DirectWriteным интерфейсам api, поддерживающим отрисовку и масштабирование пользовательского шрифта. |
| [Компонент обработки изображений Windows (WIC)](/windows/desktop/wic/-wic-api) | Документация по API-интерфейсам WIC, которые используются для чтения различных форматов растровых изображений и управления ими. |
| [Поверхности DirectDraw (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) для текстур | Документация по API-интерфейсам DDS, которые используются для сжатия 2D-текстур и распаковки в сочетании с API-интерфейсами WIC. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Документация по интерфейсам API Директксмас, поддерживающим Direct3D с набором типов и функций, которые подходят для трехмерной разработки графики в режиме реального времени. (Ранее Кснамас.) |
| [DirectCompute](https://walbourn.github.io/) | Документация по интерфейсам API DirectCompute, используемым для вычислений или функций шейдера общего пользования. |

## <a name="audio-media-and-input-apis"></a>Интерфейсы API аудио, мультимедиа и ввода

| Раздел | Описание |
|-|-|
| [Руководство по программированию для XAudio2](/windows/desktop/xaudio2/programming-guide) | Узел верхнего уровня для основной документации по API XAudio2 Audio. |
| [Справочник по программированию в XAudio2](/windows/desktop/xaudio2/programming-reference) | Узел верхнего уровня для справочной документации по API аудио XAudio2. |
| [Ксинпут по программированию](/windows/desktop/xinput/programming-guide) | Узел верхнего уровня для основной документации по API контроллера Ксинпут. |
| [Справочник по программированию Ксинпут](/windows/desktop/xinput/programming-reference) | Узел верхнего уровня для справочной документации по API контроллера Ксинпут. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Узел верхнего уровня для документации по API воспроизведения Media Foundation (MF) Media (Audio/Video). Как правило, MF используется в играх для воспроизведения звуковой дорожки, тогда как XAudio2 используется для динамического аудио. |

## <a name="port-to-directx-11"></a>Перенос в DirectX 11

| Раздел | Описание |
|-|-|
| [Переход на Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Основные рекомендации по переносу базы кода DirectX 9 в DirectX 11. |
| [Двойные методы программирования для игр](https://walbourn.github.io/) | Подробная запись блога о разработке для \_ \* уровней компонентов DirectX 9 и DirectX 11 \_ \* в одном приложении. |
| [Реализация теневых буферов для уровня функций Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)) | Руководство по реализации теневых карт на уровне функций DirectX 9 \_ \* . |

## <a name="work-with-c"></a>Работа с C++

если вы давно используете C++ на Windowsных платформах, то некоторые могут выглядеть немного иначе. Ниже приведены некоторые ссылки на разделы, которые помогут вам получить маркер в отношении разницы.

> [!NOTE]
> Некоторые из этих статей помогут вам в обслуживании приложения C++/CX. Однако в новых приложениях мы рекомендуем использовать [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt). C++/WinRT — это полностью стандартная проекция языка C++17 для API среды выполнения Windows (WinRT), реализованная как библиотека на основе файлов заголовков и предназначенная для предоставления вам первоклассного доступа к современным интерфейсам API Windows.

| Раздел | Описание |
|-|-|
| [**Справочник по языку Visual C++ (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Страница высокого уровня со ссылкой на содержимое, связанное с C++. |
| [**Краткий справочник (среда выполнения Windows и Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Таблица, в которой содержатся краткие сведения об операторах и ключевых словах расширений компонентов Visual C++ (C++/CX). |
| [**Система типов (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Справочное содержимое для типов, поддерживаемых C++/CX. |
| [**Пространства имен (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | справочное содержимое для пространств имен, содержащих типы, относящиеся к C++, которые можно использовать в приложениях Windows Store. |

| Раздел | Описание |
|-|-|
| [Асинхронное программирование (DirectX и C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | Сведения о асинхронном и многопоточном программировании для приложений и игр DirectX. |
| [Асинхронное программирование на языке C++](/previous-versions/windows/apps/hh780559(v=win.10)) | описывает основные способы использования класса task для получения среда выполнения Windows асинхронных методов. |
| [**Класс Task (среда выполнения с параллелизмом)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Справочная документация по классу Task. |
| [Параллелизм задач (среда выполнения с параллелизмом)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Подробное обсуждение класса Task и его использование. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>дополнительные полезные библиотеки для программирования Windows C++

| Раздел | Описание |
|-|-|
| [Библиотека стандартных шаблонов C++](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Windows Типы среды выполнения хорошо воспроизводятся с использованием стандартных типов библиотек шаблонов. большинство приложений C++ Windows магазина используют стандартные коллекции и алгоритмы библиотек шаблонов, за исключением границ ABI. |
| [Библиотека параллельных шаблонов](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | PPL предоставляет алгоритмы и типы, которые упрощают параллелизм задач и параллелизм данных в ЦП.  |
| [C++ Accelerated Massive Parallelism (C++ AMP)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP предоставляет доступ к GPU для обеспечения параллелизма данных общего назначения на видеоадаптерах, поддерживающих DirectX 11. |

## <a name="blogs-and-other-resources"></a>Блоги и другие ресурсы

| Раздел | Описание |
|-|-|
| [блоги для Windows и DirectX](https://walbourn.github.io/) | Регулярно обновляемый блог с помощью ключевого участника DirectX dev и всего отличного ресурса для DirectX разработчики. |
| [Windows Блог разработчиков DirectX](https://devblogs.microsoft.com/directx/) | официальный блог Windows DirectX. |
| [Блог Шон харгреаве для DirectX](https://www.shawnhargreaves.com/blogindex.html)) | блог разработки от другого хорошо соблюдающий Windows участника DirectX dev. |
| [Набор инструментов DirectX](https://directxtk.codeplex.com/) | Сайт CodePlex для набора средств DirectX (Дкстк), который содержит ряд полезных API поддержки для загрузки сеток, воспроизведения звуков и других распространенных поведений. |
| [Библиотеки обработки текстур DirectXTex](https://directxtex.codeplex.com/) | Сайт плекса кода для библиотеки обработки текстур DirectX (Дкстекс), который содержит API-интерфейсы поддержки для обработки текстур и сжатия и распаковки. |