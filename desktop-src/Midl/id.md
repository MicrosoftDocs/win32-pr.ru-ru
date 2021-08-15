---
title: Атрибут идентификатора
description: Атрибут \ ID \ указывает идентификатор DISPID для функции-члена (свойства или метода в интерфейсе или DISP).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- атрибут ID MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4d783265ebfcf9dca454c80c39031dc0c37dfb63a8749b4d0e6299a510d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643070"
---
# <a name="id-attribute"></a>Атрибут идентификатора

Атрибут **\[ ID \]** задает DISPID для функции-члена (свойства или метода в интерфейсе или DISP).

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*ID-num* 
</dt> <dd>

DISPID для функции.

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Указывает список атрибутов интерфейса MIDL, отданных от нуля или более.

</dd> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Указывает тип возвращаемого значения функции.

</dd> <dt>

*имя функции* 
</dt> <dd>

Указывает имя функции в IDL-файле.

</dd> <dt>

*список необязательных параметров* 
</dt> <dd>

Ноль или более параметров функции.

</dd> </dl>

## <a name="remarks"></a>Remarks

Используйте атрибут **\[ ID \]** , если необходимо назначить стандартный идентификатор DISPID (например \_ , значение DISPID, DISPID \_ NEWENUM и т. д.) в метод или свойство или при реализации собственного **интерфейса IDispatch:: Invoke** вместо делегирования в **диспинвоке** / **ITypeInfo:: Invoke**.

Если атрибут **\[ ID \]** не используется в интерфейсе, компилятор MIDL присвоит вам идентификатор DISPID. Однако при указании disp-интерфейса с помощью свойств и методов необходимо указать DISPID для каждого свойства и метода.

*ID-num* — это 32-разрядное положительное целочисленное значение. Отрицательные идентификаторы зарезервированы для использования службой автоматизации.

## <a name="examples"></a>Примеры

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 