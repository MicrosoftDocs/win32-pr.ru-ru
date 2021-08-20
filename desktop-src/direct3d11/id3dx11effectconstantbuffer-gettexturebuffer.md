---
title: Метод ID3DX11EffectConstantBuffer Жеттекстуребуффер (D3dx11effect. h)
description: Получение буфера текстуры.
ms.assetid: 8d09e67c-358e-49ee-8ca4-e1f548b52c3a
keywords:
- Метод Жеттекстуребуффер Direct3D 11
- Метод Жеттекстуребуффер Direct3D 11, интерфейс ID3DX11EffectConstantBuffer
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, метод Жеттекстуребуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea492e15612e5d4a0533ac6b811a60097136560480216979d36306d18761de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046432"
---
# <a name="id3dx11effectconstantbuffergettexturebuffer-method"></a>Метод ID3DX11EffectConstantBuffer:: Жеттекстуребуффер

Получение буфера текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTextureBuffer(
   ID3D11ShaderResourceView **ppTextureBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пптекстуребуффер* 
</dt> <dd>

Тип: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Адрес указателя на интерфейс представления шейдера-ресурса для доступа к буферу текстуры. См. [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





