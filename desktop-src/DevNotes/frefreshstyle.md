---
description: Перезагрузка параметров цвета из реестра.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: Функция Фрефрешстиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657267"
---
# <a name="frefreshstyle-function"></a>Функция Фрефрешстиле

Перезагрузка параметров цвета из реестра.

## <a name="syntax"></a>Синтаксис


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE в случае успешного выполнения; в противном случае — значение FALSE.

## <a name="remarks"></a>Комментарии

Эта функция не связана с библиотекой импорта или файлом заголовка. Он должен вызываться с помощью функций [**LoadLibrary**](-loadlibrary.md) и [**GetProcAddress**](-getprocaddress-.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**GetProcAddress**](-getprocaddress-.md)
</dt> <dt>

[**LoadLibrary**](-loadlibrary.md)
</dt> </dl>

 

 




