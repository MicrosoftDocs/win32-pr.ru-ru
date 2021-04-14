---
title: wire_marshal - атрибут
description: Атрибут \ проводное \_ маршалирование \ задает тип данных, который будет использоваться для передачи (тип связи) вместо типа данных, зависящего от приложения (усерм-Type).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal атрибута MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104413988"
---
# <a name="wire_marshal-attribute"></a>атрибут проводного \_ маршалирования

Атрибут **\[ проводного \_ маршалирования \]** задает тип данных, который будет использоваться для передачи ( *тип связи*) вместо типа данных, зависящего от приложения ( *усерм-Type*).

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Тип провода* 
</dt> <dd>

Указывает именованный тип данных передачи, который фактически передается между клиентом и сервером. *Тип связи* должен быть базовым типом MIDL, предопределенным типом или идентификатором типа, который может быть передан по сети.

</dd> <dt>

*Описатель типа* 
</dt> <dd>

Тип, для которого *усерм-Type* станет псевдонимом.

</dd> <dt>

*усерм — тип* 
</dt> <dd>

Указывает идентификатор пользовательского типа данных для маршалирования. Это может быть любой тип, заданный *описателем типа*, при условии, что он имеет четко определенный размер. *Тип усерм* не может быть передающим, но должен быть типом, известным компилятору MIDL.

</dd> <dt>

*пфлагс* 
</dt> <dd>

Задает указатель на поле флага [**(**](unsigned.md) [**длинное**](long.md)целое). Слово в высоком порядке определяет флаги представления данных NDR в соответствии с определением DCE для представления с плавающей запятой, с большим или прямым порядком байтов. Слово нижнего порядка задает флаг контекста маршалирования. Точный макет флагов описан в [ \_ функции Type усерсизе](/windows/desktop/Rpc/the-type-usersize-function).

</dd> <dt>

*стартингсизе* 
</dt> <dd>

Задает текущий размер буфера (смещение) перед изменением размера объекта.

</dd> <dt>

*Пусер \_ типеобжект* 
</dt> <dd>

Указывает указатель на объект *\_ типа усерм.*

</dd> <dt>

*Буфер* 
</dt> <dd>

Указывает текущий указатель буфера.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Каждый тип данных, относящийся к конкретному приложению, *усерм-Type,* имеет корреспонденцию "один к одному" с *типом связи* , который определяет сетевое представление типа. Необходимо предоставить подпрограммы для изменения размера данных для маршалирования, маршалирования и распаковки данных, а также для освобождения памяти. Обратите внимание, что при наличии в данных внедренных типов, которые также определены с помощью **\[ проводного \_ маршалирования \]** или **\[** [**пользовательского \_ маршалирования**](user-marshal.md) **\]** , необходимо также управлять обслуживанием этих внедренных типов. Дополнительные сведения об этих подоперациях см. [в описании атрибута Wired \_ Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute).

Реализация должна соответствовать правилам маршалинга в соответствии со спецификацией использование-DCE. Подробные сведения о синтаксисе перемещения NDR см. в статье [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) . Не рекомендуется использовать передачу по **\[ сети \_ \]** , если вы не знакомы с протоколом передачи по сети.

*Тип провода* не может быть указателем интерфейса или полным указателем. *Тип связи* должен иметь четко определенный объем памяти. Дополнительные сведения о том, как маршалировать данный *тип связи*, см. в разделе [правила упаковки для \_ \_ упаковки и](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) передачи данных.

*Усерм-Type* не должен быть указателем интерфейса, так как они могут быть упакованы напрямую. Если тип пользователя является полным указателем, необходимо самостоятельно управлять псевдонимами.

Нельзя использовать атрибут **\[ Wired \_ Marshal \]** с **\[** [](allocate.md) **\]** атрибутом allocate прямо или косвенно, так как модуль NDR не контролирует выделение памяти для переданного типа.

## <a name="examples"></a>Примеры

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[Представление данных](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**поддерживаем**](long.md)
</dt> <dt>

[**ндржетусермаршалинфо**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[Атрибут Wired \_ Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[**передать \_ как**](transmit-as.md)
</dt> <dt>

[**без знака**](unsigned.md)
</dt> <dt>

[**Пользовательская \_ Упаковка**](user-marshal.md)
</dt> </dl>

 

 