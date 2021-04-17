---
description: Возвращает Имеморибуффер в виде массива байтов.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'Метод Имеморибуффербитеакцесс:: with buffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711059"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a>Метод Имеморибуффербитеакцесс:: with buffer

Возвращает [**имеморибуффер**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) в виде массива байтов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Указатель на массив байтов, содержащий данные буфера.

</dd> <dt>

*емкость* \[ заполняет\]
</dt> <dd>

Число байтов в возвращаемом массиве

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

При вызове [**параметр memorybuffer:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) код, использующий этот буфер, должен установить указатель на *значение* null.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имеморибуффербитеакцесс**](/previous-versions//mt297505(v=vs.85))
</dt> </dl>

 

 
