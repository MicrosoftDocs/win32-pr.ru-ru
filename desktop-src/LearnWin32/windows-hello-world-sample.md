---
title: Windows Hello Пример мира
description: в этом примере приложения показано, как создать минимальную Windows программу.
ms.assetid: ec316ad8-d01d-4558-91b6-19fdbba3d520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a437c1b576ab7c1f46341abee1c446d69aaec29585a1ed3966bd1dd289747cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387453"
---
# <a name="windows-hello-world-sample"></a>Windows Hello Пример мира

в этом примере приложения показано, как создать минимальную Windows программу.

## <a name="description"></a>Описание

пример приложения Windows Hello World создает и отображает пустое окно, как показано на снимке экрана ниже. Этот пример обсуждается в [модуле 1. первая программа Windows](your-first-windows-program.md).

![снимок экрана с примером программы.](images/window01.png)

## <a name="downloading-the-sample"></a>Загрузка образца

Этот пример доступен [здесь](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/HelloWorld).

чтобы скачать его, перейдите к корню примера репозитория на GitHub ([microsoft/Windows-классическая-samples](https://github.com/microsoft/Windows-classic-samples/)) и нажмите кнопку **клонировать или скачать** , чтобы загрузить zip-файл всех примеров на компьютер. Затем распакуйте папку.

чтобы открыть пример в Visual Studio, выберите **файл/открыть/Project/солутион**, а затем перейдите в папку, в которой была распакована папка, и **Windows-классическая-samples-master/samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp**. Откройте файл **HelloWorld. sln**.

После загрузки образца необходимо обновить его для работы с Windows 10. в меню **Project** в Visual Studio выберите пункт **свойства**. обновите **версию Windows SDK** до пакета SDK для Windows 10, например 10.0.17763.0 или более. затем измените **набор инструментов платформы** на Visual Studio 2017 или более. Теперь можно запустить пример, нажав клавишу F5!


## <a name="related-topics"></a>Связанные темы

* [сведения о программе для Windows: пример кода](learn-to-program-for-windows--sample-code.md)
* [Модуль 1. первая программа Windows](your-first-windows-program.md)
