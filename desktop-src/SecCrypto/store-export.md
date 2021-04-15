---
description: Копирует содержимое открытого хранилища сертификатов в закодированную строку.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Метод Store. Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669074"
---
# <a name="storeexport-method"></a>Метод Store. Export

\[Метод **Export** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Export** копирует содержимое открытого [*хранилища сертификатов*](../secgloss/c-gly.md) в закодированную строку.

## <a name="syntax"></a>Синтаксис


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сохранить* \[ как в необязательное\]
</dt> <dd>

Значение перечисления " [CAPICOM \_ Store \_ \_ — \_ тип](capicom-store-save-as-type.md) ", которое указывает формат для операции экспорта. Значение по умолчанию — CAPICOM \_ Store \_ Сохранить \_ как \_ сериализованное. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                     | Значение                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <dt>**CAPICOM \_ Store \_ Сохранить \_ как \_ сериализованный**</dt> </dl> | Хранилище сохраняется в сериализованном формате.<br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <dt>**CAPICOM \_ Store \_ Сохранить \_ как \_ PKCS7**</dt> </dl>                | Хранилище сохраняется в \# формате PKCS 7.<br/>   |



 

</dd> <dt>

*Енкодингтипе* \[ в необязательное\]
</dt> <dd>

Значение перечисления [ \_ \_ типа CAPICOM Encoding](capicom-encoding-type.md) , указывающее тип кодировки экспортируемого хранилища. Значение по умолчанию — CAPICOM- \_ кодировать \_ Base64. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                  | Значение                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ кодирует \_ ANY**</dt> </dl>          | Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования. Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64. Представлено в CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ кодирует \_ Base64**</dt> </dl> | Данные сохраняются в виде строки в кодировке Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_двоичная кодировка CAPICOM \_**</dt> </dl> | Данные сохраняются в виде чисто двоичной последовательности.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает строку, содержащую сертификаты из хранилища в указанной форме кодировки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Магазин**](store.md)
</dt> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> </dl>

 

 
