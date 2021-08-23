---
title: Класс MSAD_ReplNeighbor
description: Представляет \_ \_ структуру соседей DS REPL, которая содержит сведения о состоянии входящей репликации для определенной пары контекста именования (NC) и исходного сервера.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- Класс MSAD_ReplNeighbor Active Directory
- Active Directory класса MSAD_ReplNeighbor, описание
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0598116413d34334e0610895a9c3b0629399fed8bb482e0d08cdae9cafb17fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025762"
---
# <a name="msad_replneighbor-class"></a>\_Класс МСАД реплнеигхбор

Представляет структуру [**\_ \_ соседей DS REPL**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) , которая содержит сведения о состоянии входящей репликации для определенной пары контекста именования (NC) и исходного сервера, возвращаемые функцией [**дсрепликажетинфо**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a>Члены

Класс **МСАД \_ реплнеигхбор** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **МСАД \_ реплнеигхбор** содержит следующие методы.



| Метод                                                           | Описание                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**синкнамингконтекст**](syncnamingcontext-msad-replneighbor.md) | Синхронизирует целевой контекст именования с одним из его источников.<br/> |



 

### <a name="properties"></a>Свойства

Класс **МСАД \_ реплнеигхбор** имеет следующие свойства.

<dl> <dt>

**асинЦинтерситетранспортдн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает путь X. 500 объекта [**интерситетранспорт**](/windows/desktop/ADSchema/c-intersitetransport) , который соответствует транспорту, по которому выполняется репликация. Задайте для репликации RPC/IP **значение NULL** .

</dd> <dt>

**асинЦинтерситетранспортобжгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает идентификатор GUID объекта межсайтового транспорта, соответствующего свойству **асинЦинтерситетранспортдн** .

</dd> <dt>

**компрессчанжес**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, задан ли **флаг \_ \_ \_ сжатия \_ Changes НБР redirectory REPL** в свойстве **репликафлагс** .

</dd> <dt>

**дисаблесчедуледсинк**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, был ли установлен флаг **\_ \_ \_ \_ плановой \_ синхронизации DS REPL НБР Disabled Sync** в свойстве **репликафлагс** .

</dd> <dt>

**Доменная**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает каноническое имя домена реплицированного NC.

</dd> <dt>

**досчедуледсинкс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, установлен ли флаг **DS \_ REPL \_ НБР \_ Do \_ Schedule \_ syncs** в свойстве **репликафлагс** .

</dd> <dt>

**фуллсинЦинпрогресс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, установлен ли **флаг \_ \_ \_ \_ \_ \_ выполнения НБР полной синхронизации DS REPL** в свойстве **репликафлагс** .

</dd> <dt>

**фуллсинкнекстпаккет**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, установлен ли в свойстве **репликафлагс** флаг **DS \_ REPL для \_ \_ полной \_ синхронизации \_ следующего \_ пакета** .

</dd> <dt>

**игноречанженотификатионс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, установлен ли **флаг \_ \_ НБР \_ Ignore \_ \_ извещения об изменении уведомлений DS REPL** в свойстве **репликафлагс** .

</dd> <dt>

**исделетедсаурцедса**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, представляет ли это соединение исходный контроллер домена, который был удален. **Значение true** , если это подключение представляет исходный контроллер домена, который был удален; в противном случае — **значение false**. Служба DS будет по-прежнему реплицировать эти подключения на некоторое время после удаления исходного контроллера домена.

</dd> <dt>

**ластсинкресулт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает код ошибки **HRESULT** для последней попытки репликации.

</dd> <dt>

**модифиеднумконсекутивесинкфаилурес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает число последовательных неудачных попыток репликации, не включая ожидаемые подключения. Например, если свойство **исделетедсаурцедса** имеет значение **true**, ожидается сбой.

</dd> <dt>

**намингконтекстдн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает путь X. 500 для сетевого контроллера, который реплицируется с помощью этого соединения.

</dd> <dt>

**намингконтекстобжгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает идентификатор GUID для реплицированного NC.

</dd> <dt>

**неверсинцед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, был ли установлен флаг **DS \_ REPL \_ НБР, \_ не \_ синхронизированный** в свойстве **репликафлагс** .

</dd> <dt>

**ночанженотификатионс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, был ли установлен флаг **DS \_ REPL \_ НБР \_ No \_ Change \_ Notifications** в свойстве **репликафлагс** .

</dd> <dt>

**нумконсекутивесинкфаилурес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает число последовательных неудачных попыток репликации.

</dd> <dt>

**репликафлагс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает набор флагов, задающих атрибуты и параметры для данных репликации. Это свойство может быть равно нулю или быть сочетанием одного или нескольких из следующих флагов.

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**Службы каталогов \_ REPL: \_ НБР \_ запись** (16 (0x10))


</dt> <dd>

Локальная копия контекста именования доступна для записи.

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**Службы каталогов \_ REPL \_ : \_ Синхронизация НБР \_ при \_ запуске** (32 (0x20))


</dt> <dd>

Репликация этого контекста именования из этого источника предпринимается при загрузке целевого сервера. Этот флаг обычно применяется только к соседям внутри сайта.

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**Службы каталогов \_ REPL: \_ НБР \_ выполнять \_ запланированные \_ синхронизации** (64 (0x40))


</dt> <dd>

Выполнение репликации по расписанию. Этот флаг обычно задается, если только расписание для этого контекста именования или источника не равно «никогда», то есть пустое расписание.

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**Службы каталогов \_ REPL: \_ НБР \_ использование \_ асинхронного \_ межсайтового \_ транспорта** (128 (0x80))


</dt> <dd>

Выполнение репликации непрямым путем через службу межсайтовых сообщений. Этот флаг устанавливается только при репликации по протоколу SMTP. Флаг не устанавливается при репликации по межсайтовому протоколу RPC/IP.

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**Службы каталогов \_ \_НБР \_ Синхронизация двух \_ сторон \_ репликации** (512 (0x200))


</dt> <dd>

Если задано значение, указывает, что после завершения входящей репликации целевой сервер должен сообщить исходному серверу о необходимости синхронизации в обратном направлении. Данная функция используется в скриптах коммутируемого доступа, когда коммутируемое подключение может инициировать только один из двух серверов. Например, этот параметр можно использовать в головном офисе организации и филиале, где филиал подключается к корпоративному офису через Интернет через коммутируемое подключение к поставщику услуг Интернета.

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**Службы каталогов \_ REPL \_ НБР \_ возвращает \_ \_ родительские объекты** (2048 (0x800))


</dt> <dd>

Данный сосед находится в состоянии, когда он возвращает родительские объекты перед дочерними. Он входит в это состоянии после получения дочернего объекта перед его родителем.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**Службы каталогов \_ \_ \_ \_ \_ \_ Выполняется полная синхронизация REPL НБР** (65536 (0x10000))


</dt> <dd>

Сервер назначения выполняет полную синхронизацию с исходного сервера. При полной синхронизации не используются векторы, которые создают обновления (например, [**DS \_ REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) для фильтрации обновлений. Полная синхронизация не используется в качестве части протокола репликации по умолчанию.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**Службы каталогов \_ \_ \_ \_ \_ Следующий \_ пакет для НБР полной синхронизации REPL** : (131072 (0x20000))


</dt> <dd>

Последний пакет из источника указал изменение объекта, который еще не был создан целевым сервером. Следующий запрашиваемый пакет сообщает исходному серверу, что все атрибуты измененного объекта помещаются в пакет.

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**Службы каталогов \_ REPL: \_ НБР \_ не \_ синхронизировано** (2097152 (0x200000))


</dt> <dd>

Синхронизация никогда не была завершена успешно от данного источника.

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**Службы каталогов \_ REPL \_ НБР с \_ вытеснением** (16777216 (0x1000000))


</dt> <dd>

Модуль репликации временно прекратил обработку этого соседа для обслуживания другого соседа с более высоким приоритетом, либо для этой секции, либо для другой секции. Механизм репликации продолжит обработку этого соседа после завершения высокоприоритетной работы.

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**Службы каталогов \_ \_НБР \_ игнорировать \_ \_ уведомления об изменениях** (67108864 (0x4000000))


</dt> <dd>

Этот сосед имеет значение отключить синхронизацию на основе уведомлений. В пределах узла контроллеры домена синхронизируются друг с другом на основе уведомлений, когда происходят изменения. Этот параметр не разрешает этому соседу выполнять синхронизацию, активируемую уведомлениями. Сосед по-прежнему будет выполнять синхронизацию в соответствии с расписанием или в ответ на запрошенные вручную синхронизации.

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**Службы каталогов \_ REPL \_ НБР \_ Отключить \_ запланированную \_ синхронизацию** (134217728 (0x8000000))


</dt> <dd>

Для этого соседа задано значение не выполнять синхронизацию в соответствии с расписанием. Единственный способ, которым этот сосед будет выполнять синхронизацию, — в ответ на уведомления об изменениях или на синхронизацию вручную.

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**Службы каталогов \_ REPL: \_ НБР \_ Сжатие \_ изменений** (268435456 (0x10000000))


</dt> <dd>

Изменения, полученные из этого источника, должны быть сжаты. Сжатие обычно происходит, только если исходный сервер находится на другом сайте.

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**Службы каталогов \_ REPL \_ : \_ НБР \_ без \_ уведомлений об изменениях** (536870912 (0x20000000))


</dt> <dd>

От данного источника не следует получать уведомления об изменениях. Обычно задается, только если исходный сервер находится на другом сайте.

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**Службы каталогов \_ REPL \_ НБР \_ частичный \_ \_ набор атрибутов** (1073741824 (0x40000000))


</dt> <dd>

Данный сосед находится в состоянии перестроения содержимого данной реплики из-за изменения в частичном наборе атрибутов.

</dd> </dl>

</dd> <dt>

**саурцедсааддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает DNS-адрес исходного контроллера домена.

> [!Note]  
> Эта строка содержит измененный идентификатор GUID, а не часто используемое каноническое DNS-имя.

 

</dd> <dt>

**саурцедсакн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает компонент пути к объекту для DSA, представляющего исходный контроллер домена. Эта строка часто похожа на имя компьютера, но не всегда идентична.

</dd> <dt>

**саурцедсадн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает путь X. 500 для DSA, представляющего исходный контроллер домена.

</dd> <dt>

**саурцедсаинвокатионид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает идентификатор вызова, который использовался исходным сервером на момент последней репликации.

</dd> <dt>

**саурцедсаобжгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает идентификатор GUID для агента службы каталогов (DSA), который представляет исходный контроллер домена (DC).

</dd> <dt>

**саурцедсасите**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает сайт, содержащий исходный контроллер домена.

</dd> <dt>

**синконстартуп**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, установлен ли в свойстве **репликафлагс** флаг **службы DS \_ REPL \_ НБР \_ Sync \_ On \_ Startup** .

</dd> <dt>

**тимеофластсинкаттемпт**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает метку времени для последней попытки репликации.

</dd> <dt>

**тимеофластсинксукцесс**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает метку времени для последней успешной попытки репликации.

</dd> <dt>

**твовайсинк**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, установлен ли в свойстве **репликафлагс** флаг **\_ \_ \_ \_ \_ синхронизации DS REPL НБР Two** .

</dd> <dt>

**усеасинЦинтерситетранспорт**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, установлен ли в свойстве **репликафлагс** флаг **DS \_ REPL \_ НБР \_ USE \_ Async \_ межсайтового \_ транспорта** .

</dd> <dt>

**уснаттрибутефилтер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение свойства **уснластобжчанжесинцед** в конце последнего успешного завершения цикла репликации. Нуль, если нет успешно завершенных циклов репликации.

</dd> <dt>

**уснластобжчанжесинцед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение [**неизмененного**](/windows/desktop/ADSchema/a-usnchanged) атрибута последнего полученного обновления объекта.

</dd> <dt>

**Writeable (Доступно для записи)**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, установлен ли флаг **DS \_ REPL \_ НБР \_ Write** в свойстве **репликафлагс** .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ микрософтактиведиректори<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

