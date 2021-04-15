---
title: importlib - атрибут
description: Директива \ importlib \ делает типы, которые уже были скомпилированы в другую библиотеку типов, доступными для создаваемой библиотеки типов.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- атрибут importlib MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487545"
---
# <a name="importlib-attribute"></a>importlib - атрибут

Директива **\[ importlib \]** делает типы, которые уже были скомпилированы в другую библиотеку типов, доступными для создаваемой библиотеки типов.

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибуты библиотеки* 
</dt> <dd>

Ноль или более атрибутов, которые будут применены к библиотеке.

</dd> <dt>

*имя библиотеки* 
</dt> <dd>

Идентификатор, который программные компоненты будут использовать для обозначения этой [**библиотеки**](library.md).

</dd> <dt>

*файл для импорта* 
</dt> <dd>

Имя и расположение импортируемого файла во время компиляции MIDL.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Все директивы **\[ importlib \]** должны предшествовать описаниям других типов в библиотеке. Обратите внимание, что Импортированная библиотека, а также созданная библиотека, должна быть распространена вместе с приложением, чтобы она была доступна во время выполнения.

В большинстве случаев директиву импорта MIDL следует использовать **\[** [](import.md) **\]** для ссылки на определения из другого. IDL-файл в. IDL-файл. Этот метод предоставляет библиотеке типов все данные из исходного файла, тогда как **\[ importlib \]** помещает только содержимое библиотеки типов.

> [!Note]  
> Директива **\[ importlib \]** делает любой тип, определенный в импортируемой библиотеке, доступным в компилируемой библиотеке. Чтобы избежать неоднозначности при наличии повторяющихся ссылок, рекомендуется определить каждую из этих ссылок с использованием соответствующего имени библиотеки, как показано ниже.

 

``` syntax
library_name.type
```

В отсутствие такой квалификации MIDL разрешает неоднозначность повторяющейся ссылки следующим образом:

-   Начиная с версии 3,1, MIDL использует первую найденную ссылку.
-   Версия 3,0 MIDL, первая версия MIDL, способная формировать библиотеки типов, использует последнюю найденную ссылку.

## <a name="examples"></a>Примеры

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**библиотека**](library.md)
</dt> <dt>

[**импортиру**](import.md)
</dt> <dt>

[Импорт системных файлов заголовков](importing-system-header-files.md)
</dt> <dt>

[Импорт файлов и библиотек типов](importing-files-and-type-libraries.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 