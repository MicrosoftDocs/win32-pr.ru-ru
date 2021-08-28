---
description: Добавляет объект сертификата в коллекцию.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'Метод ICertificates2:: Add'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4de1c00e3f006a69fa3c6babfa2aa44a1ad618050e5802ac4c9578dc3f93937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101054"
---
# <a name="icertificates2add-method"></a>Метод ICertificates2:: Add

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Add** добавляет объект [**сертификата**](certificate.md) в коллекцию. Этот метод появился в CAPICOM 2,0.

## <a name="syntax"></a>Синтаксис


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сертификат* \[ окне\]
</dt> <dd>

Объект [**сертификата**](certificate.md) , добавляемый в коллекцию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
