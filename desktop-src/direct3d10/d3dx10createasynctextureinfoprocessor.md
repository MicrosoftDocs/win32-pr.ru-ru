---
description: Функция D3DX10CreateAsyncTextureInfoProcessor. Создайте обработчик данных, который будет использоваться в конвейере потоков.
ms.assetid: e97b6aca-1839-48ea-8dab-b96a52ec2a68
title: Функция D3DX10CreateAsyncTextureInfoProcessor (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureInfoProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 861404127cebf23954ef340d8e92441bfdaec204418add85a5b4dfabcaea17dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852354"
---
# <a name="d3dx10createasynctextureinfoprocessor-function"></a>Функция D3DX10CreateAsyncTextureInfoProcessor

Создайте обработчик данных, который будет использоваться в [**конвейере потоков**](id3dx10threadpump.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateAsyncTextureInfoProcessor(
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*плоадинфо* \[ окне\]
</dt> <dd>

Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***

Необязательный элемент. Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.

</dd> <dt>

*ппдатапроцессор* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Этот API создает интерфейс процессора данных; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) создает интерфейс процессора данных и загружает текстуру.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции текстуры в D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




