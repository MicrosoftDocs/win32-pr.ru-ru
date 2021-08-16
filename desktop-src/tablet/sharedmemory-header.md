---
description: Хранит сведения о разделах общей памяти.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: Структура SHAREDMEMORY_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9ae596819feb4bd70aa47e7881521e5a69e5bd0a509b974e591d08907efda51c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966803"
---
# <a name="sharedmemory_header-structure"></a>\_Структура заголовка шаредмемори

Хранит сведения о разделах общей памяти.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбтотал**
</dt> <dd>

Размер (в байтах) данных, на которые ссылается эта структура заголовка.

</dd> <dt>

**кбоффсетснс**
</dt> <dd>

Размер (в байтах), в котором серийные номера смещены от структуры заголовка.

</dd> <dt>

**идксевент**
</dt> <dd>

Индекс события. Это значение увеличивается с помощью последовательных событий.

</dd> <dt>

**двевент**
</dt> <dd>

Событие, связанное с этим заголовком.

</dd> <dt>

**согласуется**
</dt> <dd>

Идентификатор курсора, на который ссылается заголовок общей памяти.

</dd> <dt>

**sn**
</dt> <dd>

Серийный номер заголовка общей памяти.

</dd> <dt>

**сисевт**
</dt> <dd>

системное событие с префиксом SE \_ \* , связанное с этим заголовком. Дополнительные сведения см. в разделе "Примечания".

</dd> <dt>

**сисевтдата**
</dt> <dd>

Структура [**\_ \_ данных системных событий**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) , связанная с системным событием.

</dd> <dt>

**кпаккетс**
</dt> <dd>

Число пакетов, связанных с текущим разделом общей памяти.

</dd> <dt>

**кбпаккетс**
</dt> <dd>

Размер пакетов в байтах, связанных с текущим разделом общей памяти.

</dd> <dt>

**фснспресент**
</dt> <dd>

Флаг, указывающий, имеются ли серийные номера в текущем разделе общей памяти.

</dd> </dl>

## <a name="remarks"></a>Remarks

Для элемента **сисевт** определены следующие значения.


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_данные системных событий \_**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



