---
description: Определяет формат файла, содержащего сведения о сертификате.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Перечисление CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 2000bd582475a227fdb638649ee1a634e488a21a7c09d84dd6e21dafc5e9aa42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772645"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>\_ \_ \_ \_ Перечисление типа файла CAPICOM Certificate

Тип перечисления **CAPICOM \_ Certificate \_ resave \_ As \_** определяет формат файла, содержащего сведения о сертификате. Этот тип перечисления появился в CAPICOM 2,0.

## <a name="members"></a>Элементы



| Член                                  | Описание                                                                                                                                   | Значение |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ Certificate \_ Save \_ как \_ PFX** | Выходной файл будет отформатирован как файл PFX (PKCS 12), а все связанные с ним закрытые ключи также будут сохранены.<br/> | 0     |
| **CAPICOM \_ Certificate \_ Save \_ как \_ CER** | Выходной файл будет отформатирован как CER-файл без сохранения закрытых ключей.<br/>                                                        | 1     |



## <a name="remarks"></a>Remarks

Тип перечисления **CAPICOM \_ Certificate- \_ \_ \_ Type** используется методом [**Certificate. Save**](certificate-save.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




