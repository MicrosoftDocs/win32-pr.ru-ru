---
description: Задает или получает параметр сертификата подписывания.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Свойство SignIn. Options
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7b4a787524e967b5356ed7fb5531a3ec7d7dbfb99d57fc75217a82f220468db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898840"
---
# <a name="signeroptions-property"></a>Свойство SignIn. Options

\[Свойство **Options** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **Options** задает или получает параметр сертификата подписывания.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Значение свойства

Значение элемента [**CAPICOM \_ Certificate \_ включает \_**](capicom-certificate-include-option.md) перечисление параметров, которое указывает параметр сертификата подписывания. Значение по умолчанию — \_ это \_ цепочка include-сертификатов, \_ \_ кроме \_ root. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                                                             | Значение                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CAPICOM \_ Certificate \_ включает \_ цепочку, \_ кроме \_ root**</dt> </dl> | Сохраняет все сертификаты в цепочке, за исключением корневой сущности.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**CAPICOM \_ Certificate \_ включает \_ всю \_ цепочку**</dt> </dl>                    | Сохраняет всю цепочку сертификатов.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**CAPICOM \_ Certificate \_ — \_ только конечная \_ сущность \_**</dt> </dl>       | Сохраняет только сертификат конечного объекта.<br/>                                     |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Автор подписи**](signer.md)
</dt> </dl>

 

 
