---
description: Устанавливает новое устройство. Пользователю предлагается выбрать устройство.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: Функция Инсталлневдевице
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: cb12e87ceee4812ffc8c0e39d961ce631e26c4ab8ca7ae555785c8ad8381ca01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405313"
---
# <a name="installnewdevice-function"></a>Функция Инсталлневдевице

Устанавливает новое устройство. Пользователю предлагается выбрать устройство.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвндпарент* \[ окне\]
</dt> <dd>

Маркер окна верхнего уровня, используемый для любого требуемого пользовательского интерфейса.

</dd> <dt>

*Классгуид* \[ окне\]
</dt> <dd>

Указатель на **идентификатор GUID** класса. Это необязательный параметр. Если этот параметр имеет **значение NULL**, пользователь запускается на странице Выбор обнаружения. Если этот параметр имеет **\_ значение GUID NULL** или **GUID \_ девкласс \_ Unknown**, то пользователь запускается на странице выбора класса.

</dd> <dt>

*Предзагрузка* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает состояние перезагрузки. Этот параметр может быть **di \_ Нидрестарт** или **di \_ нидребут**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполняется успешно, возвращается ненулевое значение.

Если функция выполняется неудачно, возвращается нулевое значение. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта. Для динамической привязки к NewDev.dll необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                        |
| DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции управления устройствами](device-management-functions.md)
</dt> </dl>

 

