---
description: Получает блокировку потоков чтения/записи.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'Метод Кшарелоккнх:: Ексклусивелокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 16a5d2ba49d5ff1c25079a99a979d7a0fb4a51ee64d54fa4042152d7b010dc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667967"
---
# <a name="csharelocknhexclusivelock-method"></a>Метод Кшарелоккнх:: Ексклусивелокк

Получает блокировку потоков чтения/записи.

## <a name="syntax"></a>Синтаксис


```C++
void ExclusiveLock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Каждый вызов **ексклусивелокк** должен быть сопряжен с ровно одним вызовом [**ексклусивеунлокк**](csharelocknh--exclusiveunlock.md) , чтобы избежать риска взаимоблокировки.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ексклусивеунлокк**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
