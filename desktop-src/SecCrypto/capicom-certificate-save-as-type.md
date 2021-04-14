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
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668525"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>\_ \_ \_ \_ Перечисление типа файла CAPICOM Certificate

Тип перечисления **CAPICOM \_ Certificate \_ resave \_ As \_** определяет формат файла, содержащего сведения о сертификате. Этот тип перечисления появился в CAPICOM 2,0.

## <a name="members"></a>Элементы



| Член                                  | Описание                                                                                                                                   | Значение |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ Certificate \_ Save \_ как \_ PFX** | Выходной файл будет отформатирован как файл PFX (PKCS 12), а все связанные с ним закрытые ключи также будут сохранены.<br/> | 0     |
| **CAPICOM \_ Certificate \_ Save \_ как \_ CER** | Выходной файл будет отформатирован как CER-файл без сохранения закрытых ключей.<br/>                                                        | 1     |



## <a name="remarks"></a>Комментарии

Тип перечисления **CAPICOM \_ Certificate- \_ \_ \_ Type** используется методом [**Certificate. Save**](certificate-save.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




