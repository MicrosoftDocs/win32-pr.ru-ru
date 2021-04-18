---
description: Список различных типов уведомлений, которые могут быть получены прикреплением.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (Ктмтипес. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683838"
---
# <a name="notification_mask"></a>\_Маска уведомления

Список различных типов уведомлений, которые могут быть получены прикреплением.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_Маска уведомления \_ транзакции**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



Маска, которая указывает все допустимые биты для уведомления транзакции.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**Предварительная \_ Подготовка уведомлений транзакции \_**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Это уведомление вызывается после того, как клиент вызывает [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) , а либо диспетчер ресурсов (RM) не поддерживает однофазную фиксацию, либо старший диспетчер транзакций (TM) вызывает [**препрепаринлистмент**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment). Это уведомление получает RMs, указывая, что он должен выполнить все действия, которые могут привести к тому, что другие RMs должны присоединиться к транзакции, например очистить свой кэш. После выполнения этих операций RM должен вызвать [**препрепарекомплете**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete). Для получения этого уведомления RM также должен поддерживать **\_ \_ фиксацию** **\_ уведомлений транзакции \_ Prepare** и извещения о транзакции.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**\_Подготовка уведомления \_ транзакции**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Это уведомление вызывается после завершения обработки предварительной **\_ \_ подготовки уведомления о транзакции** . Он сигнализирует диспетчеру ресурсов завершить всю работу, связанную с этим зачислением, чтобы гарантировать успешную операцию фиксации, а также выполнить операцию аварийного завершения. Как правило, основная часть работы для транзакции выполняется на этапе подготовки. Для устойчивых RMs они должны регистрировать свое состояние до вызова функции [**препарекомплете**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) . Это последняя вероятность того, что RM запросит, что была произведена откат транзакции.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**\_уведомление о \_ ФИКСАЦИи транзакции**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Это уведомление сигнализирует диспетчеру ресурсов завершить всю работу, связанную с этим зачислением. Как правило, RM освобождает все блокировки и освобождает все сведения, необходимые для отката транзакции. RM должен ответить, вызвав функцию [**коммиткомплете**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) , когда она завершит эти операции.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**\_откат уведомления \_ транзакции**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Это уведомление сообщает RM о необходимости отмены всей выполненной работы, связанной с транзакцией.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**Предварительная \_ Подготовка уведомлений транзакции \_ \_ завершена**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Это уведомление сообщает старший TM, что операция предварительной подготовки успешно завершена.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**\_Подготовка к уведомлению транзакции \_ \_ завершена**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Это уведомление сообщает старший TM, что операция подготовки успешно завершена.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**\_уведомление о \_ фиксации транзакции \_ завершено**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Это уведомление сообщает старший TM о том, что операция фиксации выполнена успешно.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**\_откат уведомления о транзакции \_ \_ завершен**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Это уведомление сообщает старший TM, что операция отката была выполнена успешно.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_Восстановление уведомления \_ транзакции**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Это уведомление передает службе RMs о том, что они должны восстановить свое состояние, так как результат транзакции должен быть доставлен снова. Например, при восстановлении RM и при наличии транзакций, оставшихся под сомнением. Это уведомление доставляется после разрешения сомнительного состояния.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**\_ \_ \_ фиксация одной фазы уведомления транзакции \_**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Это уведомление сообщает RM о завершении и фиксации транзакции без использования протокола двухфазной фиксации. Если RM хочет использовать двухэтапный процесс, он должен ответить, вызвав функцию [**синглефасережект**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_ \_ фиксация делегата уведомления транзакции \_**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



KTM сообщает старший TM о выполнении операции фиксации.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**\_запрос на \_ Восстановление \_ уведомления транзакции**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



KTM сообщает старшему TM-запросу о состоянии сомнительной транзакции.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**Предварительная \_ \_ Подготовка прикрепления для уведомления транзакции \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Это уведомление сообщает старший TM, что предварительно подготовленные уведомления должны доставляться по указанному зачислению.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ Последнее восстановление транзакции с уведомлением \_**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Это уведомление означает, что операция восстановления для этого RM завершена.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**уведомление о неопределенном \_ \_ состоянии транзакции**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Указанная транзакция находится в состоянии «под сомнением». RM получает это уведомление во время операций восстановления, когда транзакция была подготовлена, но старший диспетчер транзакций (TM) не доступен. Например, если транзакция включает в себя удаленный TM и этот узел недоступен, его узел недоступен или локальная служба [координатор распределенных транзакций](/previous-versions/windows/desktop/ms684146(v=vs.85)) недоступна, состояние транзакции считается сомнительным.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**ТРАНЗАКЦИЯ \_ уведомления \_ TM \_ Online**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



TM находится в оперативном режиме и принимает запросы.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**\_ \_ результат запроса уведомления \_ транзакции**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Сообщает RMs о том, что имеются сведения о результатах, и что необходимо сделать запрос на эту информацию.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_уведомление о \_ ФИКСАЦИи транзакции \_**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Зарезервировано.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                            |
| Header<br/>                   | <dl> <dt>Ктмтипес. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Координатор распределенных транзакций](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[Константы диспетчера транзакций ядра](kernel-transaction-manager-constants.md)
</dt> <dt>

[**креатинлистмент**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[**коммиткомплете**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[**жетнотификатионресаурцеманажер**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[**жетнотификатионресаурцеманажерасинк**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[**препарекомплете**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[**синглефасережект**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[**\_уведомление транзакции**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

