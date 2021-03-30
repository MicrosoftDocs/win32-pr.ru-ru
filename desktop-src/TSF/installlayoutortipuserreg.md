---
title: Функция Инсталллайаутортипусеррег
description: Включает указанные раскладки клавиатуры или текстовые службы для указанного пользователя.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- Платформа текстовых служб Инсталллайаутортипусеррег Function
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802369"
---
# <a name="installlayoutortipuserreg-function"></a>Функция Инсталллайаутортипусеррег

Включает указанные раскладки клавиатуры или текстовые службы для указанного пользователя.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
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

Битовое значение, задающее следующие флаги.

> [!Note]  
> Следующие идентификаторы не определены в общедоступном файле заголовка. Необходимо либо использовать шестнадцатеричное значение, либо \# определить идентификаторы. Например, чтобы использовать **\_ Удаление илот** , необходимо включить `#define ILOT_UNINSTALL 0x00000001` в код.

 



| Значение                                                                                                                                                                                                                                                                      | Значение                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <dt>**Илот \_ Удаление**</dt> <dt>0x00000001</dt> </dl>                                           | То же, что и **илот \_ disabled**.<br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <dt>**Илот \_ ДЕФПРОФИЛЕ**</dt> <dt>0x00000002</dt> </dl>                                        | Задает указанный макет или Совет в качестве элемента по умолчанию.<br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <dt>**Илот \_ НОАППЛИТОКУРРЕНТСЕССИОН**</dt> <dt>0x00000020</dt> </dl> | Параметр сохраняется, но не применяется к текущему сеансу.<br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <dt>**Илот \_ КЛЕАНИНСТАЛЛ**</dt> <dt>0x00000040</dt> </dl>                                  | Отключает все текущие раскладки клавиатуры и текстовые службы.<br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <dt>**Илот \_ ОТКЛЮЧЕНные**</dt> <dt>0x00000080</dt> </dl>                                              | Отключает указанную раскладку клавиатуры и службу текстового ввода.<br/>        |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение



| Код возврата                                                                         | Описание                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**УСЛОВИЯ**</dt> </dl> | Функция выполнена успешно.<br/>   |
| <dl> <dt>**фасе**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="remarks"></a>Комментарии

Формат строки в списке макета:

<LangID 1>: <КЛИД 1>; \[ ...<LangID N>:<KLID N>

Формат строки в списке профиля службы текстового ввода:

<LangID 1>: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX};

Ниже приведен пример значения для параметра *ПСЗ* .


```C++
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
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

