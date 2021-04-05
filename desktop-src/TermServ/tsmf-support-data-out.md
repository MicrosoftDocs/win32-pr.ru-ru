---
title: Структура TSMF_SUPPORT_DATA_OUT
description: Содержит сведения о форматах мультимедиа. | Структура TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT структуры службы удаленных рабочих столов
- PTSMF_SUPPORT_DATA_OUT службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000082"
---
# <a name="tsmf_support_data_out-structure"></a>\_ \_ Структура out данных поддержки тсмф \_

Содержит сведения о форматах мультимедиа. Эта структура используется методом [**куерипроперти**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) во время запросов **\_ \_ \_ \_ поддержки формата врдс запросов MF** .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**гуидмфсессион**
</dt> <dd>

Оно должно соответствовать свойству **гуидмфсессион** в соответствующих [**\_ данных поддержки тсмф \_ \_ в**](tsmf-support-data-in.md) структуре.

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

[**ТСМФ \_ Поддержка \_ нодедата \_**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





