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
ms.openlocfilehash: fe0ba5c86fdb2df5fe168559aa019941897563823e75670b0813ecb7e9e44d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820354"
---
# <a name="file-operation-progress-sink"></a>Приемник данных о ходе выполнения файловой операции

Демонстрирует использование методов интерфейса [**ифилеоператионпрогресссинк**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) для мониторинга сведений о действиях интерфейса [**интерфейс IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .

В этом разделе содержатся следующие подразделы.

-   [Требования](#requirements)
-   [Загрузка образца](#downloading-the-sample)
-   [Создание примера](#building-the-sample)
-   [Запуск примера](#running-the-sample)

## <a name="requirements"></a>Requirements (Требования)



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

чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  откройте обозреватель Windows и перейдите в каталог проекта **филесинусе** . Например, полный путь установки по умолчанию — `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .
2.  Дважды щелкните значок файла Филеоператионпрогресссинксампле. sln, чтобы открыть проект в Visual Studio.
    > [!Note]  
    > Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию. в этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".

     

3.  В меню **Построение** выберите пункт **Построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  перейдите в каталог, содержащий новый исполняемый файл, используя окно командной строки или проводник Windows.
2.  в командной строке введите `FileOperationProgressSinkSample.exe` или в Windows Explorer дважды щелкните значок FileOperationProgressSinkSample.exe.

 

 



