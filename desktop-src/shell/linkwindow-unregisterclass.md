---
description: Отменяет регистрацию класса окна, зарегистрированного с помощью Линквиндов \_ registerClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: Функция LinkWindow_UnregisterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 05a50d5f3af72c31ee04a1a9e8264acb22327c38f79f765ce2ad7a740086747e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968943"
---
# <a name="linkwindow_unregisterclass-function"></a>Линквиндов \_ унрегистеркласс, функция

\[эта функция доступна в Windows XP с пакетом обновления 2 (sp2) и Windows Server 2003. Он может быть изменен или недоступен в последующих версиях Windows.\]

Отменяет регистрацию класса окна, зарегистрированного с помощью [**линквиндов \_ registerClass**](linkwindow-registerclass.md).

## <a name="syntax"></a>Синтаксис


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **bool** .

Возвращает **значение true** , если операция выполнена успешно; В противном случае — **значение false** .

## <a name="remarks"></a>Remarks

Эта функция не имеет связанного заголовка или файла библиотеки, поэтому она должна вызываться по порядковому значению. Вызовите [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL Shell32.dll, чтобы получить маркер модуля. Затем вызовите [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и порядковым номером 259, чтобы использовать эту функцию.

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

 

 
