---
description: Освобождает общую блокировку.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'Метод Кшарелоккнх:: Шареунлокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 2bf59b6e1aa0f6718cece105007a8ba502291c23868aca6ec55283dd7292f8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162189"
---
# <a name="csharelocknhshareunlock-method"></a>Метод Кшарелоккнх:: Шареунлокк

Освобождает общую блокировку.

## <a name="syntax"></a>Синтаксис


```C++
void ShareUnlock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Каждый вызов [**шарелокк**](csharelocknh--sharelock.md) должен быть сопряжен с ровно одним вызовом **шареунлокк**. Только поток, который успешно вызывает **шарелокк** , может вызвать **шареунлокк**; в противном случае может возникнуть взаимоблокировка.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**шарелокк**](csharelocknh--sharelock.md)
</dt> </dl>

 

 
