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
ms.openlocfilehash: 5c071d76712877650bba8ecf502687538bb6ac354e62a0285dc08e2f22f25873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103694"
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

## <a name="remarks"></a>Remarks

Эта функция не связана с библиотекой импорта или файлом заголовка. Он должен вызываться с помощью функций [**LoadLibrary**](-loadlibrary.md) и [**GetProcAddress**](-getprocaddress-.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**GetProcAddress**](-getprocaddress-.md)
</dt> <dt>

[**LoadLibrary**](-loadlibrary.md)
</dt> </dl>

 

 




