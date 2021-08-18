---
description: Освобождает дескриптор поставщика служб шифрования (CSP) и при необходимости удаляет временный контейнер, созданный функцией Жеткриптпровфромцерт.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: Функция Фрикриптпровфромцерт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8797a6f48bcfb973a6c07a4b05ae0d39bc3b4522ab6f7ae70a80eaa77081da44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006792"
---
# <a name="freecryptprovfromcert-function"></a>Функция Фрикриптпровфромцерт

> [!IMPORTANT]
> Это нерекомендуемый API. Корпорация Майкрософт может удалить этот API в будущих выпусках.

 

Функция **фрикриптпровфромцерт** освобождает дескриптор [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и при необходимости удаляет временный контейнер, созданный функцией [**жеткриптпровфромцерт**](getcryptprovfromcert.md) .

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
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

Указатель на структуру [**хкриптпров**](hcryptprov.md) для CSP.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
