---
description: Свойство Certificates извлекает коллекцию сертификатов, представляющую сертификаты в цепочке. Это свойство по умолчанию.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'Свойство IChain2:: Certificates'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 16fb08d020dcd59ed7caf22a0e93f4a4866b58642f12d0c131f3f0368bd3e7e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769655"
---
# <a name="ichain2certificates-property"></a>Свойство IChain2:: Certificates

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Certificates** извлекает коллекцию [**сертификатов**](certificates.md) , представляющую сертификаты в цепочке. Это свойство по умолчанию.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a>Значение свойства

Коллекция [**сертификатов**](certificates.md) , которая используется для получения сведений о каждом сертификате в цепочке. Первый сертификат в возвращенной коллекции **Certificates. Item**(1) является конечным сертификатом цепочки. Последний сертификат в коллекции **Certificates. Item**(**Certificates. Count**) — это [*корневой сертификат*](../secgloss/r-gly.md) цепочки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
