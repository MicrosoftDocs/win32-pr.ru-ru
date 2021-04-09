---
description: Извлекает ПРОПВАРИАНТ и входную строку, представляющую фрагмент данных. Вызов этого метода аналогичен вызову GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'Метод Ириччунк:: Ремотежетдата'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144035"
---
# <a name="irichchunkremotegetdata-method"></a>Метод Ириччунк:: Ремотежетдата

Извлекает [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) и входную строку, представляющую фрагмент данных. Вызов этого метода аналогичен вызову [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфирстпос* \[ заполняет\]
</dt> <dd>

Получает начальную точку диапазона (с отсчетом от нуля). Этот параметр может принимать значение **NULL**.

</dd> <dt>

*пленгс* \[ заполняет\]
</dt> <dd>

Получает длину диапазона. Этот параметр может принимать значение **NULL**.

</dd> <dt>

*ппсз* \[ заполняет\]
</dt> <dd>

Получает связанное строковое значение Юникода или **значение NULL** , если оно недоступно.

</dd> <dt>

*pValue* \[ заполняет\]
</dt> <dd>

Получает связанное значение [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) или **VT \_ Empty** , если оно недоступно. Этот параметр может принимать значение **NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ириччунк**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
