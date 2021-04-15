---
description: '\_Свойство NewEnum объекта цертификатеполиЦиес Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции.'
ms.assetid: 631a11c8-4442-493e-9406-bc63f79db548
title: CertificatePolicies._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2d5e90d4b906661119936ca1e893e3b6e17c9bf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689011"
---
# <a name="certificatepolicies_newenum-property"></a>ЦертификатеполиЦиес. \_ Свойство NewEnum

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для получения политик сертификатов.\]

Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Синтаксис


```VB
CertificatePolicies._NewEnum As IUnknown
```



## <a name="property-value"></a>Значение свойства

Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.

## <a name="remarks"></a>Комментарии

Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
