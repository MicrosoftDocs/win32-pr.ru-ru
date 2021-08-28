---
description: Помечает время указанной темой и поддерживает задание меток времени для нескольких подписей.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: Функция SignerTimeStampEx3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7eb5c19292b451b1a3d0265da4bb178eafcc6f00
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468561"
---
# <a name="signertimestampex3-function"></a>Функция SignerTimeStampEx3

Функция **SignerTimeStampEx3** помечает указанную тему и поддерживает задание меток времени для нескольких подписей.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Флаг, указывающий тип создаваемой метки времени. Этот параметр может принимать одно из указанных ниже значений. Значения являются взаимоисключающими.




| Значение | Значение | 
|-------|---------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt></dl> | Задает отметку времени Authenticode.<br /><blockquote>[!Note]<br />Authenticode больше не является предпочтительным типом метки времени. Поддержка меток времени Authenticode может быть удалена в будущем. Вместо этого рекомендуется использовать RFC 3161.</blockquote><br /> | 
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt></dl> | Задает отметку времени, совместимую с RFC 3161.<br /> | 




 

</dd> <dt>

*двиндекс* \[ окне\]
</dt> <dd>

Указывает порядковый номер подписи, в которую будет добавлена метка времени. Если это значение равно нулю (0), внешняя подпись будет отметкой времени.

</dd> <dt>

*псубжектинфо* \[ окне\]
</dt> <dd>

Адрес структуры [**\_ \_ сведений о субъекте-подписывания**](signer-subject-info.md) , которая представляет субъект для отметки времени.

</dd> <dt>

*пвсзттптиместамп* \[ окне\]
</dt> <dd>

Адрес строки в Юникоде, завершающейся нулем, которая содержит URL-адрес сервера отметок времени.

</dd> <dt>

*псзалгорисмоид* \[ окне\]
</dt> <dd>

Хэш-алгоритм, используемый для выполнения отметок времени, соответствующих RFC 3161. Этот параметр не учитывается для меток времени Authenticode.

</dd> <dt>

*псрекуест* \[ в необязательное\]
</dt> <dd>

Необязательный элемент. Адрес структуры [**\_ атрибутов шифрования**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) , которая содержит дополнительные атрибуты, добавляемые в запрос метки времени.

Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.

</dd> <dt>

*псипдата* \[ в необязательное\]
</dt> <dd>

Необязательный элемент. 32-разрядное значение, передаваемое в качестве дополнительных данных в функции [*пакета интерфейса субъекта*](../secgloss/s-gly.md) (SIP). Формат и содержимое этого параметра определяется поставщиком SIP.

Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.

</dd> <dt>

*ппсигнерконтекст* \[ заполняет\]
</dt> <dd>

Необязательный элемент. Адрес указателя на структуру [**\_ контекста подписавшего**](signer-context.md) , который содержит подписанный большой двоичный объект. По завершении использования структуры **\_ контекста подписывающий** освободите ее, вызвав функцию [**сигнерфрисигнерконтекст**](signerfreesignercontext.md) .

</dd> <dt>

*пкриптополици* \[ в необязательное\]
</dt> <dd>

При наличии указателя на структуру [**\_ \_ \_ абзаца со строгой подписью сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) , содержащую параметры, используемые для проверки наличия строгих подписей. Метка времени должна пройти эту политику шифрования.

</dd> <dt>

*Сохраняется* 
</dt> <dd>

Зарезервировано. Это значение должно быть **равно NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, функция возвращает значение S \_ ОК.

Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Возможные коды ошибок, возвращаемые этой функцией, включают, но не ограничиваются следующим. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).




| Код возврата | Описание | 
|-------------|-------------|
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | Эта ошибка может возвращать следующие условия.<br /><ul><li>Для параметра <em>dwFlags</em> необходимо задать либо <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> , либо <strong>SIGNER_TIMESTAMP_RFC3161</strong> .</li><li><em>Сохраненный</em> параметр должен иметь <strong>значение NULL</strong>.</li><li>Если установить флаг <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> в параметре <em>dwFlags</em> , то необходимо присвоить параметру <em>двиндекс</em> значение 0.</li></ul> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сигнертиместамп**](signertimestamp.md)
</dt> <dt>

[**сигнертиместампекс**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 
