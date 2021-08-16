---
title: атрибут module
description: Оператор Module определяет группу функций, обычно набор точек входа DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- атрибут модуля MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a83528a1ec632fcf2309438e6228220544a32408b310ea90260b8bcfda3cb6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642812"
---
# <a name="module-attribute"></a>атрибут module

Оператор **module** определяет группу функций, обычно набор точек входа DLL.

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*attributes* 
</dt> <dd>

Атрибуты \[ [**UUID**](uuid.md) \] , \[ [**Version**](version.md) \] , \[ [**helpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] и \[ [**dllname**](dllname-str-.md) \] принимаются перед оператором **module** . Дополнительные сведения об атрибутах, принятых перед определением модуля, см. в [описании атрибутов](/previous-versions/windows/desktop/automat/attribute-descriptions)в книге OLE-автоматизации. Атрибут \[ **dllname** \] является обязательным. Если атрибут \[ **UUID** \] опущен, модуль не указывается уникальным образом в системе.

</dd> <dt>

*ModuleName* 
</dt> <dd>

Имя модуля.

</dd> <dt>

*елементлист* 
</dt> <dd>

Список константных определений и прототипов функций для каждой функции в библиотеке DLL. В списке функций может присутствовать любое количество определений функций. Функция в списке функций имеет следующий вид:

\[*атрибуты* \] *ReturnType* \[ *соглашение о вызовах funcname* \] (*params*);

\[*атрибуты* \] [**const**](const.md) константтипе *констнаме*  =  *конствал*;

Только атрибуты \[ [**helpString**](helpstring.md) \] и \[ [**HelpContext**](helpcontext.md) \] принимаются для [**const**](const.md).

Следующие атрибуты принимаются для функции в модуле: \[ [**helpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**propput**](propput.md) \] , \[ [**propputref**](propputref.md) \] и \[ [**vararg**](vararg.md) \] . Если \[  \] указано vararg, последний параметр должен быть надежным массивом типа **Variant** .

Необязательное соглашение о вызовах может быть одним из \_ \_ : Pascal/ \_ Pascal/Pascal, \_ \_ cdecl/ \_ cdecl/cdecl или \_ \_ STDCALL/ \_ STDCALL/STDCALL. *Тип соглашения о вызове paramName* может включать до двух подчеркивания в начале.

Список параметров представляет собой разделенный запятыми список:

\[*атрибута*\]

Тип может быть любым ранее объявленным типом или встроенным типом, указателем на любой тип или указателем на встроенный тип. Атрибуты в параметрах:

\[[**в**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**необязательно**](optional.md) \] .

Если \[ используется [**необязательный**](optional.md) параметр \] , типы этих параметров должны быть **Variant** или **Variant** \* .

</dd> </dl>

## <a name="remarks"></a>Remarks

Выходные данные файла заголовка (h) для модулей — это последовательность прототипов функций. Ключевое слово **module** и окружающие квадратные скобки удаляются из выходных данных файла заголовка (. h), но перед прототипами вставляется комментарий (// *ModuleName* **модуля** ). Ключевое слово **extern** вставляется перед объявлениями.

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Содержимое библиотеки типов](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**dllname**](dllname-str-.md)
</dt> <dt>

[**операции**](entry.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**служеб**](hidden.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**Строка**](string.md)
</dt> <dt>

[**типефлагс**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Версия**](version.md)
</dt> </dl>

 

 