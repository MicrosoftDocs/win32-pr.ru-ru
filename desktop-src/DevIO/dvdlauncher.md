---
description: Проверяет, соответствует ли регион носителя в DVD-дисководе региону DVD-дисковода.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: Функция Двдлаунчер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142214"
---
# <a name="dvdlauncher-function"></a>Функция Двдлаунчер

Проверяет, соответствует ли регион носителя в DVD-дисководе региону DVD-дисковода.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* \[ окне\]
</dt> <dd>

Маркер окна верхнего уровня, используемый для любого требуемого пользовательского интерфейса.

</dd> <dt>

*Буква_диска* \[ окне\]
</dt> <dd>

Буква диска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена удачно и области совпадают, возвращаемое значение не равно нулю. В противном случае возвращаемое значение равно нулю.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта. Для динамической привязки к StorProp.dll необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                          |
| DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции управления устройствами](device-management-functions.md)
</dt> </dl>

 

