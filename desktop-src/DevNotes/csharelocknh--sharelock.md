---
description: Получает общую блокировку.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'Метод Кшарелоккнх:: Шарелокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 7fd398228c6d0feb7e63133e8faeefd7a2fd3359bf62e80a8f398a3467424b90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654834"
---
# <a name="csharelocknhsharelock-method"></a>Метод Кшарелоккнх:: Шарелокк

Получает общую блокировку.

## <a name="syntax"></a>Синтаксис


```C++
void ShareLock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Каждый вызов **шарелокк** должен быть сопряжен с ровно одним вызовом [**шареунлокк**](csharelocknh--shareunlock.md). Только поток, который успешно вызывает **шарелокк** , может вызвать **шареунлокк**; в противном случае может возникнуть взаимоблокировка.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**шареунлокк**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
