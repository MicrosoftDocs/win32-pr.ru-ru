---
title: Структура TSMF_SUPPORT_NODEDATA_OUT
description: Используется в \_ \_ структуре out данных поддержки тсмф \_ для хранения сведений о поддерживаемых форматах мультимедиа.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT структуры службы удаленных рабочих столов
- PTSMF_SUPPORT_NODEDATA_OUT службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3eb4c515963e13d2a7919c58a6d55ca4b2a7600c429a33516093215b5ac0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869014"
---
# <a name="tsmf_support_nodedata_out-structure"></a>\_Структура тсмф поддержки \_ нодедата \_ out

Используется в структуре [**\_ \_ \_ out данных поддержки тсмф**](tsmf-support-data-out.md) для хранения сведений о поддерживаемых форматах мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**nodeId**
</dt> <dd>

Узел.

</dd> <dt>

**хрсуппортстатус**
</dt> <dd>

Поддерживается ли приемник, идентифицируемый параметром *клсидневсинк* .

Возможные значения:.

<dt>

0
</dt> <dd>

Не поддерживается

</dd> <dt>

1
</dt> <dd>

Поддерживается

</dd> </dl>

Другие значения не определены.

</dd> <dt>

**клсидневсинк**
</dt> <dd>

Приемник, связанный с типом носителя.

</dd> <dt>

**суппортедмедиатипеиндекс**
</dt> <dd>

Отсчитываемый от нуля индекс типа носителя, поддерживаемого приемником.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>         |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**\_Исходящие \_ данные поддержки тсмф \_**](tsmf-support-data-out.md)
</dt> </dl>

 

 





