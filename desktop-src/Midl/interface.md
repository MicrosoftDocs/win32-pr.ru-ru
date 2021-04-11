---
title: interface - атрибут
description: Ключевое слово interface указывает имя интерфейса. Имя интерфейса должно быть указано как в IDL-файле, так и в ACF.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- атрибут интерфейса MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890508"
---
# <a name="interface-attribute"></a>interface - атрибут

Ключевое слово **Interface** указывает имя интерфейса. Имя интерфейса должно быть указано как в IDL-файле, так и в ACF.

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Interface-список атрибутов* 
</dt> <dd>

Задает атрибуты, применяемые к интерфейсу в целом. Допустимыми атрибутами интерфейса для IDL-файла являются **\[** [**Конечная точка**](endpoint.md) **\]** , **\[** [**Локальная**](local.md) **\]** , **\[** [**объект**](object.md) **\]** , **\[** [**указатель \_ по умолчанию**](pointer-default.md) **\]** , **\[** [**UUID**](uuid.md) **\]** и **\[** [**версия**](version.md) **\]** . Допустимые атрибуты интерфейса для ACF включают **\[** [**кодирование**](encode.md) **\]** , **\[** [**декодирование**](decode.md) **\]** , **\[** [**автоматическую \_ обработку**](auto-handle.md) **\]** или **\[** [**неявный \_ маркер**](implicit-handle.md) **\]** , а также **\[** [**код**](code.md) **\]** или код **\[** [](nocode.md) **\]** .

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Указывает имя интерфейса. Имя интерфейса должно быть уникальным именем и должно начинаться с буквы или символа подчеркивания.

</dd> <dt>

*базовый интерфейс* 
</dt> <dd>

Указывает имя интерфейса, от которого этот производный интерфейс наследует функции члена, коды состояния и атрибуты интерфейса. Производный интерфейс не наследует определения типов. Для этого используйте ключевое слово [**Import**](import.md) , чтобы импортировать idl-файл базового интерфейса.

</dd> <dt>

*декларатор-список* 
</dt> <dd>

Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов. Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md). и [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers). *Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Имена интерфейсов в IDL-файле и ACF должны совпадать, за исключением случаев, когда используется параметр компилятора MIDL [**/АКФ**](-acf.md).

Имя интерфейса образует первую часть имени структур данных интерфейсного обработчика, которые являются параметрами функций времени выполнения RPC. Дополнительные сведения см. в разделе [**RPC \_ if \_ Handle**](/windows/desktop/Rpc/rpc-if-handle).

Если заголовок интерфейса содержит **\[** атрибут [**объекта**](object.md) **\]** , указывающий на COM-интерфейс, он должен также включать атрибут **\[** [**UUID**](uuid.md) **\]** и указывать базовый COM-интерфейс, от которого он является производным. Дополнительные сведения о COM-интерфейсах см. в разделе **\[** [**Object**](object.md) **\]** .

Можно также использовать ключевое слово **Interface** с ключевым словом [**typedef**](typedef.md) для определения типа данных интерфейса.

## <a name="examples"></a>Примеры

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации приложения (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Языковые**](local.md)
</dt> <dt>

[**объектами**](object.md)
</dt> <dt>

[**Указатель \_ по умолчанию**](pointer-default.md)
</dt> <dt>

[**RPC \_ if \_ Handle**](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[**определение**](typedef.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> <dt>

[**Версия**](version.md)
</dt> </dl>

 

 