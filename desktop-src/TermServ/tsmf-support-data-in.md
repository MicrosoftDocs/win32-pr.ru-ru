---
title: Структура TSMF_SUPPORT_DATA_IN
description: Содержит сведения о форматах мультимедиа. | Структура TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN структуры службы удаленных рабочих столов
- PTSMF_SUPPORT_DATA_IN службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ae90099b69494425344ff65b73090cce574b843cd1589572203a4786b38ff6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755780"
---
# <a name="tsmf_support_data_in-structure"></a>\_Данные поддержки \_ тсмф \_ в структуре

Содержит сведения о форматах мультимедиа. Эта структура используется методом [**куерипроперти**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) во время запросов **\_ \_ \_ \_ поддержки формата врдс запросов MF** .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a>Члены

<dl> <dt>

**гуидмфсессион**
</dt> <dd>

Сеанс.

</dd> <dt>

**нументриес**
</dt> <dd>

Количество структур в данных переменной длины.

</dd> <dt>

**...**
</dt> <dd>

Переменное число структур, содержащих данные в формате мультимедиа.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>         |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**\_Поддержка тсмф \_ нодедата \_ в**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





