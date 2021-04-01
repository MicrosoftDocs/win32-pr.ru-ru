---
title: dispinterface - атрибут
description: Оператор DISP определяет набор свойств и методов, для которых можно вызвать вызов IDispatch.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- интерфейс MIDL с атрибутом DISP
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890617"
---
# <a name="dispinterface-attribute"></a>dispinterface - атрибут

Оператор **DISP** определяет набор свойств и методов, для которых можно вызвать **IDispatch:: Invoke**. Диспетчерский интерфейс может быть определен путем явного перечисления набора поддерживаемых методов и свойств (синтаксис 1) или путем перечисления одного интерфейса (синтаксис 2).

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*attributes* 
</dt> <dd>

Задает атрибуты, которые применяются ко всему **интерфейсу**. Принимаются следующие атрибуты: **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**unextensible**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** и **\[** [**Version**](version.md) **\]** .

</dd> <dt>

*имя disp-интерфейса* 
</dt> <dd>

Имя, по которому **диспетчерский интерфейс** известен в библиотеке типов. Это имя должно быть уникальным в пределах библиотеки типов.

</dd> <dt>

*список свойств* 
</dt> <dd>

(Синтаксис 1) Необязательный список свойств, поддерживаемых объектом, объявленный в виде переменных. Это краткая форма для объявления функций свойств в списке методов. Дополнительные сведения см. в разделе комментариев.

</dd> <dt>

*список методов* 
</dt> <dd>

(Синтаксис 1) Список, состоящий из прототипа функции для каждого метода и свойства в **DISP-интерфейсе**. В *меслист* может использоваться любое количество определений функций. Функция в *меслист* имеет следующую форму:

**\[  атрибуты \]** *ReturnType меснаме Type paramName ***(*** params * * *);**

Следующие атрибуты принимаются для метода в **DISP-интерфейсе**: **\[ helpString \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** , **\[** [**propputref**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** и **\[** [**vararg**](vararg.md) **\]** . Если указано **\[ \] vararg** , последний параметр должен быть надежным массивом типа **Variant** .

Список параметров представляет собой список с разделителями-запятыми, каждый элемент которого имеет следующую форму:

**\[***атрибута***\]**

*Тип* может быть любым объявленным или встроенным типом или указателем на любой тип. Атрибуты в параметрах:

**\[**[**в**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**необязательный**](optional.md) **\]** , **\[ строка \]**

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

(Синтаксис 2) Имя интерфейса, объявляемого как интерфейс IDispatch.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Компилятор MIDL принимает следующий порядок параметров (слева направо):

1.  Обязательные параметры (параметры, у которых нет \[ DefaultValue \] или \[ необязательных \] атрибутов);
2.  необязательные параметры с \[ атрибутом DefaultValue или без него \]
3.  параметры с \[ необязательным \] атрибутом и без \[ \] атрибута DefaultValue,
4.  \[параметр [**LCID**](lcid.md) \] , если он есть,
5.  \[[**retval**](retval.md) \] параметр

Функции методов задаются точно так же, как описано на странице Справочник по [**модулю**](module.md) , за исключением того, что \[ атрибут [**entry**](entry.md) \] не разрешен. Обратите внимание, что STDOLE32. TLB (СТДОЛЕ. TLB в 16-разрядных системах) необходимо импортировать, так как **диспетчерский интерфейс** наследует от IDispatch.

Свойства можно объявлять в списках свойств или методов. Объявление свойств в списке свойств не указывает тип доступа, который поддерживает свойство (т. е. Get, WHERE или путреф). Укажите атрибут \[ [**ReadOnly**](readonly.md) \] для свойств, которые не поддерживают размещение или путреф. При объявлении функций свойств в списке методов функции для одного свойства имеют одинаковый идентификатор.

При использовании первого синтаксиса требуются Теги Properties: и. Атрибут \[ [**ID**](id.md) \] также требуется для каждого элемента. Пример:

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

В отличие от членов интерфейса, члены disp-интерфейсов не могут использовать атрибут [**retval**](retval.md) для возврата значения в дополнение к коду ошибки HRESULT. Атрибут \[ [**LCID**](lcid.md) \] также является недопустимым для disp-интерфейсов, так как IDispatch:: Invoke передает код языка. Однако можно повторно объявить интерфейс, использующий эти атрибуты.

С помощью второго синтаксиса интерфейсы, поддерживающие IDispatch и объявленные ранее в скрипте ODL, могут быть повторно объявлены как интерфейсы IDispatch следующим образом:

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

В предыдущем примере объявляются все члены Hello и все члены, которые Привет наследуют как поддерживающие IDispatch. В этом случае, если аргумент Hello был объявлен ранее \[ с \] элементами LCID и \[ retval \] , которые возвращали HRESULTS, MkTypLib будет удалять каждый \[ \] параметр LCID и тип возвращаемого значения HRESULT, а вместо этого помечать возвращаемый тип как \[ \] параметр retval.

> [!Note]  
> Средство Mktyplib.exe устарело. Вместо этого используйте компилятор MIDL.

 

Свойства и методы disp-интерфейса не являются частью таблицы VTBL. Следовательно, [креатестддиспатч](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) и [диспинвоке](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) нельзя использовать для реализации IDispatch:: Invoke. Диспетчерский интерфейс используется, когда приложению необходимо предоставить доступ к существующим функциям, не относящимся к VTBL, с помощью службы автоматизации. Эти приложения могут реализовать IDispatch:: Invoke путем проверки параметра Диспидмембер и непосредственного вызова соответствующей функции.

## <a name="examples"></a>Примеры

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**служеб**](hidden.md)
</dt> <dt>

[**окне**](in.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**используемых**](optional.md)
</dt> <dt>

[**заполняет**](out-idl.md)
</dt> <dt>

[**nonextensible**](nonextensible.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**зона**](restricted.md)
</dt> <dt>

[**Строка**](string.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Версия**](version.md)
</dt> </dl>

 

 