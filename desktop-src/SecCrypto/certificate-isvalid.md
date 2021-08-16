---
description: Создает цепочку проверки сертификатов для сертификата и возвращает объект Цертификатестатус, который содержит состояние действия сертификата.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: 'Метод ICertificate2:: IsValid'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97e31129497759fa73abb4456ea8d1b8d20748bef76629d6dd857954863f5aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126984"
---
# <a name="icertificate2isvalid-method"></a>Метод ICertificate2:: IsValid

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **IsValid** создает цепочку проверки сертификата для сертификата и возвращает объект [**цертификатестатус**](certificatestatus.md) , который содержит состояние действия сертификата.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.IsValid()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Криптографические объекты](cryptography-objects.md)
</dt> <dt>

[**Сертификат**](certificate.md)
</dt> </dl>

 

 
