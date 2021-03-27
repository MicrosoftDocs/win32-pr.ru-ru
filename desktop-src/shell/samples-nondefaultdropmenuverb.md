---
description: Демонстрирует расширение контекстного меню перетаскивания (иногда называемое контекстным меню).
title: Пример NonDefaultDropMenuVerb
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347932"
---
# <a name="nondefaultdropmenuverb-sample"></a>Пример NonDefaultDropMenuVerb

Демонстрирует расширение контекстного меню перетаскивания (иногда называемое контекстным меню).

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
| GitHub  | [Пример Нондефаултдропменуверб](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из командной строки, выполните следующую команду:

1.  Откройте окно командной строки и перейдите в каталог проекта **нондефаултдропменуверб** .
2.  Введите `msbuild NonDefaultDropMenuVerb.sln`.

Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  Откройте проводник Windows и перейдите в каталог проекта **нондефаултдропменуверб** .
2.  Дважды щелкните значок файла Нондефаултдропменуверб. sln, чтобы открыть проект в Visual Studio.
3.  В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  Перейдите в каталог, содержащий новый файл DLL, с помощью командной строки или проводника Windows.
2.  Скопируйте NonDefaultDropMenuVerb.dll в системный каталог (например, C: \\ Windows \\ System32).
3.  В командной строке введите `regedit NonDefaultDropMenuVerb.reg` .
4.  Используйте правую кнопку мыши, чтобы перетащить файл из одной папки в другую. Вы увидите дополнительные пункты меню для операции DROP.

 

 



