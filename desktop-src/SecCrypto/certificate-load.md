---
description: Импортирует сертификат из файла.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'Метод ICertificate2:: Load'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fceb6ba9a9868711aefae64865c08e49551e20e8a05686e1691f390f05b76071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771546"
---
# <a name="icertificate2load-method"></a>Метод ICertificate2:: Load

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Load** импортирует сертификат из файла. Этот метод появился в CAPICOM 2,0.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя файла* \[ окне\]
</dt> <dd>

Строка, содержащая путь к CER-файлу или PFX, который содержит данные сертификата.

</dd> <dt>

*Пароль* \[ в необязательное\]
</dt> <dd>

Строка, содержащая пароль в [*виде открытого текста*](../secgloss/p-gly.md) для файла [*закрытого ключа*](../secgloss/p-gly.md) . Пароль может содержать до 32 символов Юникода, включая завершающий нуль-символ. Сведения о защите пароля см. в разделе [обработка паролей](../secbp/handling-passwords.md).

</dd> <dt>

*Кэйсторажефлаг* \[ в необязательное\]
</dt> <dd>

Значение перечисления [**\_ \_ \_ флагов хранилища CAPICOM Key**](capicom-key-storage-flag.md) , определяющее флаги хранилища ключей. По умолчанию используется \_ хранилище CAPICOM key \_ \_ . В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                           | Значение                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**\_хранилище CAPICOM \_ key \_ по умолчанию**</dt> </dl>                       | Хранилище ключей по умолчанию.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**\_хранилище CAPICOM Key, \_ \_ экспортируемое**</dt> </dl>              | Ключ доступен для экспорта.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**\_ \_ \_ защищенное пользователем хранилище CAPICOM key \_**</dt> </dl> | Ключ защищен пользователем.<br/> |



 

</dd> <dt>

*Кэйлокатион* \[ в необязательное\]
</dt> <dd>

Значение перечисления " [**CAPICOM \_ key \_ Location**](capicom-key-location.md) ", определяющее типы расположения ключей. Значение по умолчанию — "CAPICOM \_ текущий \_ ключ пользователя" \_ . В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                               | Значение                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**CAPICOM \_ текущий \_ \_ ключ пользователя**</dt> </dl>    | Ключ — это ключ пользователя.<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**ключ CAPICOM на \_ локальном \_ компьютере \_**</dt> </dl> | Ключ является ключом компьютера.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
