---
title: Связывание значков с категорией
description: Связывание значков с категорией
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62af14480d24053ffc517d405635ecbe4d6e45c8edac256039ea008160f11063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793834"
---
# <a name="associating-icons-with-a-category"></a>Связывание значков с категорией

Создание пользовательского интерфейса, позволяющего пользователю выбирать категории компонентов в категории, требует возможность отображать осмысленное изображение для определенной категории. Чтобы связать значок с категорией компонента, создайте ключ для идентификатора CATID категории и заполните этот ключ подразделом [дефаултикон](defaulticon.md) . Запись реестра выглядит следующим образом:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

Имя файла, на которое ссылается ключ Дефаултикон, может быть файлом EXE или DLL (библиотека DLL только для ресурсов).

Чтобы связать маленький значок панели элементов с категорией компонента, создайте ключ в **\_ \_ корневом \\ идентификаторе CLSID классов hKey** для идентификатора CATID категории и заполните этот ключ подключом [ToolBoxBitmap32](toolboxbitmap32.md) , как показано в следующем примере:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

Имя файла, на которое ссылается ключ [ToolBoxBitmap32](toolboxbitmap32.md) , также может быть файлом EXE или DLL (библиотека DLL только для ресурсов).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Категоризация по возможностям компонентов](categorizing-by-component-capabilities.md)
</dt> <dt>

[Категоризация по возможностям контейнеров](categorizing-by-container-capabilities.md)
</dt> <dt>

[Классы и ассоциации по умолчанию](default-classes-and-associations.md)
</dt> <dt>

[Определение категорий компонентов](defining-component-categories.md)
</dt> <dt>

[**икатинформатион**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[**икатрегистер**](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[Диспетчер категорий компонентов](the-component-categories-manager.md)
</dt> </dl>

 

 




