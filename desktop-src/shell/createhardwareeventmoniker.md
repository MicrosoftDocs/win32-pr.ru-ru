---
description: Создает моникер, представляющий аппаратный компонент и связанный с ним обработчик событий. Функция автозапуска использует эту функцию, чтобы разрешить приложениям использовать события автозапуска.
title: Функция Креатехардваривентмоникер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: c22f01835f9c526e95a4330e6ad35d370421e604
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841245"
---
# <a name="createhardwareeventmoniker-function"></a>Функция Креатехардваривентмоникер

\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003. Он может быть изменен или недоступен в последующих версиях Windows.\]

Создает моникер, представляющий аппаратный компонент и связанный с ним обработчик событий. Функция автозапуска использует эту функцию, чтобы разрешить приложениям использовать события автозапуска.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор CLSID* \[ окне\]
</dt> <dd>

Тип: **рефклсид**

Идентификатор класса, к которому привязывается моникер.

</dd> <dt>

*псзевенсандлер* \[ окне\]
</dt> <dd>

Тип: **LPCTSTR**

Имя обработчика событий.

</dd> <dt>

*ппмоникер* \[ заполняет\]
</dt> <dd>

Тип: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***

Адрес переменной указателя, получающей указатель интерфейса [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Используйте **креатехардваривентмоникер** при регистрации работающих приложений, чтобы эти приложения имели доступ к событиям автозапуска. Чтобы использовать события автозапуска в выполняющихся приложениях, необходимо сначала создать новый компонент, реализующий интерфейс [**ихвевенсандлер**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) . Инициализируйте этот интерфейс со значением Иниткмдлине из записи конкретного обработчика в разделе **обработчиков** , так как автозапуск не вызывает метод [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) .

Необходимо вызвать **креатехардваривентмоникер** , чтобы получить моникер, представляющий компонент и его обработчик событий. Затем используйте значение, возвращенное в параметре *ппмоникер* , для регистрации компонента в запущенной таблице объектов (ROT), как показано в примере.

Обратите внимание, что **креатехардваривентмоникер** не определен в файле заголовка. Чтобы использовать его в коде, необходимо получить обработчик для файла Shsvcs.dll с помощью вызова [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Затем этот маркер используется в вызове [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения экземпляра функции **креатехардваривентмоникер** .

Для вызова [**ируннингобжекттабле:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) необходимо ввести в реестр следующие сведения о **AppID** .

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>None</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shsvcs.dll</dt> </dl> |



 

 
