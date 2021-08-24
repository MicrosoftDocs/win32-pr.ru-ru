---
description: Скачивает подпись файла .cab, проверяет разрешения, связанные с пакетами, и выполняет их на основе проверки подлинности.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: Функция Довнлоаджаваекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 628fdb1b8b0ec9979d844c8f48fb02fbf8f6a642a96c925f427c868160dd6b27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795264"
---
# <a name="downloadjavaex-function"></a>Функция Довнлоаджаваекс

Скачивает подпись файла .cab, проверяет разрешения, связанные с пакетами, и выполняет их на основе проверки подлинности.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Зарезервировано* \[ окне\]
</dt> <dd>

Этот параметр зарезервирован.

</dd> <dt>

*ппровидердата* \[ окне\]
</dt> <dd>

Структура [**\_ \_ данных поставщика шифрования**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) , содержащая данные сертификата, такие как разрешения файла и зоны.

</dd> <dt>

*пжава* \[ окне\]
</dt> <dd>

Структура [**\_ \_ поставщика политики Java**](/previous-versions//bb432350(v=vs.85)) , которая содержит данные, связанные с поставщиком политики.

</dd> <dt>

*пфунктионс* \[ окне\]
</dt> <dd>

Структура [**\_ \_ функций поставщика**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) , которая содержит список методов для проверки объектов сертификата, подписей и окончательных политик.

</dd> <dt>

*фцертификате* \[ окне\]
</dt> <dd>

Если сертификат имеется, этот параметр имеет **значение true**. В противном случае — **false**.

</dd> <dt>

*птруст* \[ окне\]
</dt> <dd>

Структура [**\_ доверия Java**](/windows/desktop/api/Capi/ns-capi-java_trust) , содержащая сведения о доверии, такие как закодированное разрешение, сигнатура кодировщика и подлинное возвращение кода политики.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение **S \_ ОК**. В противном случае возвращаемое значение является кодом ошибки.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
