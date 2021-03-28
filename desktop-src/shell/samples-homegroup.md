---
description: Показывает, как определить состояние членства в домашней группе, перечислить элементы верхнего уровня в папке оболочки домашней группы и запустить мастер общего доступа к домашней группе.
title: Пример HomeGroup
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080952"
---
# <a name="homegroup-sample"></a>Пример HomeGroup

Показывает, как определить состояние членства в домашней группе, перечислить элементы верхнего уровня в папке оболочки **домашней группы** и запустить **мастер общего доступа к домашней группе**.

В этом разделе содержатся следующие подразделы.

-   [Требования](#requirements)
-   [Загрузка образца](#downloading-the-sample)
-   [Создание примера](#building-the-sample)
-   [Запуск примера](#running-the-sample)
-   [См. также](#related-topics)

## <a name="requirements"></a>Требования



| Продукт                                | Минимальная версия продукта |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Загрузка образца

| Расположение      | URL-адрес пути                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Пример домашней группы](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из командной строки, выполните следующую команду:

1.  Откройте окно командной строки и перейдите в каталог проекта **домашней группы** .
2.  Введите `msbuild HomeGroup.sln`.

Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  Откройте проводник Windows и перейдите к каталогу проекта **домашней группы** .
2.  Дважды щелкните значок файла Домашняя группа. sln, чтобы открыть проект в Visual Studio.
3.  В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.
2.  В командной строке введите `HomeGroup.exe` . Кроме того, в проводнике Windows дважды щелкните значок HomeGroup.exe.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**ихомеграуп**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[**кновнфолдерид**](knownfolderid.md)
</dt> </dl>

 

 



