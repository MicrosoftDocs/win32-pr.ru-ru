---
title: Функция D3DX11SaveTextureToFile (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Каптуретекстуре затем Саветоксксксфиле (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Для упрощенного сценария создания снимка экрана из текстуры цели рендеринга рекомендуется использовать библиотеку Директкстк, Саведдстекстуретофиле или Савевиктекстуретофиле. Сохранение текстуры в файл.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- D3DX11SaveTextureToFile функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986990"
---
# <a name="d3dx11savetexturetofile-function"></a>Функция D3DX11SaveTextureToFile

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

> [!Note]  
> Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **каптуретекстуре** затем **саветоксксксфиле** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Для упрощенного сценария создания снимка экрана из текстуры цели рендеринга рекомендуется использовать библиотеку [директкстк](https://github.com/Microsoft/DirectXTK) , **саведдстекстуретофиле** или **савевиктекстуретофиле**.

 

Сохранение текстуры в файл.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pContext* 
</dt> <dd>

Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*псрктекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Указатель на текстуру, которую необходимо сохранить. См. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*Дестформат* \[ окне\]
</dt> <dd>

Тип: **[ **D3DX11 \_ image \_ File \_ Format**](d3dx11-image-file-format.md)**

Формат текстуры будет сохранен как (см. раздел [**\_ \_ \_ Формат файла изображения D3DX11**](d3dx11-image-file-format.md)). D3DX11 \_ одиночная \_ DDS — это предпочтительный формат, так как это единственный вариант, поддерживающий все форматы [**в \_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*пдестфиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Имя целевого выходного файла, в котором будет сохранена текстура. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае тип данных разрешается в LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md). Используйте возвращаемое значение, чтобы узнать, поддерживается ли *дестформат* .

## <a name="remarks"></a>Примечания

**D3DX11SaveTextureToFile** записывает дополнительную [**\_ \_ DXT10 структуру заголовков DDS**](/windows/desktop/direct3ddds/dds-header-dxt10) для текстуры ввода, только если это необходимо (например, поскольку текстура ввода имеет стандартный RGB-формат (sRGB)). Если **D3DX11SaveTextureToFile** записывает **\_ \_ DXT10 структуру заголовков DDS** , он устанавливает для текстуры **двфауркк** член в структуре [**\_ PIXELFORMAT DDS**](/windows/desktop/direct3ddds/dds-pixelformat) **, чтобы указать** содержимым DX10 в заголовке **DDS \_ \_ пресценсе** расширенный заголовок.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

