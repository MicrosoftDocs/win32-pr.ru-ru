---
title: propput - атрибут
description: Атрибут \ propput \ задает функцию настройки свойства. Свойство должно иметь то же имя, что и функция.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- атрибут propput MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133735"
---
# <a name="propput-attribute"></a>propput - атрибут

Атрибут **\[ propput \]** указывает функцию настройки свойства. Свойство должно иметь то же имя, что и функция *.*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
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

## <a name="remarks"></a>Комментарии

Функция, имеющая атрибут **\[ propput \]** , должна также иметь в качестве последнего параметра параметр с **\[** [](in.md) **\]** атрибутом in.

**\[** [](propget.md) **\]** Для функции можно указать не более одного параметра propget, **\[ propput \]** и **\[** [**propputref**](propputref.md) **\]** .

Если атрибут **\[** [**LCID**](lcid.md) **\]** используется в списке параметров функции, содержащей параметр с атрибутом **\[ propput \]** , то параметр **\[ LCID \]** должен находиться в секундах до последней.

### <a name="flags"></a>Флаги

ВЫЗВАТЬ \_ пропертипут

## <a name="examples"></a>Примеры

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Различия между MIDL и MKTYPLIB](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**типефлагс**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 