---
title: propget - атрибут
description: Атрибут \ propget \ задает функцию доступа к свойству. Свойство должно иметь то же имя, что и функция.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- атрибут propget MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aaa55521042adc07f4242a44060e2442f087e609d0e3995d8c77457c8653c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383339"
---
# <a name="propget-attribute"></a>propget - атрибут

Атрибут **\[ propget \]** задает функцию доступа к свойству. Свойство должно иметь то же имя, что и функция.

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
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

Функция с атрибутом propget также должна иметь в качестве последнего параметра тип указателя с **\[** [](out-idl.md) **\]** атрибутами out и **\[** [**retval**](retval.md) **\]** . Если у последнего параметра нет \[ атрибутов out, \] то возвращаемое значение функции обрабатывается как \[ параметр out, retval \] . Например, функция с прототипом

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

рассматривается как

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

Для функции можно указать не более одного параметра **\[ propget \]**, **\[** [**propput**](propput.md) **\]** и **\[** [**propputref**](propputref.md) **\]** .

Если атрибут **\[** [**LCID**](lcid.md) **\]** используется в списке параметров функции, содержащей параметр с **\[** [](propput.md) **\]** атрибутом propput, то параметр **\[ LCID \]** должен находиться в секундах до последней.

### <a name="flags"></a>Флаги

ВЫЗВАТЬ \_ пропертижет

## <a name="examples"></a>Примеры

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**заполняет**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**типефлагс**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 