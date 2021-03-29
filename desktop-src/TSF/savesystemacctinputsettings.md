---
title: Функция Савесистемакктинпутсеттингс
description: Применяет параметр "Пользовательская раскладка клавиатуры и служба текстового ввода" к кусту "системные учетные записи".
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- Платформа текстовых служб Савесистемакктинпутсеттингс Function
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414845"
---
# <a name="savesystemacctinputsettings-function"></a>Функция Савесистемакктинпутсеттингс

Применяет параметр "Пользовательская раскладка клавиатуры и служба текстового ввода" к кусту "системные учетные записи".

## <a name="syntax"></a>Синтаксис


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвндпарент* \[ окне\]
</dt> <dd>

Родительское окно для диалогового окна "предупреждение". Диалоговое окно предупреждение не всегда отображается и отображается соответствующим образом. Если этот параметр имеет **значение NULL**, диалоговое окно предупреждения отображаться не будет.

</dd> <dt>

*хсаурцерегкэй* \[ окне\]
</dt> <dd>

Корневой раздел реестра для копируемого параметра пользователя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение



| Код возврата                                                                          | Описание                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**УСЛОВИЯ**</dt> </dl>  | Функция выполнена успешно.<br/>   |
| <dl> <dt>**ISFALSE**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="remarks"></a>Комментарии

Куст системной учетной записи — это \_ Пользователи hKey \\ . ПО УМОЛЧАНИю, HKEY \_ Users \\ s-1-5-19 и hKey \_ Users \\ s-1-5-20.

## <a name="examples"></a>Примеры

Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). В следующем примере показано, как получить указатель на эту функцию.

> [!Note]  
> Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL. Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
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



 

