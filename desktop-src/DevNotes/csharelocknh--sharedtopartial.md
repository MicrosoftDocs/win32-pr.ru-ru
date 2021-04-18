---
description: Изменяет общую блокировку на частичную блокировку.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'Метод Кшарелоккнх:: Шаредтопартиал'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657206"
---
# <a name="csharelocknhsharedtopartial-method"></a>Метод Кшарелоккнх:: Шаредтопартиал

Изменяет общую блокировку на частичную блокировку.

## <a name="syntax"></a>Синтаксис


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если получена частичная блокировка. в противном случае возвращается **значение false** , и блокировка остается в общем режиме.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
