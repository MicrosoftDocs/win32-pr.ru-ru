---
description: Задает или получает значение перечисления, которое указывает CAPICOM имя EKU. Это свойство по умолчанию.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'Свойство ИЕКУ:: Name'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648909"
---
# <a name="iekuname-property"></a>Свойство ИЕКУ:: Name

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Name** задает или получает значение перечисления, которое указывает CAPICOM Name EKU. Это свойство по умолчанию.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>Значение свойства

Значение перечисления [**CAPICOM \_ EKU**](capicom-eku.md) , которое указывает CAPICOM-имя EKU. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                           | Значение                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**\_другое расширенное EKU \_**</dt> </dl>                                                      | В сертификате используются определенные в локальной политике. Используется, если требуемое EKU не определено и значение OID должно быть задано приложением.<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**\_ \_ \_ Проверка подлинности сервера CAPICOM EKU**</dt> </dl>                                   | Сертификат можно использовать для проверки подлинности сервера.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**\_ \_ \_ Проверка подлинности клиента CAPICOM EKU**</dt> </dl>                                   | Сертификат можно использовать для проверки подлинности клиента.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**\_Подписывание \_ кода CAPICOM EKU \_**</dt> </dl>                                | Сертификат можно использовать для создания цифровой подписи.<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**\_ \_ Защита электронной почты CAPICOM EKU \_**</dt> </dl>                    | Сертификат можно использовать для защиты электронной почты.<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**\_Вход в \_ смарт-карту CAPICOM EKU \_**</dt> </dl>                       | Сертификат можно использовать для входа с использованием смарт-карты. Представлено в CAPICOM 2,0.<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**\_ \_ \_ Файловая система с шифрованием CAPICOM EKU \_**</dt> </dl> | Сертификат можно использовать для EFS. Представлено в CAPICOM 2,0.<br/>                                                                                      |



 

## <a name="remarks"></a>Комментарии

Когда значение этого свойства сбрасывается прямо или косвенно, полное [*состояние*](../secgloss/s-gly.md) объекта сбрасывается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
