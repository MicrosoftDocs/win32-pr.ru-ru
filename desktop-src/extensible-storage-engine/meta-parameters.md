---
description: Дополнительные сведения о параметрах meta.
title: Параметры Meta
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 455b46465733a906b879dcedc4b5a2f4e6ef1f9e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472480"
---
# <a name="meta-parameters"></a>Параметры Meta


_**Применимо к:** Windows | Windows Сервером_

## <a name="meta-parameters"></a>Параметры Meta

Этот раздел содержит параметры, используемые для управления другими параметрами.

JET_paramConfiguration  
129  
Этот параметр предоставляет несколько наборов значений по умолчанию для всего набора системных параметров. Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации. Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию.

Кроме того, сам параметр может иметь другие последствия поведения ядра СУБД.

В настоящее время существует две поддерживаемые конфигурации:

  - Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти.

  - Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию.

При небольшой конфигурации по умолчанию для следующих системных параметров задаются указанные значения:


| <p>Системный параметр</p> | <p>Новое значение по умолчанию</p> | 
|-------------------------|--------------------------|
| <p>JET_paramMaxSessions</p> | <p>30 000</p> | 
| <p>JET_paramMaxOpenTables</p> | <p>2147483647</p> | 
| <p>JET_paramMaxCursors</p> | <p>2147483647</p> | 
| <p>JET_paramMaxVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramMaxTemporaryTables</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileSize</p> | <p>64</p> | 
| <p>JET_paramLogBuffers</p> | <p>1</p> | 
| <p>JET_paramDbExtensionSize</p> | <p>16</p> | 
| <p>JET_paramPageTempDBMin</p> | <p>14</p> | 
| <p>JET_paramCacheSizeMax</p> | <p>16</p> | 
| <p>JET_paramCheckpointDepthMax</p> | <p>65536</p> | 
| <p>JET_paramLRUKHistoryMax</p> | <p>10</p> | 
| <p>JET_paramOutstandingIOMax</p> | <p>16</p> | 
| <p>JET_paramStartFlushThreshold</p> | <p>1</p> | 
| <p>JET_paramStopFlushThreshold</p> | <p>2</p> | 
| <p>JET_paramNoInformationEvent</p> | <p>1</p> | 
| <p>JET_paramCacheSizeMin</p> | <p>16</p> | 
| <p>JET_paramPreferredVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileCreateAsynch</p> | <p>0</p> | 
| <p>JET_paramGlobalMinVerPages</p> | <p>1</p> | 
| <p>JET_paramPageHintCacheSize</p> | <p>32</p> | 
| <p>JET_paramDisablePerfmon</p> | <p>1</p> | 
| <p>JET_paramEnableFileCache</p> | <p>1</p> | 
| <p>JET_paramEnableViewCache</p> | <p>1</p> | 
| <p>JET_paramVerPageSize</p> | <p>1024</p> | 
| <p>JET_paramEnableAdvanced</p> | <p>0</p> | 
| <p>JET_paramCheckpointIOMax</p> | <p>8</p> | 



Небольшая конфигурация также имеет ряд других изменений в ядре СУБД, в том числе:

  - Все ресурсы, управляемые системными параметрами, выделяются из кучи по мере необходимости

  - Другие внутренние ресурсы, используемые ядром СУБД, масштабируются по размеру.

  - Различные операции обслуживания масштабируются обратно во избежание фонового действия потока.


| | | <p>Значение по умолчанию:</p> | <p>1 (устаревший)</p> | | <p>Тип:</p> | <p>Целое число</p> | | <p>Допустимый диапазон:</p> | <p>0 – 1</p> | | <p>Область.</p> | <p>Экземпляр</p> | | <p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p> | <p>Да</p> | | <p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p> | <p>Нет</p> | | <p>Влияет на физический макет:</p> | <p>Нет</p> | | <p>Влияет на надежность:</p> | <p>Нет</p> | | <p>Влияет на производительность:</p> | <p>Да</p> | | <p>Влияет на ресурсы:</p> | <p>Да</p> | | <p>"Доступность":</p> | <p>начиная с Windows Server 2008 и Windows Vista</p> | 



JET_paramEnableAdvanced  
130  
Этот параметр используется для управления тем, когда ядро СУБД принимает или отклоняет изменения в подмножестве системных параметров. Этот параметр используется совместно с JET_paramConfiguration, чтобы предотвратить установку некоторых системных параметров из значений по умолчанию выбранной конфигурации.

Следующие системные параметры будут защищены от установки, если этот параметр имеет значение false:

  - JET_paramMaxSessionsfon

  - JET_paramMaxOpenTables

  - JET_paramPreferredMaxOpenTables

  - JET_paramMaxCursors

  - JET_paramMaxVerPages

  - JET_paramMaxTemporaryTables

  - JET_paramLogBuffers

  - JET_paramWaitLogFlush

  - JET_paramLogCheckpointPeriod

  - JET_paramLogWaitingUserMax

  - JET_paramDbExtensionSize

  - JET_paramPageTempDBMin

  - JET_paramPageFragment

  - JET_paramBatchIOBufferMax

  - JET_paramCacheSizeMax

  - JET_paramLRUKCorrInterval

  - JET_paramLRUKHistoryMax

  - JET_paramLRUKPolicy

  - JET_paramLRUKTimeout

  - JET_paramLRUKTrxCorrInterval

  - JET_paramOutstandingIOMax

  - JET_paramStartFlushThreshold

  - JET_paramStopFlushThreshold

  - JET_paramCacheSize

  - JET_paramCacheSizeMin

  - JET_paramPreferredVerPages

  - JET_paramBackupChunkSize

  - JET_paramBackupOutstandingReads

  - JET_paramLogFileCreateAsynch

  - JET_paramRecordUpgradeDirtyLevel

  - JET_paramGlobalMinVerPages

  - JET_paramPageHintCacheSize

  - JET_paramVersionStoreTaskQueueMax

  - JET_paramDBAPageAvailMin

  - JET_paramMaxRandomIOSize

  - JET_paramCachedClosedTables

  - JET_paramEnableFileCache

  - JET_paramEnableViewCache

  - JET_paramVerPageSize

  - JET_paramCheckpointIOMax


| | | <p>Значение по умолчанию:</p> | <p>True</p> | | <p>Тип:</p> | <p>Логическое</p> | | <p>Допустимый диапазон:</p> | <p>False, true</p> | | <p>Область.</p> | <p>Экземпляр</p> | | <p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p> | <p>Да</p> | | <p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p> | <p>Да</p> | | <p>Влияет на физический макет:</p> | <p>Нет</p> | | <p>Влияет на надежность:</p> | <p>Нет</p> | | <p>Влияет на производительность:</p> | <p>Нет</p> | | <p>Влияет на ресурсы:</p> | <p>Нет</p> | | <p>"Доступность":</p> | <p>начиная с Windows Server 2008 и Windows Vista</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетинит](./jetinit-function.md)
