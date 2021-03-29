---
description: 'Освобождает дескриптор от поставщика служб шифрования (CSP) или ключа API шифрования: следующего поколения (CNG).'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: Функция Фрикриптпровфромцертекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912039"
---
# <a name="freecryptprovfromcertex-function"></a>Функция Фрикриптпровфромцертекс

Функция **фрикриптпровфромцертекс** освобождает дескриптор как [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP), так и ключ API шифрования: следующего поколения (CNG).

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*факкуиред* \[ окне\]
</dt> <dd>

Значение типа, указывающее, был ли получен обработчик поставщика из [*сертификата*](../secgloss/c-gly.md).

</dd> <dt>

*хпров* \[ окне\]
</dt> <dd>

Описатель для CSP или маркера для ключа CNG.

</dd> <dt>

*двкэйспек* 
</dt> <dd>

Адрес переменной **типа DWORD** , которая получает дополнительные сведения о ключе. Это может быть одно из следующих значений.



| Значение                                                                                                                                                                                | Значение                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**по адресу \_ кэйексчанже**</dt> </dl>                     | Пара ключей является парой обмена ключами.<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**в \_ сигнатуре**</dt> </dl>                           | Пара ключей является парой сигнатур.<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**\_ \_ Спецификация ключа NCRYPT для сертификата \_**</dt> </dl> | Ключ является ключом CNG.<br/> **Windows Server 2003 и Windows XP:** Это значение не поддерживается.<br/> |



 

</dd> <dt>

*пвсзкапипровидер* \[ в необязательное\]
</dt> <dd>

Указатель на строку, завершающуюся нулем, для имени поставщика.

</dd> <dt>

*двпровидертипе* \[ окне\]
</dt> <dd>

Указывает тип CSP. Это может быть ноль или один из [типов поставщиков служб шифрования](cryptographic-provider-types.md). Если этот член равен нулю, контейнер ключей является одним из поставщиков хранилища ключей CNG.

</dd> <dt>

*пвсзтмпконтаинер* \[ в необязательное\]
</dt> <dd>

Указатель на строку, завершающуюся нулем, для имени временного контейнера ключей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
