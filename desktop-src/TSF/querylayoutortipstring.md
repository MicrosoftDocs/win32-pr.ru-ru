---
title: Функция Куерилайаутортипстринг
description: Запрашивает указанную строку, которая представляет формат списка раскладки клавиатуры или списка профилей служб текстового ввода.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- Платформа текстовых служб Куерилайаутортипстринг Function
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682042"
---
# <a name="querylayoutortipstring-function"></a>Функция Куерилайаутортипстринг

Запрашивает указанную строку, которая представляет формат списка раскладки клавиатуры или списка профилей служб текстового ввода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
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

Атрибут должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция может возвращать одно из этих значений.



| Код возврата                                                                                  | Описание                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Все макеты или профили, определенные в *ПСЗ* , являются допустимыми.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Один или несколько макетов или профилей, определенных в *ПСЗ* , являются недопустимыми.<br/> |



 

## <a name="remarks"></a>Комментарии

Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL. Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

Формат строки в списке макета:

<LangID 1>: <КЛИД 1>; \[ ...<LangID N>:<KLID N>

Формат строки в списке профиля службы текстового ввода:

<LangID 1>: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX};

Ниже приведен пример значения для параметра *ПСЗ* .

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

