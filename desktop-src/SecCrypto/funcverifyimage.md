---
description: Используется поставщиком служб шифрования (CSP) для проверки подписи библиотеки DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: Указатель функции CRYPT_VERIFY_IMAGE (Кспдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: b33e6e627c87840e4adb7615f7e3ca5932a7402a3b3ae7110be51c0847a5f67f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006682"
---
# <a name="crypt_verify_image-function-pointer"></a>\_Проверка шифрования \_ указатель функции изображения

Функция обратного вызова **функверифимаже** используется [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP) для проверки подписи библиотеки DLL.

Все вспомогательные библиотеки DLL, в которые CSP вызывает вызовы функций, должны быть подписаны аналогичным образом (и с тем же ключом), что и первичная библиотека CSP. Чтобы обеспечить эту сигнатуру, вспомогательные библиотеки DLL должны динамически загружаться с помощью функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Но перед загрузкой библиотеки DLL необходимо проверить подпись библиотеки DLL. CSP выполняет эту проверку, вызывая функцию **функверифимаже** , как показано в примере ниже.

## <a name="syntax"></a>Синтаксис


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсзимаже* \[ окне\]
</dt> <dd>

Адрес строки, завершающейся нулем, которая содержит путь и имя файла библиотеки DLL для проверки подписи.

</dd> <dt>

*пбсигдата* \[ окне\]
</dt> <dd>

Адрес буфера, содержащего подпись.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если функция завершается успешно, в противном случае — **значение false** .

## <a name="examples"></a>Примеры

В следующем примере показано, как использовать функцию обратного вызова **функверифимаже** для проверки подписи библиотеки DLL перед ее загрузкой CSP.


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Кспдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**кпаккуиреконтекст**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**втаблепровструк**](vtableprovstruc.md)
</dt> </dl>

 

 
