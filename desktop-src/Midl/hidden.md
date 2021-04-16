---
title: hidden - атрибут
description: Атрибут \ Hidden \ указывает, что элемент существует, но не должен отображаться в браузере, ориентированном на пользователей.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- скрытый атрибут MIDL
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650334"
---
# <a name="hidden-attribute"></a>hidden - атрибут

Атрибут **\[ Hidden \]** указывает, что элемент существует, но не должен отображаться в браузере, ориентированном на пользователей.

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*другие атрибуты* 
</dt> <dd>

Ноль или несколько необязательных атрибутов MIDL.

</dd> <dt>

*дерев* 
</dt> <dd>

Одна из следующих директив: [**компонент coclass**](coclass.md), [**DISP**](dispinterface.md), [**интерфейс**](interface.md)или [**Библиотека**](library.md).

</dd> <dt>

*имя элемента* 
</dt> <dd>

Имя, которое другие программные компоненты могут использовать для отделения текущего элемента.

</dd> <dt>

*вирус* 
</dt> <dd>

Указывает инструкции, которые составляют определение элемента.

</dd> <dt>

*тип функции* 
</dt> <dd>

Тип возвращаемого значения функции.

</dd> <dt>

*имя функции* 
</dt> <dd>

Имя, используемое для вызова функции.

</dd> <dt>

*список необязательных параметров* 
</dt> <dd>

Ноль или более параметров функции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Атрибут **\[ Hidden \]** позволяет удалять члены интерфейса (путем экранирования их из дальнейшего использования), сохраняя совместимость с существующим кодом. Атрибут **\[ Hidden \]** можно использовать для свойств, методов и операторов [**coclass**](coclass.md), [**DISP**](dispinterface.md), [**Interface**](interface.md)и [**Library**](library.md) .

При указании для библиотеки атрибут **\[ Hidden \]** предотвращает отображение всей библиотеки. Этот режим предназначен для использования с элементами управления. Узлы должны создать новую библиотеку типов, инкапсулирующую элемент управления с расширенными свойствами.

### <a name="flags"></a>Флаги

ВАРФЛАГ \_ фхидден, функфлаг \_ ФХИДДЕН, типефлаг \_ фхидден

## <a name="examples"></a>Примеры

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[**кокласс**](coclass.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[**библиотека**](library.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 