---
title: Функция Сетдефаултлайаутортипусеррег
description: Задает указанную раскладку клавиатуры или текстовую службу в качестве входного элемента по умолчанию для пользовательского реестра.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- Платформа текстовых служб Сетдефаултлайаутортипусеррег Function
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 340e21d8d7416d72361a0e505029500b9a7dde3e53d3388c9311ae3351345c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118875288"
---
# <a name="setdefaultlayoutortipuserreg-function"></a>Функция Сетдефаултлайаутортипусеррег

Задает указанную раскладку клавиатуры или текстовую службу в качестве входного элемента по умолчанию для пользовательского реестра.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзусеррег* \[ в необязательное\]
</dt> <dd>

Путь к реестру пользователя. Если этот параметр имеет **значение NULL**, \_ \_ используется текущий пользователь hKey.

</dd> <dt>

*псзсистемрег* \[ в необязательное\]
</dt> <dd>

Путь реестра системы. Если этот параметр имеет **значение NULL**, \_ \_ используется система локального компьютера hKey \\ .

</dd> <dt>

*псзсофтваререг* \[ в необязательное\]
</dt> <dd>

Путь реестра программного обеспечения. Если этот параметр имеет **значение NULL**, \_ \_ \\ используется программное обеспечение для локального компьютера hKey.

</dd> <dt>

*ПСЗ* \[ окне\]
</dt> <dd>

Строка, представляющая список раскладок клавиатуры или профиль служб текстового ввода.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Битовое значение, задающее следующие флаги:

> [!Note]  
> Следующие идентификаторы не определены в общедоступном файле заголовка. Необходимо либо использовать шестнадцатеричное значение, либо \# определить идентификаторы. Например, чтобы использовать СДЛОТ \_ ноапплитокуррентсессион, необходимо включить \# \_ в код определение сдлот ноапплитокуррентсессион 0x00000001.

 



| Значение                                                                                                                                                                                                                                                                         | Значение                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**Сдлот \_ НОАППЛИТОКУРРЕНТСЕССИОН**</dt> <dt>0x00000001</dt> </dl> | Сохраняет параметр в реестре, но четкое не обновляет параметр клавиатуры среды выполнения текущего сеанса. Если альтернативный путь реестра задан в **сетдефаултлайаутортипусеррег**, этот флаг должен быть установлен.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**Сдлот \_ АППЛИТОКУРРЕНТСРЕАД**</dt> <dt>0x00000002</dt> </dl>          | Применяет параметр сразу к текущему потоку.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение



| Код возврата                                                                          | Описание                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**УСЛОВИЯ**</dt> </dl>  | Функция выполнена успешно.<br/>   |
| <dl> <dt>**ISFALSE**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="remarks"></a>Remarks

Формат строки в списке макета:

<LangID 1>: <КЛИД 1>; \[ ...<LangID N>:<KLID N>

Формат строки в списке профиля службы текстового ввода:

<LangID 1>: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX};

Ниже приведен пример значения для параметра *ПСЗ* .


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Примеры

Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). В следующем примере показано, как получить указатель на эту функцию.

> [!Note]  
> Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL. Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

