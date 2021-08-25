---
description: KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии диспетчера транзакций (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Маски доступа диспетчера транзакций (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfa093f38898ec49a789699fc5c7230612ef744fec78f200021361327d9f714
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913904"
---
# <a name="transaction-manager-access-masks"></a>Маски доступа диспетчера транзакций

KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии диспетчера транзакций (TM).

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**\_сведения о запросе диспетчером транзакций \_**
</dt> <dd> <dl> <dt>

Номера 0x00001
</dt> <dt>



Вызывающий объект может запросить сведения об этом TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**\_сведения о задании диспетчеров транзакций \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



Вызывающий объект может задать сведения об этом TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**Восстановление ДИСПЕТЧЕРом транзакций \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



Вызывающий объект может восстановить этот TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**Переименование диспетчер транзакций \_**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



Вызывающий объект может переименовать экземпляр TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**Диспетчер транзакций \_ создает \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



Вызывающий объект может создать диспетчер ресурсов, связанный с этим TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**\_транзакция привязки \_ транзакции транзакций**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Это значение зарезервировано.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**\_универсальное чтение с диспетчером транзакций \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



Вызывающий объект имеет следующие привилегии: **стандартные \_ права \_ Чтение** и **Диспетчер транзакций, \_ \_ сведения о запросах**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**\_Общая \_ запись в диспетчер транзакций**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



Вызывающий объект имеет следующие привилегии **: \_ стандартные \_ права записи**, диспетчер транзакций, **\_ \_ сведения о задании**, **\_ Восстановление**, диспетчер **транзакций \_** и **\_ Создание \_ RM**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**\_универсальное выполнение диспетчером транзакций \_**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



Вызывающий объект имеет следующие привилегии: **стандартные \_ права \_ выполнения**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**Диспетчер транзакций \_ все \_ доступ**
</dt> <dd> <dl> <dt>

0xF003F
</dt> <dt>



Это значение задает все допустимые биты для значения доступа TM.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Файл WinNT. h</dt> </dl> |



 

 




