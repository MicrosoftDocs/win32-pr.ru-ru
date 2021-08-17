---
description: Копирует сертификат в зашифрованную строку.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'Метод ICertificate2:: Export'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f002be332097baa0ad0947367259d15f0657d276770682b709402e2f0a333290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771771"
---
# <a name="icertificate2export-method"></a>Метод ICertificate2:: Export

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Export** копирует сертификат в зашифрованную строку. Закодированная строка может быть записана в файл или импортирована в новый объект [**сертификата**](certificate.md) .

## <a name="syntax"></a>Синтаксис


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Енкодингтипе* \[ в необязательное\]
</dt> <dd>

Значение перечисления [**\_ \_ типа CAPICOM Encoding**](capicom-encoding-type.md) , указывающее тип кодировки для операции экспорта. Значение по умолчанию — **CAPICOM- \_ кодировать \_ Base64**. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                  | Значение                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ кодирует \_ ANY**</dt> </dl>          | Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования. Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64. Представлено в CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ кодирует \_ Base64**</dt> </dl> | Данные сохраняются в виде строки в кодировке Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_двоичная кодировка CAPICOM \_**</dt> </dl> | Данные сохраняются в виде чисто двоичной последовательности.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Строка, содержащая экспортированный сертификат в указанной форме кодировки.

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

 

 
