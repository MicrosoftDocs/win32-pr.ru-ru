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
ms.openlocfilehash: 18d264b30b8f3ed4d06e80f236908dd7bc81dbe96c4eb9c3231fa330331e34f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940254"
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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта и не объявлена в общедоступном файле заголовка. Для динамической привязки к MFCaptureEngine.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
