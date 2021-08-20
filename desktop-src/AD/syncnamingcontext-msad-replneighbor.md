---
title: Метод Синкнамингконтекст класса MSAD_ReplNeighbor
description: Вызывает функцию Дсрепликасинк, которая синхронизирует целевой контекст именования с одним из его источников.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Active Directory метода Синкнамингконтекст
- Active Directory метода Синкнамингконтекст, класс MSAD_ReplNeighbor
- Класс MSAD_ReplNeighbor Active Directory, метод Синкнамингконтекст
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b96dd7363b5c2a48a6c25826d8c2752c181bc9125955b6c73d5532eb2665514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024672"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>Метод Синкнамингконтекст \_ класса РЕПЛНЕИГХБОР МСАД

Вызывает функцию [**дсрепликасинк**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) , которая синхронизирует целевой контекст именования с одним из его источников.

## <a name="syntax"></a>Синтаксис


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Дополнительные данные, определяющие способ обработки запроса методом. Этот параметр может быть сочетанием следующих значений.

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**\_ \_ Добавление ссылки в репсинк DS \_**


</dt> <dd>

Заставляет исходный агент системы каталогов (DSA) проверить наличие локального DSA в списке репликация источника. Если локальный DSA отсутствует, он добавляется. Это гарантирует, что источник отправляет уведомления об изменениях.

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ репсинк \_ все \_ источники**


</dt> <dd>

Это значение не поддерживается.

**Windows server 2008 R2, Windows server 2008 и Windows server 2003:** Выполняет синхронизацию из всех источников.

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS \_ репсинк, \_ асинхронная \_ операция**


</dt> <dd>

Выполняет эту операцию асинхронно.

**Windows server 2008 R2, Windows server 2008 и Windows server 2003:** Требуется при использовании **DS \_ репсинк \_ все \_ источники**.

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS \_ репсинк \_ Force**


</dt> <dd>

Синхронизирует, даже если ссылка в данный момент отключена.

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**\_РЕПСИНК DS \_ Full**


</dt> <dd>

Синхронизирует, начиная с первого порядкового номера обновления (USN).

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**\_Служба DS репсинк \_ межсайтовые \_ сообщения**


</dt> <dd>

Синхронизирует с помощью ISM.

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ репсинк \_ No \_ undiscard**


</dt> <dd>

Не отменяет этот запрос на синхронизацию даже в случае, если аналогичная синхронизация находится в состоянии ожидания.

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ репсинк \_ периодически**


</dt> <dd>

Указывает, что эта операция является периодическим запросом синхронизации, запланированным администратором.

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**Служба DS \_ репсинк \_ срочно**


</dt> <dd>

Указывает, что эта операция является уведомлением об обновлении, которое помечено как срочное.

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**\_РЕПСИНК DS \_ для записи**


</dt> <dd>

Указывает, что эта реплика доступна для записи. Если этот флаг не установлен, реплика доступна только для чтения.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ микрософтактиведиректори<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**МСАД \_ реплнеигхбор**](msad-replneighbor.md)
</dt> </dl>

 

 





