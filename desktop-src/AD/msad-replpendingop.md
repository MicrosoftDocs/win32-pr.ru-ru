---
title: Класс MSAD_ReplPendingOp
description: Представляет \_ \_ структуру Op REPL DS, которая описывает задачу репликации, которая выполняется в данный момент или ожидает выполнения.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- Класс MSAD_ReplPendingOp Active Directory
- Active Directory класса MSAD_ReplPendingOp, описание
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164c5ebe672a52bb399727940e5e51b98904f7db322cc362425dabda25f547a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186079"
---
# <a name="msad_replpendingop-class"></a>\_Класс МСАД реплпендингоп

Представляет структуру [**\_ \_ Op REPL DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , которая описывает задачу репликации, которая выполняется в данный момент или ожидает выполнения. Эта структура возвращается функцией [**дсрепликажетинфо**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a>Члены

Класс **МСАД \_ реплпендингоп** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **МСАД \_ реплпендингоп** имеет следующие свойства.

<dl> <dt>

**дсааддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает сетевой адрес удаленного сервера, связанного с этой операцией. **Значение NULL** , если отсутствует удаленный сервер, связанный с этой операцией.

</dd> <dt>

**дсадн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает путь к DSA X. 500, связанному с удаленным сервером, который соответствует этой операции. **Значение NULL** , если ни один удаленный сервер не соответствует этой операции.

</dd> <dt>

**дсаобжгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение атрибута [**OBJECTGUID**](/windows/desktop/ADSchema/a-objectguid) DSA, идентифицируемого свойством **дсадн** .

</dd> <dt>

**намингконтекстдн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает путь X. 500 контекста именования (NC), связанного с данной операцией.

</dd> <dt>

**намингконтекстобжгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает атрибут [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) сетевого контекста, идентифицируемого свойством **намингконтекстдн** .

</dd> <dt>

**опстарттиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает время начала операции. **Значение NULL** , если эта операция все еще находится в очереди.

</dd> <dt>

**Параметры**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает набор флагов, которые предоставляют дополнительные данные об операции. Содержимое этого элемента определяется значением свойства **OpType** .

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_ \_ \_ Синхронизация типа операции DS \_ REPL**


</dt> <dd>

Содержит ноль или сочетание одного или нескольких значений **DS \_ \_ \* репсинк* _, как определено для параметра _Options * в [**дсрепликасинк**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**\_ \_ \_ Добавление типа Op в DS REPL \_**


</dt> <dd>

Содержит ноль или комбинацию одного или нескольких значений **DS \_ \_ \* repadd*, определенных для параметра _Options * в [**дсрепликаадд**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**\_ \_ операция \_ \_ удаления типа операции DS REPL**


</dt> <dd>

Содержит ноль или сочетание одного или нескольких значений **DS \_ \_ \* репдел* _, как определено для параметра _Options * в [**дсрепликадел**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS \_ REPL \_ , \_ изменение типа Op \_**


</dt> <dd>

Содержит ноль или сочетание одного или нескольких значений **DS \_ \_ \* репмод* _, как определено для параметра _Options * в [**дсрепликамодифи**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_ссылки для \_ \_ обновления типа \_ \_ операций DS REPL**


</dt> <dd>

Содержит ноль или сочетание одного или нескольких значений **DS \_ \_ \* репсупд* _, как определено для параметра _Options * в [**дсрепликаупдатерефс**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение [**\_ \_ \_ типа Op REPL**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) , которое указывает тип операции, представляемой этим классом.

</dd> <dt>

**поситионинк**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает расположение этой операции в очереди.

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает приоритет этой операции. Задачи с более высоким приоритетом выполняются первыми. Приоритет вычисляется сервером в зависимости от типа операции, представляемой этим классом, и параметров операции.

</dd> <dt>

**Номер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает идентификатор операции, уникальный для каждого компьютера и для каждой загрузки.

</dd> <dt>

**тиминкуеуед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает время, когда эта операция была добавлена в очередь.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ микрософтактиведиректори<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

