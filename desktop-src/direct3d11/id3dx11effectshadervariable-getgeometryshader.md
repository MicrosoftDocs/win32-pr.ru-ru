---
title: Метод ID3DX11EffectShaderVariable Жетжеометришадер (D3dx11effect. h)
description: Получение шейдера Geometry.
ms.assetid: 395d5c92-a941-4fbf-9bb9-b43634c1810b
keywords:
- Метод Жетжеометришадер Direct3D 11
- Метод Жетжеометришадер Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетжеометришадер
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetGeometryShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77bd190566fbc4e699e087b0203c2f42b697bb1ab0f5dd30d7ec4659367ebd63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565914"
---
# <a name="id3dx11effectshadervariablegetgeometryshader-method"></a>Метод ID3DX11EffectShaderVariable:: Жетжеометришадер

Получение шейдера Geometry.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGeometryShader(
   UINT                 ShaderIndex,
   ID3D11GeometryShader **ppGS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*шадериндекс* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый с нуля индекс.

</dd> <dt>

*ппгс* 
</dt> <dd>

Тип: **[ **ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***

Указатель на указатель [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) , для которого будет задан шейдер Geometry при возврате.

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

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

