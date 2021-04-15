---
description: Сохраняет объекты сертификата в коллекции.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Метод Certificates. Save
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669365"
---
# <a name="certificatessave-method"></a>Метод Certificates. Save

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Save** сохраняет объекты [**сертификата**](certificate.md) в коллекции.

## <a name="syntax"></a>Синтаксис


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя файла* \[ окне\]
</dt> <dd>

Строка, содержащая имя выходного файла, в котором будут сохранены сертификаты.

</dd> <dt>

*Пароль* \[ в необязательное\]
</dt> <dd>

Строка, содержащая пароль в [*виде открытого текста*](../secgloss/p-gly.md) для файла [*закрытого ключа*](../secgloss/p-gly.md) . Значением по умолчанию является пустая строка (""). Для пароля можно использовать до 32 символов Юникода, включая завершающий нуль-символ. Сведения о защите пароля см. в разделе [обработка паролей](../secbp/handling-passwords.md).

</dd> <dt>

*Сохранить* \[ как в необязательное\]
</dt> <dd>

Значение перечисления [**CAPICOM \_ Certificates \_ Сохранить \_ как \_ тип**](capicom-certificates-save-as-type.md) , определяющее формат выходного файла. По умолчанию CAPICOM \_ Certificates \_ сохраняется \_ как \_ PFX. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                                          | Значение                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <dt>**CAPICOM \_ Certificates \_ Сохранить \_ как \_ PFX**</dt> </dl>                      | Сертификаты сохраняются в формате PFX.<br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <dt>**CAPICOM \_ Certificates \_ Сохранить \_ как \_ PKCS7**</dt> </dl>                | Сертификаты сохраняются в виде PKCS \# 7.<br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <dt>**CAPICOM \_ Certificates \_ Сохранить \_ как \_ сериализованный**</dt> </dl> | Сертификаты сохраняются как сериализованные.<br/> |



 

</dd> <dt>

*Експортфлаг* \[ в необязательное\]
</dt> <dd>

Значение перечисления [**\_ \_ флагов CAPICOM Export**](capicom-export-flag.md) , которое указывает, пропускаются ли ошибки экспорта закрытого ключа. Значение по умолчанию — \_ Экспорт \_ по умолчанию CAPICOM. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                                                                                          | Значение                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <dt>**\_ \_ по умолчанию для экспорта CAPICOM**</dt> </dl>                                                                                                      | Ошибки экспорта закрытого ключа не пропускаются.<br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <dt>**CAPICOM \_ Export \_ игнорировать \_ ошибку закрытого \_ ключа \_ без \_ экспорта \_**</dt> </dl> | Ошибки экспорта закрытого ключа игнорируются.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.

Объекты [**сертификата**](certificate.md) можно получить с помощью метода [**Store. Load**](store-load.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сертификаты**](certificates.md)
</dt> </dl>

 

 
