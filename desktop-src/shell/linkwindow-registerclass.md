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
ms.openlocfilehash: 75936c918a930698ef803b02743b935660e876b0d87d7f6d5eddce91d4f4c0a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968963"
---
# <a name="linkwindow_registerclass-function"></a>Линквиндов \_ registerClass, функция

\[эта функция доступна в Windows XP с пакетом обновления 2 (sp2) и Windows Server 2003. Он может быть изменен или недоступен в последующих версиях Windows. Вместо этого используйте [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) .\]

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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанного заголовка или файла библиотеки, поэтому она должна вызываться по порядковому значению. Вызовите [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL Shell32.dll, чтобы получить маркер модуля. Затем вызовите [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и порядковым номером 258, чтобы использовать эту функцию.

Используйте [**линквиндов \_ унрегистеркласс**](linkwindow-unregisterclass.md) , чтобы отменить регистрацию класса после использования.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения об элементах управления SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
