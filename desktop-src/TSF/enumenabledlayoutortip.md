---
title: Функция Енуменабледлайаутортип
description: Перечисляет все включенные раскладки клавиатуры или текстовые службы указанного параметра пользователя.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- Платформа текстовых служб Енуменабледлайаутортип Function
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681876"
---
# <a name="enumenabledlayoutortip-function"></a>Функция Енуменабледлайаутортип

Перечисляет все включенные раскладки клавиатуры или текстовые службы указанного параметра пользователя.

## <a name="syntax"></a>Синтаксис


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
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

*плайаутортиппрофиле* \[ заполняет\]
</dt> <dd>

Указатель на буфер, который получает массив ЛАЙАУТОРТИППРОФИЛЕ.

</dd> <dt>

*убуфленгс* \[ окне\]
</dt> <dd>

Длина буфера, на который указывает *плайаутортиппрофиле*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если *плайаутортиппрофиле* имеет **значение NULL**, число элементов клавиатуры, включенных в параметре пользователя; в противном случае число элементов клавиатуры, копируемых в *плайаутортиппрофиле*.

Для языков редактора методов ввода (IME) возвращаются все редакторы IME, даже если включен только один редактор IME. Например, если у пользователя включен новый быстрый редактор IME для CHT, функция **енуменабледлайаутортип** возвращает все 5 редакторов IME для CHT.

## <a name="remarks"></a>Комментарии

Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL. Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

Определение ЛАЙАУТОРТИППРОФИЛЕ:

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

