---
title: настраиваемый атрибут
description: Атрибут \ Custom \ создает определяемый пользователем атрибут.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- пользовательский атрибут MIDL
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace6a558da428da07a432653391e0e48b7a5545bb1a83eb40d9c950abfa9d9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643673"
---
# <a name="custom-attribute"></a>настраиваемый атрибут

**\[ Настраиваемый \]** атрибут создает определяемый пользователем атрибут.

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Attribute-ID* 
</dt> <dd>

Идентификатор GUID для настраиваемого атрибута.

</dd> <dt>

*атрибут-значение* 
</dt> <dd>

Значение, которое содержит атрибут. Значение должно быть значением, которое может быть помещается в тип VARIANT.

</dd> <dt>

*Список атрибутов* 
</dt> <dd>

Другие атрибуты, такие как **\[** [**UUID**](uuid.md) **\]** и **\[** [**helpString**](helpstring.md) **\]** , которые применяются к этому элементу.

</dd> <dt>

*Element-Type* 
</dt> <dd>

Тип элемента, к которому применяется настраиваемый атрибут. Это может быть оператор библиотеки, сведения о типе, переменная, функция или параметр. Нельзя использовать настраиваемый атрибут для члена класса coclass.

</dd> <dt>

*имя элемента* 
</dt> <dd>

Имя элемента.

</dd> </dl>

## <a name="remarks"></a>Remarks

Используйте **\[ настраиваемый \]** атрибут для определения собственного атрибута. Например, можно создать атрибут с строковыми значениями, который предоставляет идентификатор ProgID для класса.

Чтобы получить значение настраиваемого атрибута, вызовите один из следующих элементов:

-   ITypeLib2:: Жеткустдата (ргуид, Пварвал)
-   ITypeInfo2:: Жеткустдата (ргуид, Пварвал)
-   ITypeInfo2:: Жетфунккустдата (index, ргуид, Пварвал)
-   ITypeInfo2:: Жетваркустдата (index, ргуид, пварвал)
-   ITypeInfo2:: Жетпарамкустдата (Индексфунк, Индекспарам, ргуид, Пварвал)

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Библиотечная**](library.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 