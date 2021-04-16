---
description: Предотвращает получение блокировки более чем одним потоком.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: 'Кшарелоккнх: метод:P Артиаллокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657209"
---
# <a name="csharelocknhpartiallock-method"></a>Кшарелоккнх: метод:P Артиаллокк

Предотвращает получение блокировки более чем одним потоком.

## <a name="syntax"></a>Синтаксис


```C++
void PartialLock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Хотя **партиаллокк** действует, другие потоки, вызывающие [**шарелокк**](csharelocknh--sharelock.md) , могут войти в блокировку.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
