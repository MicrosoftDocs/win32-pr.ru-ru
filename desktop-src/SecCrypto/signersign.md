---
description: Подписывает указанный файл.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: Функция Сигнерсигн
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: d9756fba3a931ddf09715b5086e613a9395c10c57c82fa18c64007aeb02b615c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973138"
---
# <a name="signersign-function"></a>Функция Сигнерсигн

Функция **сигнерсигн** подписывает указанный файл.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псубжектинфо* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ \_ сведений о субъекте-подписавшем**](signer-subject-info.md) , указывающий тему для подписывания.

</dd> <dt>

*псигнерцерт* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ сертификата подписи**](signer-cert.md) , указывающий сертификат, используемый для создания цифровой подписи.

</dd> <dt>

*псигнатуреинфо* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ \_ сведений о сигнатуре**](signer-signature-info.md) для подписи, которая содержит сведения о цифровой подписи.

</dd> <dt>

*ппровидеринфо* \[ в необязательное\]
</dt> <dd>

Указатель на структуру [**\_ \_ сведений о поставщике подписи**](signer-provider-info.md) , указывающий [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и сведения о [*закрытом ключе*](../secgloss/p-gly.md) , используемые для создания цифровой подписи.

Если значение этого параметра равно **null**, то значение параметра *псигнерцерт* должно указывать сертификат, связанный с CSP.

</dd> <dt>

*пвсзттптиместамп* \[ в необязательное\]
</dt> <dd>

URL-адрес сервера отметок времени.

</dd> <dt>

*псрекуест* \[ в необязательное\]
</dt> <dd>

Указатель на массив [**понятных структур \_ атрибутов**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) , которые добавляются в запрос на подписывание. Этот параметр пропускается, если параметр *пвсзттптиместамп* не содержит допустимого значения, отличного от **null**.

</dd> <dt>

*псипдата* \[ в необязательное\]
</dt> <dd>

32-разрядное значение, передаваемое в функции SIP в качестве дополнительных данных. Формат и содержимое этого объекта определяется поставщиком SIP.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, функция возвращает значение S \_ ОК.

Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сигнерсигнекс**](signersignex.md)
</dt> </dl>

 

 
