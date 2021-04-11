---
title: Пример Hello World Windows
description: В этом примере приложения показано, как создать минимальную программу Windows.
ms.assetid: ec316ad8-d01d-4558-91b6-19fdbba3d520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932d3b0c524c643022904b08402507d4a603adb
ms.sourcegitcommit: e084958628fb997e9e11fe08574d82edbba07dbf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2019
ms.locfileid: "104332859"
---
# <a name="windows-hello-world-sample"></a>Пример Hello World Windows

В этом примере приложения показано, как создать минимальную программу Windows.

## <a name="description"></a>Описание

Пример приложения Windows Hello World создает и отображает пустое окно, как показано на снимке экрана ниже. Этот пример обсуждается в [модуле 1. Ваша первая программа Windows](your-first-windows-program.md).

![снимок экрана с примером программы.](images/window01.png)

## <a name="downloading-the-sample"></a>Загрузка образца

Этот пример доступен [здесь](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/HelloWorld).

Чтобы скачать его, перейдите к корню примера репозитория на сайте GitHub ([Microsoft/Windows-классическая-Samples](https://github.com/microsoft/Windows-classic-samples/)) и нажмите кнопку **клонировать или скачать** , чтобы загрузить ZIP-файл всех примеров на компьютер. Затем распакуйте папку.

Чтобы открыть пример в Visual Studio, выберите **файл/открыть/проект/решение**, а затем перейдите в папку, в которой вы разархивированы, и **Windows-классическая-Samples-Master/Samples/Win7Samples/Begin/LearnWin32/HelloWorld/cpp**. Откройте файл **HelloWorld. sln**.

После загрузки образца необходимо обновить его для работы с Windows 10. В меню **проект** в Visual Studio выберите пункт **свойства**. Обновите **версию Windows SDK** до пакета SDK для Windows 10, например 10.0.17763.0 или более. Затем измените **набор инструментов платформы** на Visual Studio 2017 или более высокую. Теперь можно запустить пример, нажав клавишу F5!


## <a name="related-topics"></a>См. также

* [Сведения о программе для Windows: пример кода](learn-to-program-for-windows--sample-code.md)
* [Модуль 1. Ваша первая программа Windows](your-first-windows-program.md)
