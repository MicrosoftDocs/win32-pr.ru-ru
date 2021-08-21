---
description: Удаляет из коллекции один объект сертификата.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'Метод ICertificates2:: Remove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 72ab0624784078b2c496032639c371280ff0019ac957d3c579e2c3c9080629bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770436"
---
# <a name="icertificates2remove-method"></a>Метод ICertificates2:: Remove

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Remove** удаляет из коллекции один объект [**сертификата**](certificate.md) . Этот метод появился в CAPICOM 2,0.

## <a name="syntax"></a>Синтаксис


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Значение индекса для удаляемого объекта [**сертификата**](certificate.md) . Этот параметр может иметь один из следующих возможных типов.



| Тип                                                                                                                                                                                                                                                              | Значение                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> * * * * <dt>Длинный *</dt> * * * *<dt></dt> </dl>                                                | Объект [**сертификата**](certificate.md) по указанному индексу в коллекции удален.<br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>* * * * Строка *</dt> * * * <dt></dt> </dl>                                        | Первый объект [**сертификата**](certificate.md) в коллекции, соответствующий отпечатку [*SHA-1*](../secgloss/s-gly.md) , который содержится в указанной строке, удаляется.<br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <dt>**[**Сертификат**](certificate.md)**</dt><dt></dt> </dl> | Удаляется первый объект [**сертификата**](certificate.md) в коллекции, соответствующий указанному объекту **сертификата** .<br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
