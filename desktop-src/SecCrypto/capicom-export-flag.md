---
description: '\_ \_ Перечислимый тип флага CAPICOM определяет, будут ли игнорироваться ошибки экспорта закрытого ключа.'
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: Перечисление CAPICOM_EXPORT_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d6be9953640eeb2eb1d6c7fad812f5efe2d2da2f6888a01b4450c638ab68bfca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772469"
---
# <a name="capicom_export_flag-enumeration"></a>\_ \_ Перечисление флагов CAPICOM Export

Перечислимый тип **\_ \_ флага CAPICOM** определяет, будут ли игнорироваться ошибки экспорта закрытого ключа.

## <a name="members"></a>Элементы



| Член                                                            | Описание                                               | Значение |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **\_ \_ по умолчанию для экспорта CAPICOM**                                      | Любые ошибки экспорта закрытого ключа не пропускаются.<br/> | 0     |
| **CAPICOM \_ Export \_ игнорировать \_ ошибку закрытого \_ ключа \_ без \_ экспорта \_** | Все ошибки экспорта закрытого ключа игнорируются.<br/>     | 1     |



## <a name="remarks"></a>Remarks

\_ \_ Тип перечисления флагов CAPICOM Export используется следующим методом:

-   [**Certificates. Save**](certificates-save.md)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




