---
description: Освобождает блокировку, полученную с помощью Ексклусивелокк в общем режиме.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'Метод Кшарелоккнх:: Ексклусивеунлокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 20d614f733b1668e3dea7619629cf2833f1d6af40384e679aea79a7a48279724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667840"
---
# <a name="csharelocknhexclusiveunlock-method"></a>Метод Кшарелоккнх:: Ексклусивеунлокк

Освобождает блокировку, полученную с помощью [**ексклусивелокк**](csharelocknh--exclusivelock.md) в общем режиме.

## <a name="syntax"></a>Синтаксис


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Каждый вызов [**ексклусивелокк**](csharelocknh--exclusivelock.md) должен быть сопряжен с ровно одним вызовом **ексклусивеунлокк** , чтобы избежать риска взаимоблокировки.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ексклусивелокк**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
