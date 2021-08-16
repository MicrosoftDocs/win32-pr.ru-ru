---
description: Демонстрирует, как реализовать команду оболочки с помощью метода CreateProcess.
title: 'Пример: команда CreateProcess'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c0af34d5ec9f687ec6c58bb73f337b38d512527c0ace4bd20eae12d49c87a62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858344"
---
# <a name="createprocess-verb-sample"></a>Пример: команда CreateProcess

Демонстрирует, как реализовать команду оболочки с помощью метода CreateProcess.

В этом разделе содержатся следующие подразделы.

-   [Описание](#description)
-   [Требования](#requirements)
-   [Загрузка образца](#downloading-the-sample)
-   [Создание примера](#building-the-sample)
-   [Запуск примера](#running-the-sample)

## <a name="description"></a>Описание

Команды на основе CreateProcess зависят от запуска исполняемого файла и передачи ему аргумента командной строки. Этот метод не так эффективен, как методы Дроптаржет и ExecuteCommand, но он обеспечивает желаемое поведение вне процесса.

## <a name="requirements"></a>Требования



| Продукт                                | Минимальная версия продукта |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Загрузка образца

| Расположение      | URL-адрес пути                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Пример Креатепроцессверб](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из командной строки, выполните следующую команду:

1.  Откройте окно командной строки и перейдите в каталог проекта **креатепроцессверб** .
2.  Введите `msbuild CreateProcessVerb.sln`.

чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  откройте обозреватель Windows и перейдите в каталог проекта **креатепроцессверб** .
2.  Дважды щелкните значок файла Креатепроцессверб. sln, чтобы открыть проект в Visual Studio.
3.  В меню **Построение** выберите пункт **Построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  перейдите в каталог, содержащий новый исполняемый файл, используя командную строку или обозреватель Windows.
2.  В командной строке введите `CreateProcessVerb.exe` . кроме того, в обозревателе Windows дважды щелкните значок CreateProcessVerb.exe.
3.  Следуйте инструкциям в отображаемом диалоговом окне.

 

 



