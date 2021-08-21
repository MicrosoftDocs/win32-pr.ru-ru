---
title: Метод ID3DX11EffectShaderVariable Жетвертексшадер (D3dx11effect. h)
description: Получение шейдера вершин.
ms.assetid: 31a250ae-154b-43ce-97e3-6480f23dc4e2
keywords:
- Метод Жетвертексшадер Direct3D 11
- Метод Жетвертексшадер Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетвертексшадер
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetVertexShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f6fa74c19c764e70239623ea0bb239ebf822439be5fb2e640eb7e4085c6ce2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533012"
---
# <a name="id3dx11effectshadervariablegetvertexshader-method"></a>Метод ID3DX11EffectShaderVariable:: Жетвертексшадер

Получение шейдера вершин.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetVertexShader(
   UINT               ShaderIndex,
   ID3D11VertexShader **ppVS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*шадериндекс* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый с нуля индекс.

</dd> <dt>

*ппвс* 
</dt> <dd>

Тип: **[ **ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader)\*\***

Указатель на указатель [**ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader) , для которого будет задан шейдер вершин при возврате.

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

 

