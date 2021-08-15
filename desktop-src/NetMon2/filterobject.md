---
description: Определяет один объект фильтра просмотра.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Структура ФИЛТЕРОБЖЕКТ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6a8da526eb60d8d581ca10e24f87a78b91492c4c043e6322eebe6a2ca0ebfd10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795787"
---
# <a name="filterobject-structure"></a>Структура ФИЛТЕРОБЖЕКТ

Структура **филтеробжект** определяет один объект фильтра просмотра. Функция [**филтераддобжект**](filteraddobject.md) использует **филтеробжект** для создания фильтра просмотра.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Действие**
</dt> <dd>

Флаг, указывающий действие **филтеробжект** . Флаг может указывать свойство, значение или оператор.

В следующей таблице перечислены флаги свойств члена действия.



| Значение                                                                                                                                                                                                | Значение                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <dt>**свойство действия фильтра \_**</dt> </dl>                | Содержит это свойство.<br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ пропертексист**</dt> </dl> | Указывает, что свойство действия фильтра уже определено.<br/> |



 

В следующей таблице перечислены флаги значений членов действий.



| Значение                                                                                                                                                                                        | Значение                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <dt>**значение действия фильтра \_**</dt> </dl>                 | Содержит это значение.<br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <dt>**Строка действия фильтра \_**</dt> </dl>              | Содержит эту строку.<br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <dt>**\_массив фильтра**</dt> </dl>                 | Содержит этот массив.<br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ контаинснк**</dt> </dl>  | Указывает, что свойство содержит подстроку без учета регистра.<br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ содержит**</dt> </dl>        | Указывает, что свойство содержит подстроку с учетом регистра.<br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <dt>**адрес действия фильтра \_**</dt> </dl>           | Содержит MAC-адрес.<br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ аддрессани**</dt> </dl>  | Соответствует любому MAC-адресу.<br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ из**</dt> </dl>                    | Указывает **MAC-** адрес.<br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ для**</dt> </dl>                          | Указывает **MAC-** адрес.<br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ фромто**</dt> </dl>              | Указывает на связывание MAC-адресов **от или к** .<br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ ларжеинт**</dt> </dl>        | Содержит большое целое число.<br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <dt>**время действия фильтра \_**</dt> </dl>                    | Содержит структуру **SYSTEMTIME** .<br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <dt>**\_ETHER адрес действия фильтра \_**</dt> </dl> | Содержит MAC-адрес Ethernet.<br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <dt>**\_маркер адреса в действии фильтра \_**</dt> </dl> | Содержит MAC-адрес Token Ring.<br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <dt>**адрес действия фильтра \_ \_ FDDI**</dt> </dl>    | Содержит MAC-адрес FDDI.<br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <dt>**адрес действия фильтра ( \_ \_ IPX)**</dt> </dl>       | Содержит MAC-адрес IPX.<br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <dt>**\_ \_ IP-адрес получателя фильтра**</dt> </dl>          | Содержит IP-адрес MAC.<br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <dt>**\_идентификатор объекта действия фильтра**</dt> </dl>                       | Содержит идентификатор объекта (OID).<br/>                             |



 

В следующей таблице перечислены флаги операторов члена действия.



| Значение                                                                                                                                                                                                        | Значение                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <dt>**\_недопустимое действие фильтра**</dt> </dl>                           | Указывает на недопустимое действие фильтра.<br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ и**</dt> </dl>                                       | Указывает логическую инструкцию **и** .<br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ или**</dt> </dl>                                          | Указывает на логический оператор **или** .<br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ XOR**</dt> </dl>                                       | Указывает на логическую исключающую инструкцию **или** (XOR).<br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ не**</dt> </dl>                                       | Указывает на логическую инструкцию **Not** .<br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ екуалнк**</dt> </dl>                           | Действие фильтра равно и не учитывает регистр.<br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ равно**</dt> </dl>                                 | Действие фильтра равно и учитывает регистр.<br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ нотекуалнк**</dt> </dl>                  | Оператор логического **не** равен и не учитывает регистр.<br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ NOTEQUAL**</dt> </dl>                        | Оператор логического **не** равен и учитывает регистр.<br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ греатернк**</dt> </dl>                     | Действие фильтра больше (>) и не учитывает регистр.<br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ выше**</dt> </dl>                           | Действие фильтра больше (>) и с учетом регистра.<br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ лесснк**</dt> </dl>                              | Действие фильтра меньше (<) и не учитывает регистр.<br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ меньше**</dt> </dl>                                    | Действие фильтра меньше (<) и с учетом регистра.<br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ греатерекуалнк**</dt> </dl>      | Действие фильтра больше или равно (>=) и не учитывает регистр.<br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ загруженность**</dt> </dl>            | Действие фильтра больше или равно (>=) и с учетом регистра.<br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ лессекуалнк**</dt> </dl>               | Действие фильтра меньше или равно (<=) и не учитывает регистр.<br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ лессекуал**</dt> </dl>                     | Действие фильтра меньше или равно (<=) и учитывает регистр.<br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ плюс**</dt> </dl>                                    | Добавить оператор (+).<br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ минус**</dt> </dl>                                 | Оператор вычитания (-).<br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ аребитсон**</dt> </dl>                     | Указывает побитовую операцию.<br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ аребитсофф**</dt> </dl>                  | Указывает на побитовую операцию.<br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ протоколсексист**</dt> </dl>      | Указывает, что выбранные протоколы существуют.<br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ протоколексист**</dt> </dl>         | Указывает, что выбранный протокол существует.<br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ аррайекуал**</dt> </dl>                  | Указывает, что содержимое массива равно. Флаг должен использоваться с структурой **\_ массива фильтра** .<br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <dt>**ДЕЙСТВИЕ фильтра \_ дерефпроперти**</dt> </dl>         | Описывает соответствие шаблона по смещению (в байтах) от протокола.<br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <dt>**\_идентификатор объекта действия фильтра \_**</dt> </dl>           | Вычисляет подстроку в пределах идентификатора объекта. Действие должно использоваться с структурой **\_ OID объекта фильтра** .<br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <dt>**Идентификатор объекта действия фильтра ( \_ OID) \_ начинается \_ с**</dt> </dl> | Вычисляет подстроку, которая начинает идентификатор объекта. Флаг должен использоваться с **\_ идентификатором объекта действия фильтра**.<br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <dt>**\_идентификатор объекта действия фильтра \_ заканчивается \_ на**</dt> </dl>       | Вычисляет подстроку, которая завершает идентификатор объекта. Флаг должен использоваться с **\_ идентификатором объекта действия фильтра**.<br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <dt>**\_приемники \_ фильтра**</dt> </dl>                 | Содержит MAC-адрес Vines.<br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <dt>**выражение действия фильтра \_**</dt> </dl>                  | Содержит выражение действия.<br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <dt>**Логическое значение действия фильтра \_**</dt> </dl>                                    | Содержит тип данных **bool** .<br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <dt>**\_направление фильтра \_ Далее**</dt> </dl>                       | Управляет последовательным направлением (следующий кадр) в файле записи.<br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <dt>**\_ \_ предыдущее направление фильтра**</dt> </dl>                       | Управляет последовательным направлением (предыдущий кадр) в файле записи.<br/>                                                |



 

</dd> <dt>

**хпроперти**
</dt> <dd>

Обработчик для ключа свойства.

</dd> <dt>

**Значение**
</dt> <dd>

Значение объекта.

</dd> <dt>

**хпротокол**
</dt> <dd>

Маркер для протокола фильтра просмотра.

</dd> <dt>

**lpArray**
</dt> <dd>

Указатель на массив.

</dd> <dt>

**лппротоколтабле**
</dt> <dd>

Указатель на список протоколов, предназначенный для проверки существования протокола в кадре.

</dd> <dt>

**лпаддресс**
</dt> <dd>

Указатель на адрес типа ядра. Например, MAC или IP.

</dd> <dt>

**лпларжеинт**
</dt> <dd>

двойное **слово DWORD** используется в приложении Windows NT или Windows 2000.

</dd> <dt>

**лптиме**
</dt> <dd>

Указатель на структуру **SYSTEMTIME** .

</dd> <dt>

**лпоид**
</dt> <dd>

Указатель на структуру **\_ идентификатора объекта** (OID).

</dd> <dt>

**ByteCount**
</dt> <dd>

Число в байтах в кадре.

</dd> <dt>

**ByteOffset**
</dt> <dd>

Значение байта смещения структуры ФИЛТЕРОБЖЕКТ, используемое для сравнения массивов.

</dd> <dt>

**пнекст**
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




