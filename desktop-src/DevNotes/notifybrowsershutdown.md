---
description: Освобождает загрузчики классов Java, которые могли использоваться при просмотре приложений.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: Функция Нотифибровсершутдовн
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 60f361d8f9963081c4af2a840a01eb29f9946eb064cad2335f95b3622932add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826820"
---
# <a name="notifybrowsershutdown-function"></a>Функция Нотифибровсершутдовн

Освобождает загрузчики классов Java, которые могли использоваться при просмотре приложений.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпвресервед* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение **S \_ ОК**. В противном случае возвращаемое значение является кодом ошибки.

## <a name="remarks"></a>Remarks

Когда число окон браузера достигает нуля в интегрированном веб-режиме, эта функция освобождает загрузчики классов Java. Когда пользователь снова начинает просмотр приложений, виртуальная машина Java загрузит последние файлы классов.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
