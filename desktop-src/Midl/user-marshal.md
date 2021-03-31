---
title: атрибут user_marshal
description: '\_Атрибут ACF пользователя Marshal связывает именованный локальный тип на целевом языке (усерм-Type) с типом передачи (тип связи), который передается между клиентом и сервером.'
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal атрибута MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337025"
---
# <a name="user_marshal-attribute"></a>Пользовательский \_ атрибут маршалирования

Атрибут ACF **пользователя \_ Marshal** связывает именованный локальный тип на целевом языке (*усерм-Type*) с типом передачи (тип *связи*), который передается между клиентом и сервером.

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*усерм — тип* 
</dt> <dd>

Указывает идентификатор пользовательского типа данных для маршалирования. Тип усерм не должен быть *поддерживающим* передачу и не должен быть типом, известным компилятору MIDL.

</dd> <dt>

*Тип провода* 
</dt> <dd>

Указывает именованный тип данных передачи, который фактически передается между клиентом и сервером. Тип сети должен быть базовым типом MIDL, предопределенным типом или идентификатором типа, который может быть передан по сети.

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

Указывает указатель на объект *\_ типа усерм*.

</dd> <dt>

*Буфер* 
</dt> <dd>

Указывает текущий указатель буфера.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Каждый именованный локальный тип *усерм-Type* имеет корреспонденцию "один к одному" с *типом связи* "канал", который определяет прямое представление типа. Необходимо предоставить подпрограммы для изменения размера данных для маршалирования, маршалирования и распаковки данных, а также для освобождения памяти. Дополнительные сведения об этих подоперациях см. [в описании \_ атрибута User Marshal](/windows/desktop/Rpc/the-user-marshal-attribute). Обратите внимание, что при наличии в данных внедренных типов, которые также определены с помощью **\_ маршалирования пользователя** или \[ [**\[ проводного \_ маршалирования \]**](wire-marshal.md), необходимо также управлять обслуживанием этих внедренных типов.

*Тип провода* не может быть указателем интерфейса или полным указателем. *Тип связи* должен иметь четко определенный объем памяти. Дополнительные сведения о том, как маршалировать данный *тип связи*, см. в разделе [правила упаковки для \_ \_ упаковки и](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) передачи данных.

*Усерм-Type* не должен быть указателем интерфейса, так как они могут быть упакованы напрямую. Если тип пользователя является полным указателем, необходимо самостоятельно управлять псевдонимами.

## <a name="examples"></a>Примеры

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации приложения (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**поддерживаем**](long.md)
</dt> <dt>

[**представлять \_ как**](represent-as.md)
</dt> <dt>

[**без знака**](unsigned.md)
</dt> <dt>

[Атрибут пользовательской \_ маршалирования](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**проводное \_ маршалирование**](wire-marshal.md)
</dt> <dt>

[**ндржетусермаршалинфо**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 