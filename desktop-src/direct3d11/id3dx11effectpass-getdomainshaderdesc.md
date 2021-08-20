---
title: Метод ID3DX11EffectPass Жетдомаиншадердеск (D3dx11effect. h)
description: Получите описание шейдера домена.
ms.assetid: 02109930-0922-46b8-9381-bb75abd0c4a0
keywords:
- Метод Жетдомаиншадердеск Direct3D 11
- Метод Жетдомаиншадердеск Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Жетдомаиншадердеск
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDomainShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f61de7dd44d19cb57390adf7829766fc4bffcff82bf1019b3dae1e2979ae37ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046022"
---
# <a name="id3dx11effectpassgetdomainshaderdesc-method"></a>Метод ID3DX11EffectPass:: Жетдомаиншадердеск

Получите описание шейдера домена.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDomainShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдеск* 
</dt> <dd>

Тип: **[ **D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***

Указатель на описание области шейдера домена (см. раздел [**D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)).

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





