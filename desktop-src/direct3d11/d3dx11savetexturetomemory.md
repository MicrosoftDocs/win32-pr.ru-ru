---
title: Функция D3DX11SaveTextureToMemory (D3DX11tex. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Каптуретекстуре затем Саветоксксксмемори (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Сохранение текстуры в памяти.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- D3DX11SaveTextureToMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8459b9652701110a27efa88cf75d1bd5eb9214f72e860a5a80c18d0fa6292ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124569"
---
# <a name="d3dx11savetexturetomemory-function"></a>Функция D3DX11SaveTextureToMemory

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.

 

> [!Note]  
> Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **каптуретекстуре** затем **саветоксксксмемори** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр).

 

Сохранение текстуры в памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
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

Формат текстуры будет сохранен как. См. раздел [**\_ \_ \_ Формат файла изображения D3DX11**](d3dx11-image-file-format.md).

</dd> <dt>

*ппдестбуф* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***

Адрес указателя на память, содержащую сохраненную текстуру.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Необязательный элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

