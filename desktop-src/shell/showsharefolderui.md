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
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346425"
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

## <a name="remarks"></a>Примечания

Эта функция не имеет связанного LIB файла. Для его использования необходимо использовать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Шовшарефолдеруив** (Юникод)<br/>                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**каншарефолдерв**](cansharefolderw.md)
</dt> </dl>

 

 
