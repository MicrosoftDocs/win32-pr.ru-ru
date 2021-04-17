---
description: Сохранение текстуры в файл.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Функция D3DX10SaveTextureToFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694356"
---
# <a name="d3dx10savetexturetofile-function"></a>Функция D3DX10SaveTextureToFile

Сохранение текстуры в файл.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
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

Формат текстуры будет сохранен как (см. раздел [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md)). D3DX10 \_ одиночная \_ DDS — это предпочтительный формат, так как это единственный вариант, поддерживающий все форматы [**в \_ формате DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*пдестфиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Имя целевого выходного файла, в котором будет сохранена текстура. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае тип данных разрешается в LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md). Используйте возвращаемое значение, чтобы узнать, поддерживается ли *дестформат* .

## <a name="remarks"></a>Комментарии

**D3DX10SaveTextureToFile** записывает дополнительную [**\_ \_ DXT10 структуру заголовков DDS**](../direct3ddds/dds-header-dxt10.md) для текстуры ввода, только если это необходимо (например, поскольку текстура ввода имеет стандартный RGB-формат (sRGB)). Если **D3DX10SaveTextureToFile** записывает **\_ \_ DXT10 структуру заголовков DDS** , он устанавливает для текстуры **двфауркк** член в структуре [**\_ PIXELFORMAT DDS**](../direct3ddds/dds-pixelformat.md) **, чтобы указать** содержимым DX10 в заголовке **DDS \_ \_ пресценсе** расширенный заголовок.

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

 

 
