---
description: Создает обработчик потока байтов для источника мультимедиа MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: Функция MFCreateMP3ByteStreamPlugin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656549"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a>Функция MFCreateMP3ByteStreamPlugin

\[Этот API не поддерживается и может быть изменен или недоступен в будущем. Вместо этого приложения должны использовать [сопоставитель источников](source-resolver.md) для создания источника мультимедиа в формате MP3.\]

Создает обработчик потока байтов для источника мультимедиа MP3.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*riid* \[ окне\]
</dt> <dd>

Идентификатор IID запрошенного интерфейса. Задайте для этого параметра значение **IID \_ имфбитестреамхандлер** , чтобы получить указатель на интерфейс [**имфбитестреамхандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .

</dd> <dt>

*ппвхандлер* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс. Вызывающий объект должен освободить интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта. Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к mf.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |
| Окончание поддержки клиента<br/>    | Windows Vista<br/>                             |
| Поддержка конца сервера<br/>    | Windows Server 2008<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции Media Foundation](media-foundation-functions.md)
</dt> <dt>

[Обработчики схем и обработчики Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Сопоставитель источников](source-resolver.md)
</dt> </dl>

 

 
