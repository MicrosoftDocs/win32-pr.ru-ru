---
description: Создает экземпляр подсистемы захвата.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: Функция Мфкреатекаптурингине
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711278"
---
# <a name="mfcreatecaptureengine-function"></a>Функция Мфкреатекаптурингине

\[Мфкреатекаптурингине не поддерживается и может быть изменен или недоступен в будущем. \]

Создает экземпляр подсистемы захвата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппкаптурингине* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**имфкаптурингине**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) . Вызывающий объект должен освободить интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение S \_ ОК. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта и не объявлена в общедоступном файле заголовка. Для динамической привязки к MFCaptureEngine.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                     |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
