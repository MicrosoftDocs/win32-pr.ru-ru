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
ms.openlocfilehash: 3ec8f4c88ea01aad410e982fc24fd248f3c1826d8c8657e904844b535e621fd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719186"
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

чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  откройте обозреватель Windows и перейдите в каталог проекта **експлореркоммандверб** .
2.  Дважды щелкните значок файла Експлореркоммандверб. sln, чтобы открыть проект в Visual Studio.
3.  В меню **Построение** выберите пункт **Построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  перейдите в каталог, содержащий ExplorerCommandVerb.dll, используя командную строку или обозреватель Windows. Убедитесь, что используется 64-разрядный файл DLL на 64-разрядной Windows.
2.  В командной строке введите `regsvr32.exe ExplorerCommandVerb.dll` .
3.  Если щелкнуть правой кнопкой мыши файл .txt, в контекстном меню будут отображаться две новые команды.

 

 



