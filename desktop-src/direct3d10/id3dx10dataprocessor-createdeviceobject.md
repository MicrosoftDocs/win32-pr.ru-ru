---
description: Создайте объект устройства.
ms.assetid: 5b9b00de-c744-43c7-b383-1d3358c80741
title: 'Метод ID3DX10DataProcessor:: Креатедевицеобжект (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.CreateDeviceObject
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca20de85e867cc8c444f05ea187fb314a6b983ad8c72a5f8ae921c0747bd9ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540422"
---
# <a name="id3dx10dataprocessorcreatedeviceobject-method"></a>Метод ID3DX10DataProcessor:: Креатедевицеобжект

Создайте объект устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдатаобжект* \[ заполняет\]
</dt> <dd>

Тип: **void \* \***

Адрес указателя на созданный объект устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10DataProcessor](id3dx10dataprocessor.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




