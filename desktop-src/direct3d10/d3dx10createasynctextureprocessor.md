---
description: Функция D3DX10CreateAsyncTextureProcessor. Создайте обработчик данных, который будет использоваться в конвейере потоков.
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Функция D3DX10CreateAsyncTextureProcessor (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e75ab6b796f23399b453a6c7eebfe0d40e3b7b49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102792"
---
# <a name="d3dx10createasynctextureprocessor-function"></a>Функция D3DX10CreateAsyncTextureProcessor

Создайте обработчик данных, который будет использоваться в [**конвейере потоков**](id3dx10threadpump.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Указатель на девиве (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).

</dd> <dt>

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

Этот API создает интерфейс процессора данных и загружает текстуру. [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) создает интерфейс процессора данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции текстуры в D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




