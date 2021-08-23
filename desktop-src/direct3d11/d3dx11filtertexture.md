---
title: Функция D3DX11FilterTexture (D3DX11tex. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Женератемипмапс и GenerateMipMaps3D. Создает цепочку mipmap с помощью определенного фильтра текстуры.
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- D3DX11FilterTexture функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 728f76a28a2d97d3e6789a35c2f375d964d331c607c7570e44aa44a17ccbaa8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124699"
---
# <a name="d3dx11filtertexture-function"></a>Функция D3DX11FilterTexture

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.

 

> [!Note]  
> Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **женератемипмапс** и **GenerateMipMaps3D**.

 

Создает цепочку mipmap с помощью определенного фильтра текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pContext* 
</dt> <dd>

Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*птекстуре* 
</dt> <dd>

Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Объект текстуры для фильтрации. См. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*срклевел* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Уровень mipmap, данные которого используются для создания оставшейся части цепочки mipmap.

</dd> <dt>

*мипфилтер* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Флаги, управляющие фильтрацией каждого миплевел (или D3DX11 \_ по умолчанию для \_ \_ линейного фильтра D3DX11). См [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md).

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

 

