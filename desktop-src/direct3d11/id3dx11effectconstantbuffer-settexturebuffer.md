---
title: Метод ID3DX11EffectConstantBuffer Сеттекстуребуффер (D3dx11effect. h)
description: Задайте буфер текстуры.
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- Метод Сеттекстуребуффер Direct3D 11
- Метод Сеттекстуребуффер Direct3D 11, интерфейс ID3DX11EffectConstantBuffer
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, метод Сеттекстуребуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736ec4c5f0125dfc37925d67875cf97c5441117c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986834"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a>Метод ID3DX11EffectConstantBuffer:: Сеттекстуребуффер

Задайте буфер текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуребуффер* 
</dt> <dd>

Тип: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***

Указатель на интерфейс представления шейдера-ресурса для доступа к буферу текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Примечания

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





