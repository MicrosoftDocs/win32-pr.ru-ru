---
description: Демонстрирует, как реализовать команду оболочки с помощью методов Експлореркомманд и Експлореркоммандстате.
title: 'Пример: команда в проводнике'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912923"
---
# <a name="explorer-command-verb-sample"></a>Пример: команда в проводнике

Демонстрирует, как реализовать команду оболочки с помощью методов Експлореркомманд и Експлореркоммандстате.

В этом разделе содержатся следующие подразделы.

-   [Требования](#requirements)
-   [Загрузка образца](#downloading-the-sample)
-   [Создание примера](#building-the-sample)
-   [Запуск примера](#running-the-sample)

## <a name="requirements"></a>Требования



| Продукт                                | Минимальная версия продукта |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Загрузка образца

| Расположение      | URL-адрес пути                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Пример Експлореркоммандверб](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из командной строки, выполните следующую команду:

1.  Откройте окно командной строки и перейдите в каталог проекта **експлореркоммандверб** .
2.  Введите `msbuild ExplorerCommandVerb.sln`.

Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  Откройте проводник Windows и перейдите в каталог проекта **експлореркоммандверб** .
2.  Дважды щелкните значок файла Експлореркоммандверб. sln, чтобы открыть проект в Visual Studio.
3.  В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  Перейдите в каталог, содержащий ExplorerCommandVerb.dll, с помощью командной строки или проводника Windows. Убедитесь, что используется 64-разрядный файл DLL в 64-разрядной версии Windows.
2.  В командной строке введите `regsvr32.exe ExplorerCommandVerb.dll` .
3.  Если щелкнуть правой кнопкой мыши txt-файл, в контекстном меню будут отображаться две новые команды.

 

 



