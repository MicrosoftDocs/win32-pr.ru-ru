---
description: Отображает вкладку Общий доступ к папке на странице свойств указанной папки.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: Функция Шовшарефолдеруи
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: 9683d7faee4bd44bd8f21e14250503f351e1a134119f978f872d7a0fe3ad6c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968263"
---
# <a name="showsharefolderui-function"></a>Функция Шовшарефолдеруи

Отображает вкладку **общий доступ к папке** на странице свойств указанной папки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвндпарент* \[ окне\]
</dt> <dd>

Тип: **HWND**

Маркер родительского окна для страницы свойств.

</dd> <dt>

*псзпас* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на строку, указывающую путь к папке, в которой отображается вкладка **совместного доступа к папке** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Эта функция всегда возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанного LIB файла. Для его использования необходимо использовать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Шовшарефолдеруив** (Юникод)<br/>                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**каншарефолдерв**](cansharefolderw.md)
</dt> </dl>

 

 
