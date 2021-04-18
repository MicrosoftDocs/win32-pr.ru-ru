---
description: Сохранение текстуры в памяти.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: Функция D3DX10SaveTextureToMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694176"
---
# <a name="d3dx10savetexturetomemory-function"></a>Функция D3DX10SaveTextureToMemory

Сохранение текстуры в памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псрктекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Указатель на текстуру, которую необходимо сохранить. См. раздел [**интерфейс ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*Дестформат* \[ окне\]
</dt> <dd>

Тип: **[ **D3DX10 \_ image \_ File \_ Format**](d3dx10-image-file-format.md)**

Формат текстуры будет сохранен как. См. раздел [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md).

</dd> <dt>

*ппдестбуф* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Адрес указателя на память, содержащую сохраненную текстуру. См. раздел [**интерфейс ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Необязательный элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
