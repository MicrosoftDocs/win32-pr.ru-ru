---
title: Образец макета сетки
description: демонстрирует использование Windows анимации с помощью Direct2D для анимации сетки изображений.
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf287dc7d6f96b9b5db4ce3fff7d30c34b1f8b998518dbdddc9d7abbda793330
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999684"
---
# <a name="grid-layout-sample"></a>Образец макета сетки

демонстрирует использование Windows анимации с помощью Direct2D для анимации сетки изображений.

## <a name="downloading-the-sample"></a>Загрузка образца

Этот образец доступен в следующих расположениях.



| Расположение                               | Путь или URL-адрес                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows SDK | [пакет средств разработки Microsoft Windows Software Development Kit 7,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Коллекция кодов                           | [Windows Пример кода для диспетчера анимации](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

после загрузки и установки Windows SDK вы найдете образцы в каталоге установки. например, если вы используете путь установки по умолчанию для Windows SDK для Windows 7, образцы устанавливаются в C: \\ Program files \\ Microsoft sdks \\ Windows \\ v 7.0 \\ samples.

## <a name="building-the-sample"></a>Построение образца

Для построения образца используйте один из следующих методов.

**Построение примера в командной строке**

1.  Откройте окно командной строки и перейдите в каталог проекта GridLayout. например, путь установки по умолчанию для этого образца — C: \\ Program files \\ Microsoft sdks \\ Windows \\ v 7.0 \\ samples \\ мультимедиа \\ виндовсаниматион \\ GridLayout

2.  Выполните следующую команду: **MSBuild GridLayout. sln**

**построение примера с помощью Microsoft Visual Studio (предпочтительно)**

1.  откройте обозреватель Windows и перейдите к каталогу проекта GridLayout.

    > [!Note]  
    > Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию. в этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".

     

2.  Дважды щелкните значок файла GridLayout. sln, чтобы открыть проект в Visual Studio.

3.  В меню **Построение** выберите пункт **Построить решение**.

## <a name="running-the-sample"></a>Запуск примера

Для выполнения образца:

1.  перейдите в каталог, содержащий новый исполняемый файл, используя командную строку или проводник Windows.

2.  запустите **GridLayout.exe** из командной строки или дважды щелкните значок для GridLayout.exe в обозревателе Windows.

3.  Образцы изображений загружаются из библиотеки рисунков. Измените размер окна, и изображения будут размещаться в сетке.

 

 




