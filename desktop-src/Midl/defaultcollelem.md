---
title: defaultcollelem - атрибут
description: Атрибут \ дефаултколлелем \ помечает свойство как функцию доступа для элемента коллекции по умолчанию.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- атрибут дефаултколлелем MIDL
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069950"
---
# <a name="defaultcollelem-attribute"></a>defaultcollelem - атрибут

Атрибут **\[ дефаултколлелем \]** помечает свойство как функцию доступа для элемента коллекции по умолчанию.

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Property — список атрибутов* 
</dt> <dd>

Другие атрибуты, которые применяются к свойству.

</dd> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Указывает тип возвращаемого значения функции.

</dd> <dt>

*имя свойства* 
</dt> <dd>

Имя свойства.

</dd> <dt>

*Prop-param-List* 
</dt> <dd>

Список из нуля или более параметров, связанных со свойством.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Атрибут **\[ дефаултколлелем \]** используется для оптимизации кода Visual басикâ®. Если член интерфейса или DISP помечается как функция доступа, то вызов перейдет непосредственно к этому элементу.

Использование **\[ дефаултколлелем \]** должно соответствовать свойству. Например, если атрибут используется для свойства *Get* , он также должен присутствовать в свойстве *let* .

### <a name="typeflags-representation"></a>Представление типефлагс

Присутствие ФУНКФЛАГ \_ фдефаултколлелем или варфлаг \_ фдефаултколлелем.

## <a name="examples"></a>Примеры

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 