---
description: Помечает время указанной темой. Эта функция поддерживает отметку времени Authenticode. Чтобы выполнить отметку времени X. 509 для инфраструктуры открытых ключей (RFC 3161), используйте функцию SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: Функция Сигнертиместамп
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999213"
---
# <a name="signertimestamp-function"></a>Функция Сигнертиместамп

Время функции **сигнертиместамп** помечает указанную тему. Эта функция поддерживает отметку времени Authenticode. Чтобы выполнить отметку времени X. 509 для инфраструктуры открытых ключей (RFC 3161), используйте функцию [**SignerTimeStampEx2**](signertimestampex2.md) .

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псубжектинфо* \[ окне\]
</dt> <dd>

Адрес структуры [**\_ \_ сведений о субъекте-подписывания**](signer-subject-info.md) , которая представляет субъект для отметки времени.

</dd> <dt>

*пвсзттптиместамп* \[ окне\]
</dt> <dd>

Адрес строки в Юникоде, завершающейся нулем, которая содержит URL-адрес сервера отметок времени.

</dd> <dt>

*псрекуест* \[ в необязательное\]
</dt> <dd>

Адрес структуры [**\_ атрибутов шифрования**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) , которая содержит дополнительные атрибуты, добавляемые в запрос метки времени.

Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.

</dd> <dt>

*псипдата* \[ в необязательное\]
</dt> <dd>

32-разрядное значение, передаваемое в функции SIP в качестве дополнительных данных. Формат и содержимое этого объекта определяется поставщиком SIP.

Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, функция возвращает значение S \_ ОК.

Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
