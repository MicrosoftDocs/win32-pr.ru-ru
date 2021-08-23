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
ms.openlocfilehash: f29963020290686521d5e3bd165d2c8fac6e5e0c96f34552ad11f725d95567cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654504"
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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
