---
description: Сохраняет сертификат в файл.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'Метод ICertificate2:: Save'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685391"
---
# <a name="icertificate2save-method"></a>Метод ICertificate2:: Save

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Save** сохраняет сертификат в файл. Этот метод появился в CAPICOM 2,0.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя файла* \[ окне\]
</dt> <dd>

Строка, содержащая имя выходного файла, в котором будет сохранен сертификат.

</dd> <dt>

*Пароль* \[ в необязательное\]
</dt> <dd>

Строка, содержащая пароль в [*виде открытого текста*](../secgloss/p-gly.md) для файла [*закрытого ключа*](../secgloss/p-gly.md) . Пароль может содержать до 32 символов Юникода, включая завершающий нуль-символ. Сведения о защите пароля см. в разделе [обработка паролей](../secbp/handling-passwords.md).

</dd> <dt>

*Сохранить* \[ как в необязательное\]
</dt> <dd>

Значение перечисления [**\_ \_ \_ \_ типа CAPICOM Certificate**](capicom-certificate-save-as-type.md) , определяющее формат выходного файла. По умолчанию используется элемент **CAPICOM \_ Certificate \_ Save \_ как \_ CER**. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                  | Значение                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <dt>**CAPICOM \_ Certificate \_ Save \_ как \_ CER**</dt> </dl> | Выходной файл будет отформатирован как CER-файл без сохранения закрытых ключей.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <dt>**CAPICOM \_ Certificate \_ Save \_ как \_ PFX**</dt> </dl> | Выходной файл будет отформатирован как PFX-файл (PKCS \# 12), и все связанные с ним закрытые ключи также будут сохранены.<br/> |



 

</dd> <dt>

*Инклудеоптион* \[ в необязательное\]
</dt> <dd>

Значение элемента [**CAPICOM \_ Certificate \_ включает \_**](capicom-certificate-include-option.md) перечисление параметров, которое указывает, сколько сертификатов в цепочке сохраняется в выходном файле. По умолчанию CAPICOM \_ Certificate \_ включает \_ только конечную \_ сущность \_ . В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                                                             | Значение                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CAPICOM \_ Certificate \_ включает \_ цепочку, \_ кроме \_ root**</dt> </dl> | Сохраняет все сертификаты в цепочке, за исключением корневой сущности<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**CAPICOM \_ Certificate \_ включает \_ всю \_ цепочку**</dt> </dl>                    | Сохранение всей цепочки сертификатов<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**CAPICOM \_ Certificate \_ — \_ только конечная \_ сущность \_**</dt> </dl>       | Сохраняет только сертификат конечного объекта<br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
