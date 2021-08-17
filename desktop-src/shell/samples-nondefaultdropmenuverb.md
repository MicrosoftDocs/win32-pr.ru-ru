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
ms.openlocfilehash: 1c4623b9143e0a23762cfc44dd8dfc4f46b827a0f6433098d45d8a784ead81f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968793"
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
| Windows SDK | 7,0                     |



 

## <a name="downloading-the-sample"></a>Загрузка образца

| Расположение      | URL-адрес пути                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Пример Нондефаултдропменуверб](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из командной строки, выполните следующую команду:

1.  Откройте окно командной строки и перейдите в каталог проекта **нондефаултдропменуверб** .
2.  Введите `msbuild NonDefaultDropMenuVerb.sln`.

чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  откройте обозреватель Windows и перейдите в каталог проекта **нондефаултдропменуверб** .
2.  Дважды щелкните значок файла Нондефаултдропменуверб. sln, чтобы открыть проект в Visual Studio.
3.  В меню **Построение** выберите пункт **Построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  перейдите в каталог, содержащий новый файл DLL, с помощью командной строки или проводника Windows.
2.  скопируйте NonDefaultDropMenuVerb.dll в системный каталог (например, C: \\ Windows \\ System32).
3.  В командной строке введите `regedit NonDefaultDropMenuVerb.reg` .
4.  Используйте правую кнопку мыши, чтобы перетащить файл из одной папки в другую. Вы увидите дополнительные пункты меню для операции DROP.

 

 



