---
title: Идентификаторы доступа (Фвпму. h)
description: Платформа фильтрации Windows (WFP) использует стандартные права доступа Win32, а также набор специальных прав доступа для конкретных платформ, встроенных в платформу фильтрации.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989326"
---
# <a name="access-right-identifiers"></a>Идентификаторы прав доступа

Платформа фильтрации Windows (WFP) использует [стандартные права доступа Win32](/windows/desktop/SecAuthZ/standard-access-rights) , а также набор специальных прав доступа для конкретных платформ, встроенных в платформу фильтрации. Эти права доступа используются для защиты объектов только в пользовательском режиме. Вызывающие объекты режима ядра обходят все проверки доступа.

Идентификаторы прав доступа, специфические для WFP, приведены ниже.

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**\_Добавление фвпм актрл \_**
</dt> <dd> <dl> <dt>



Добавьте объект в модуль базовой фильтрации (BFE). Это право доступа требуется для вызова функций [**\* Add0 фвпм**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**ФВПМ \_ актрл \_ Добавить \_ ссылку**
</dt> <dd> <dl> <dt>



Добавьте объект, на который ссылается ссылка. Например, это право доступа требуется для вызовов, на которые ссылаются с помощью идентификаторов GUID.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**ФВПМ \_ актрл \_ Начало \_ чтения \_ транзакция**
</dt> <dd> <dl> <dt>



Начать транзакцию только для чтения. Это право доступа необходимо для вызова [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**ФВПМ \_ актрл \_ начать \_ запись \_ транзакция**
</dt> <dd> <dl> <dt>



Начать транзакцию для чтения и записи. Это право доступа необходимо для вызова [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) для транзакции чтения и записи.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_классификация фвпм актрл \_**
</dt> <dd> <dl> <dt>



Классификация удаленного вызова процедур (RPC). Это право доступа требуется во время выполнения RPC, чтобы применить фильтры RPC.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**\_перечисление АКТРЛ фвпм \_**
</dt> <dd> <dl> <dt>



Перечислить. Это право доступа требуется для вызова функций [**\* CreateEnumHandle0 фвпм**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) . Чтобы перечислить объект, вызывающему объекту также требуется ФВПМ \_ актрл \_ доступ для чтения к объекту.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**ФВПМ \_ актрл \_ Open**
</dt> <dd> <dl> <dt>



Откройте сеанс с обработчиком фильтров. Это право доступа необходимо для вызова [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**\_Чтение фвпм актрл \_**
</dt> <dd> <dl> <dt>



доступ для чтения; Это право доступа требуется для вызова функций [**фвпм \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) и [**фвпм \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_ \_ Статистика чтения фвпм \_ актрл**
</dt> <dd> <dl> <dt>



Чтение статистики. Это право доступа необходимо для вызова [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) и [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**\_Подписка фвпм актрл \_**
</dt> <dd> <dl> <dt>



Оформите подписку. Это право доступа требуется для вызова функций [**\* SubscribeChanges0 фвпм**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) . Чтобы получить уведомление для объекта, подписчику также требуется ФВПМ \_ актрл \_ доступ для чтения к объекту.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**ФВПМ \_ актрл \_ запись**
</dt> <dd> <dl> <dt>



Параметры модуля записи. Это право доступа необходимо для вызова [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**ФВПМ \_ универсальное \_ чтение**
</dt> <dd> <dl> <dt>



СТАНДАРТНЫЕ \_ права \_ Чтение \| фвпм \_ актрл \_ Начало \_ чтения \_ транзакция \| фвпм \_ актрл \_ классификация \| фвпм \_ актрл \_ Open \| фвпм \_ актрл \_ Read \| фвпм \_ актрл \_ Read \_ stats


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**ФВПМ \_ универсальное \_ выполнение**
</dt> <dd> <dl> <dt>



СТАНДАРТНЫЕ \_ права \_ выполнить \| фвпм \_ актрл \_ Enum \| фвпм \_ актрл \_ Subscribe


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**ФВПМ \_ Универсальная \_ запись**
</dt> <dd> <dl> <dt>



\_права на \_ запись \| Удаление \| фвпм \_ актрл \_ Добавить \| фвпм \_ актрл \_ Add \_ Link \| фвпм \_ актрл \_ Начало \_ записи \_ транзакция \| фвпм \_ актрл \_ Write


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**ФВПМ \_ Общие \_ все**
</dt> <dd> <dl> <dt>



для стандартных \_ прав \_ требуются \| фвпм \_ актрл \_ Add \| фвпм \_ актрл \_ Add \_ Link \| фвпм \_ актрл \_ Начало \_ чтения \_ транзакция \| фвпм \_ актрл \_ Begin \_ Write \_ транзакция \| фвпм \_ актрл \_ классифицировать \| фвпм \_ актрл \_ Enum \| фвпм \_ актрл \_ Open \| фвпм \_ актрл \_ Read \| фвпм \_ ACTRL \_ Read \_ stats \| FWPM \_ ACTRL \_ Subscribe \| FWPM \_ ACTRL \_ Write


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Фвпму. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Модель контроля доступа платформы фильтрации Windows](access-control.md)
</dt> <dt>

[Стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

