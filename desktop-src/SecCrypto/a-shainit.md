---
description: Инициирует хэширование потока данных.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: Функция A_SHAInit (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0081311988a5da0ae5ca21e924305918bb1e713a6cde3be1b77821c9b458cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774269"
---
# <a name="a_shainit-function"></a>\_Функция шаинит

Инициирует хэширование потока данных.

## <a name="syntax"></a>Синтаксис


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Контекст* \[ в, out\]
</dt> <dd>

Контекст SHA.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Эта функция очень похожа на Шаинит, но вызывается непосредственно из библиотеки, а не направляется через криптографическую инфраструктуру. дополнительные сведения см. в статье [Windows поставщики нткриптографик](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Библиотека<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
