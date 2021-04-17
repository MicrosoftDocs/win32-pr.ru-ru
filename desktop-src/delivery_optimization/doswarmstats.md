---
title: Структура Досвармстатс (Deliveryoptimization. h)
description: Содержит поля для загрузки и передачи статистики для файла.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Структура Досвармстатс
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710552"
---
# <a name="doswarmstats-structure"></a>Структура Досвармстатс

Содержит поля для загрузки и передачи статистики для файла.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a>Члены

<dl> <dt>

**ИД**
</dt> <dd>

Строка, завершающаяся нулем, которая была указана с помощью вызова **аддфилевисранжес** .

</dd> <dt>

**саурцеурл**
</dt> <dd>

Строка, завершающаяся нулем, которая содержит имя файла на сервере (например, HTTPS:// &lt; Server &gt; / &lt; path &gt; /филе.екст).

</dd> <dt>

**Размер файла**
</dt> <dd>

Размер файла в байтах.

</dd> <dt>

**тоталбитесдовнлоадед**
</dt> <dd>

Общее число переданных байтов.

</dd> <dt>

**битесфромланпирс**
</dt> <dd>

Число байтов, передаваемых с одноранговых узлов.

</dd> <dt>

**битесфромграуппирс**
</dt> <dd>

Число байтов, переданных с одноранговых узлов.

</dd> <dt>

**битесфроминтернетпирс**
</dt> <dd>

Число байтов, передаваемых одноранговыми узлами Интернета.

</dd> <dt>

**битесфромхттп**
</dt> <dd>

Число байтов, передаваемых из HTTP.

</dd> <dt>

**битесфромдоинк**
</dt> <dd>

Только для внутреннего использования.

</dd> <dt>

**битестоланпирс**
</dt> <dd>

Число байтов, передаваемых одноранговым узлам локальной сети.

</dd> <dt>

**битестограуппирс**
</dt> <dd>

Число байтов, передаваемых одноранговым узлам группы.

</dd> <dt>

**битестоинтернетпирс**
</dt> <dd>

Число байтов, передаваемых одноранговым узлам Интернета.

</dd> <dt>

**хттпконнектионкаунт**
</dt> <dd>

Число HTTP-соединений.

</dd> <dt>

**доинкконнектионкаунт**
</dt> <dd>

Только для внутреннего использования.

</dd> <dt>

**ланконнектионкаунт**
</dt> <dd>

Число подключений к локальной сети.

</dd> <dt>

**граупконнектионкаунт**
</dt> <dd>

Число подключений к группе.

</dd> <dt>

**интернетконнектионкаунт**
</dt> <dd>

Число подключений к Интернету.

</dd> <dt>

**довнлоаддуратион**
</dt> <dd>

Длительность обмена файлами в миллисекундах.

</dd> <dt>

**downloadMode**
</dt> <dd>

Используемом режиме загрузки см. в разделе [**DownloadMode**](downloadmode.md).

</dd> <dt>

**status**
</dt> <dd>

Состояние перемещения файла см. в разделе [**свармстатус**](swarmstatus.md).

</dd> <dt>

**на задний план**
</dt> <dd>

Значение true, если это перенос в фоновом режиме.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





