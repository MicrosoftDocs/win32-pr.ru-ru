---
title: propputref - атрибут
description: Атрибут \ propputref \ указывает функцию настройки свойства, которая использует ссылку вместо значения.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- атрибут propputref MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e80b0baa4f78537142043b374c206ade0f3d51d7ca30c2f57e1c4ae4e9b695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641967"
---
# <a name="propputref-attribute"></a>propputref - атрибут

Атрибут **\[ propputref \]** указывает функцию настройки свойства, которая использует ссылку вместо значения.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибуты необязательного свойства* 
</dt> <dd>

Ноль или более атрибутов свойств.

</dd> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Тип данных, возвращаемых удаленной процедурой.

</dd> <dt>

*имя функции* 
</dt> <dd>

Имя удаленной процедуры.

</dd> <dt>

*parameters* 
</dt> <dd>

Ноль или более параметров для удаленной процедуры.

</dd> </dl>

## <a name="remarks"></a>Remarks

Функция с атрибутом **\[ propputref \]** также должна иметь в качестве последнего параметра указатель, имеющий **\[** атрибут [**in**](in.md) **\]** .

Свойство должно иметь то же имя, что и функция. **\[** [](propget.md) **\]** Для функции можно указать только один из атрибутов propget, **\[** [**propput**](propput.md) **\]** и **\[ \] propputref** .

### <a name="flags"></a>Флаги

ВЫЗВАТЬ \_ пропертипутреф

## <a name="examples"></a>Примеры

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**окне**](in.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**типефлагс**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 