---
description: Функция Исвиндовредиректедфорпринт определяет, перенаправлено ли указанное окно на печать в данный момент.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: Функция Исвиндовредиректедфорпринт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719706"
---
# <a name="iswindowredirectedforprint-function"></a>Функция Исвиндовредиректедфорпринт

Функция **исвиндовредиректедфорпринт** определяет, перенаправлено ли указанное окно на печать в данный момент.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* \[ окне\]
</dt> <dd>

Дескриптор окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если окно в данный момент перенаправлено для печати, функция возвращает ненулевое значение. в противном случае возвращается ноль.

## <a name="remarks"></a>Комментарии

Окно перенаправляется для печати при обработке вызова [**принтвиндов**](/windows/desktop/api/Winuser/nf-winuser-printwindow). При вызове **принтвиндов** окно преобразует свое содержимое в контекст устройства без экрана.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>User32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**принтвиндов**](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**\_Печать WM**](/windows/desktop/gdi/wm-print)
</dt> <dt>

[**WM \_ принтклиент**](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

