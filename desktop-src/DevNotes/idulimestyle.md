---
description: Определяет, имеет ли заданный нецветный стиль подчеркивание.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: Функция Идулиместиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648915"
---
# <a name="idulimestyle-function"></a>Функция Идулиместиле

Определяет, имеет ли заданный нецветный стиль подчеркивание.

## <a name="syntax"></a>Синтаксис


```C++
UINT __cdecl IdUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пиместиле* \[ окне\]
</dt> <dd>

Структура **иместиле** , возвращаемая из функции [**пиместилефроматтр**](pimestylefromattr.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция может возвращать одно из следующих значений.

<dl> <dt>

**Имести \_ \_Min UL** (2002)
</dt> <dt>

**Имести \_ UL \_ None** (2002)
</dt> <dt>

**Имести \_ UL, \_ один** (2003)
</dt> <dt>

**Имести \_ UL, \_ пунктир** (2005)
</dt> <dt>

**Имести \_ UL- \_ толстая** (2006)
</dt> <dt>

**Имести \_ UL \_** (2011)
</dt> <dt>

**Имести \_ UL \_ сиккловер** (2012)
</dt> <dt>

**Имести \_ UL \_ сиккдисловер** (2013)
</dt> <dt>

**Имести \_ UL \_ дисловер** (2014)
</dt> <dt>

**Имести \_ UL \_ Max** (2014)
</dt> </dl>

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**пиместилефроматтр**](pimestylefromattr.md)
</dt> </dl>

 

 
