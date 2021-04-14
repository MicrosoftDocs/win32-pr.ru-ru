---
description: Регистрирует класс окна, который позволяет использовать общий элемент управления SysLink в окне.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: Функция LinkWindow_RegisterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985672"
---
# <a name="linkwindow_registerclass-function"></a>Линквиндов \_ registerClass, функция

\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003. Он может быть изменен или недоступен в последующих версиях Windows. Вместо этого используйте [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) .\]

Регистрирует класс окна, который позволяет использовать общий элемент управления [Syslink](../controls/syslink-overview.md) в окне.

## <a name="syntax"></a>Синтаксис


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **bool** .

Возвращает **значение true** , если регистрация прошла успешно; В противном случае — **значение false** .

## <a name="remarks"></a>Примечания

Эта функция не имеет связанного заголовка или файла библиотеки, поэтому она должна вызываться по порядковому значению. Вызовите [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL Shell32.dll, чтобы получить маркер модуля. Затем вызовите [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и порядковым номером 258, чтобы использовать эту функцию.

Используйте [**линквиндов \_ унрегистеркласс**](linkwindow-unregisterclass.md) , чтобы отменить регистрацию класса после использования.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения об элементах управления SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
