---
description: Демонстрирует использование методов интерфейса Ифилеоператионпрогресссинк для мониторинга сведений о действиях интерфейса интерфейс IFileOperation.
title: Приемник данных о ходе выполнения файловой операции
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080953"
---
# <a name="file-operation-progress-sink"></a>Приемник данных о ходе выполнения файловой операции

Демонстрирует использование методов интерфейса [**ифилеоператионпрогресссинк**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) для мониторинга сведений о действиях интерфейса [**интерфейс IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .

В этом разделе содержатся следующие подразделы.

-   [Требования](#requirements)
-   [Загрузка образца](#downloading-the-sample)
-   [Создание примера](#building-the-sample)
-   [Запуск примера](#running-the-sample)

## <a name="requirements"></a>Требования



| Продукт                                | Минимальная версия продукта |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows SDK | 6.1                     |



 

## <a name="downloading-the-sample"></a>Загрузка образца

| Расположение      | URL-адрес пути                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Пример Филеоператионпрогресссинк](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из окна командной строки:

1.  Откройте окно командной строки и перейдите в каталог проекта **филеоператионпрогресссинк** .
2.  Введите `msbuild FileOperationProgressSinkSample.sln`.

Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  Откройте проводник Windows и перейдите в каталог проекта **филесинусе** . Например, полный путь установки по умолчанию — `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .
2.  Дважды щелкните значок файла Филеоператионпрогресссинксампле. sln, чтобы открыть проект в Visual Studio.
    > [!Note]  
    > Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию. В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".

     

3.  В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.
2.  В командной строке введите `FileOperationProgressSinkSample.exe` или в проводнике Windows дважды щелкните значок FileOperationProgressSinkSample.exe.

 

 



