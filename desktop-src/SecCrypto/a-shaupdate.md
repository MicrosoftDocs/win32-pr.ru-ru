---
description: Добавляет данные в указанный хэш-объект.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: Функция A_SHAUpdate (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 103438e3ef0747aa6170848398621b0246bd15366be4d1171ce5735942011007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101074"
---
# <a name="a_shaupdate-function"></a>\_Функция шаупдате

Добавляет данные в указанный хэш-объект.

## <a name="syntax"></a>Синтаксис


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Контекст* \[ в, out\]
</dt> <dd>

Контекст SHA.

</dd> <dt>

*Буфер* \[ заполняет\]
</dt> <dd>

Хэш-таблица.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Размер буфера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Эту функцию можно вызывать несколько раз, чтобы вычислить хэш для длинных потоков данных или ненепрерывных потоков данных. Перед получением хэш-значения необходимо вызвать функцию [**\_ шафинал**](a-shafinal.md) .

Эта функция очень похожа на Шаупдате, но вызывается непосредственно из библиотеки, а не направляется через криптографическую инфраструктуру. дополнительные сведения см. в статье [Windows поставщики нткриптографик](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Библиотека<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
