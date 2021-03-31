---
title: Функция Сетдефаултлайаутортип
description: Задает указанную раскладку клавиатуры или службу текстового ввода в качестве входного элемента по умолчанию для текущего пользователя.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- Платформа текстовых служб Сетдефаултлайаутортип Function
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135427"
---
# <a name="setdefaultlayoutortip-function"></a>Функция Сетдефаултлайаутортип

Задает указанную раскладку клавиатуры или службу текстового ввода в качестве входного элемента по умолчанию для текущего пользователя.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПСЗ* \[ окне\]
</dt> <dd>

Строка, представляющая раскладку клавиатуры или список профилей служб текстового ввода.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Битовое значение, задающее следующие флаги.

> [!Note]  
> Следующие идентификаторы не определены в общедоступном файле заголовка. Необходимо либо использовать шестнадцатеричное значение, либо \# определить идентификаторы. Например, чтобы использовать СДЛОТ \_ ноапплитокуррентсессион, необходимо включить \# \_ в код определение сдлот ноапплитокуррентсессион 0x00000001.

 



| Значение                                                                                                                                                                                                                                                                         | Значение                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**Сдлот \_ НОАППЛИТОКУРРЕНТСЕССИОН**</dt> <dt>0x00000001</dt> </dl> | Сохраняет параметр в реестре, но четкое не обновляет параметр клавиатуры среды выполнения текущего сеанса. Если альтернативный путь реестра задан в [**сетдефаултлайаутортипусеррег**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), этот флаг должен быть установлен.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**Сдлот \_ АППЛИТОКУРРЕНТСРЕАД**</dt> <dt>0x00000002</dt> </dl>          | Применяет параметр сразу к текущему потоку.<br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение



| Код возврата                                                                          | Описание                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**УСЛОВИЯ**</dt> </dl>  | Функция выполнена успешно.<br/>   |
| <dl> <dt>**ISFALSE**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

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
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
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



 

