---
description: Задает или получает имя элемента CAPICOM атрибута. Это свойство по умолчанию.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Attribute.Name, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3234d02e5e0f68817896f2d0c9d05be25b55bbe97f49fea4d34bafbab627b2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773658"
---
# <a name="attributename-property"></a>Attribute.Name, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс криптографикаттрибутеобжект**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]

Свойство **Name** задает или получает имя элемента CAPICOM атрибута. Это свойство по умолчанию.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>Значение свойства

Значение перечисления [**\_ атрибутов CAPICOM**](capicom-attribute.md) , которое указывает CAPICOM-имя атрибута. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                                                                                 | Значение                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**\_время подписи CAPICOM проверенного \_ атрибута \_ \_**</dt> </dl>                         | Атрибут содержит время создания подписи.<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**\_ \_ \_ имя документа атрибута CAPICOM, прошедшего проверку подлинности \_**</dt> </dl>                      | Атрибут содержит имя подписанного документа.<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**\_ \_ \_ описание документа атрибута CAPICOM, прошедшего проверку подлинности \_**</dt> </dl> | Атрибут содержит описание подписанного документа.<br/>    |



 

## <a name="remarks"></a>Remarks

Когда значение этого свойства сбрасывается прямо или косвенно, полное состояние объекта сбрасывается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**attribute**](attribute.md)
</dt> </dl>

 

 
