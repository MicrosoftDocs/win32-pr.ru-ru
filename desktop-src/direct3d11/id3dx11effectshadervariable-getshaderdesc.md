---
title: Метод ID3DX11EffectShaderVariable Жетшадердеск (D3dx11effect. h)
description: Получение описания шейдера.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- Метод Жетшадердеск Direct3D 11
- Метод Жетшадердеск Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетшадердеск
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c76730d1ad5f3de35e273034d3a17beb71fb7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987104"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a>Метод ID3DX11EffectShaderVariable:: Жетшадердеск

Получение описания шейдера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*шадериндекс* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый с нуля индекс.

</dd> <dt>

*пдеск* 
</dt> <dd>

Тип: **[ **D3DX11 \_ Effect \_ Shader \_ DESC**](d3dx11-effect-shader-desc.md)\***

Указатель на описание шейдера (см. [**D3DX11 \_ Effect \_ Shader \_ DESC**](d3dx11-effect-shader-desc.md)).

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

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

