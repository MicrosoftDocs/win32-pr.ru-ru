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
ms.openlocfilehash: a52ac620e5ec9aa3d9060d35921fcfd9c5bcc6e73cebf71ef336ceb54fc0806e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956913"
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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта. Для динамической привязки к StorProp.dll необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                          |
| DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции управления устройствами](device-management-functions.md)
</dt> </dl>

 

