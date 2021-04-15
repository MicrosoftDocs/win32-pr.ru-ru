---
description: Указывает версию CTL3D сегодня, которая выполняется в данный момент.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Функция Ctl3dGetVer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: e548d8933538ea85ba94f6e120032453079d69ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648972"
---
# <a name="ctl3dgetver-function"></a>Функция Ctl3dGetVer

Указывает версию CTL3D сегодня, которая выполняется в данный момент.

## <a name="syntax"></a>Синтаксис


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение, содержащее основной номер версии в байте высокого порядка и дополнительный номер версии в байте нижнего порядка.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
