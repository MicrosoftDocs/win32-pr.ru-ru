---
description: Определяет формат файла, содержащего сведения о сертификатах.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Перечисление CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 70185a7a48b7dc195727991fb0dcc35f4909451fa0e4da5f4100e8385adebc2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879374"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a>CAPICOM \_ Certificates \_ Сохранить \_ как \_ Перечисление типов

Тип перечисления **CAPICOM \_ Certificates \_ Save \_ As \_ Type** определяет формат файла, содержащего сведения о сертификатах. Этот тип перечисления появился в CAPICOM 2,0.

## <a name="members"></a>Элементы



| Член                                          | Описание                                          | Значение |
|-------------------------------------------------|------------------------------------------------------|-------|
| **CAPICOM \_ Certificates \_ Сохранить \_ как \_ сериализованный** | Сохраненные сертификаты сериализуются.<br/>    | 0     |
| **CAPICOM \_ Certificates \_ Сохранить \_ как \_ PKCS7**      | Сертификаты сохраняются в виде PKCS \# 7.<br/> | 1     |
| **CAPICOM \_ Certificates \_ Сохранить \_ как \_ PFX**        | Сертификаты сохраняются в формате PFX.<br/>      | 2     |



## <a name="remarks"></a>Remarks

\_Тип ПЕРЕЧИСЛЕНИЯ CAPICOM Certificates \_ Save \_ As \_ Type используется методом [**Certificates. Save**](certificates-save.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Заголовок<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




