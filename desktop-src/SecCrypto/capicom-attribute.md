---
description: Определяет тип атрибута, связанного с сигнатурой.
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: Перечисление CAPICOM_ATTRIBUTE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: b03f91d0737b29b98adeb7e6a56bf9eccd35cc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669141"
---
# <a name="capicom_attribute-enumeration"></a>\_Перечисление АТРИБУТОВ CAPICOM

Тип **перечисления \_ атрибутов CAPICOM** определяет тип атрибута, связанного с [*сигнатурой*](../secgloss/d-gly.md).

## <a name="members"></a>Элементы



| Член                                                       | Описание                                                                | Значение |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| **\_время подписи CAPICOM проверенного \_ атрибута \_ \_**         | Атрибут содержит время создания подписи.<br/> | 0     |
| **\_ \_ \_ имя документа атрибута CAPICOM, прошедшего проверку подлинности \_**        | Атрибут содержит имя подписанного документа.<br/>         | 1     |
| **\_ \_ \_ описание документа атрибута CAPICOM, прошедшего проверку подлинности \_** | Атрибут содержит описание подписанного документа.<br/>    | 2     |



## <a name="remarks"></a>Комментарии

Тип **перечисления \_ атрибутов CAPICOM** используется свойством [**Attribute.Name**](attribute-name.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
