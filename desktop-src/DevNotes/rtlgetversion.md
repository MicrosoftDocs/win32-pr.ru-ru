---
description: Возвращает сведения о версии текущей работающей операционной системы.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Функция Ртлжетверсион (Нтддк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141255"
---
# <a name="rtlgetversion-function"></a>Функция Ртлжетверсион

Возвращает сведения о версии текущей работающей операционной системы.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпверсионинформатион* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**\_ осверсионинфов справа налево**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) или структуру [**\_ осверсионинфоексв RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) , содержащую сведения о версии текущей операционной системы. Вызывающий объект указывает, какая структура ввода используется, устанавливая для элемента **двосверсионинфосизе** структуры размер в байтах используемой структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает состояние \_ Success.

## <a name="remarks"></a>Комментарии

**Ртлжетверсион** является эквивалентом функции [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) в Windows SDK. См. пример в Windows SDK, в котором показано, как получить версию системы.

При использовании **ртлжетверсион** для определения того, запущена ли определенная версия операционной системы, вызывающая сторона должна проверить номера версий, которые больше или равны номеру требуемой версии. Это гарантирует, что тест версии будет выполнен для более поздних версий Windows.

Поскольку функции операционной системы могут быть добавлены в распространяемую библиотеку DLL, проверка только основного и дополнительного номеров версий не является самым надежным способом проверки наличия определенного компонента системы. Драйвер должен использовать [**ртлверифиверсионинфо**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) для проверки наличия определенного компонента системы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                                                                     |
| Целевая платформа<br/>          | <dl> <dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| Header<br/>                   | <dl> <dt>Нтддк. h (включение Нтддк. h)</dt> </dl>                                                     |
| Библиотека<br/>                  | <dl> <dt>NTDLL. lib; </dt> <dt>NtosKrnl. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**псжетверсион**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
