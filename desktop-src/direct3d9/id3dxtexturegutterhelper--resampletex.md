---
description: Ресамплинг текстуры в гуттерхелпер параметризации.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'Метод ID3DXTextureGutterHelper:: Ресамплетекс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7d3afe8155eb33a37b30abcfc96aae83c0a96461c1ee2dd6118a671701cfed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800323"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>Метод ID3DXTextureGutterHelper:: Ресамплетекс

Ресамплинг текстуры в гуттерхелпер параметризации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуреин* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Текстура, соответствующая исходной параметризации в Пмешин. Эта текстура будет использоваться для создания Птекстуреаут.

</dd> <dt>

*пмешин* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Сетка, содержащая исходную и новую параметризации. Необходимо сохранить новую параметризацию в D3DDECLUSAGE \_ текскурд с индексом 0.

</dd> <dt>

*Использование* \[ окне\]
</dt> <dd>

Тип: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Использование данных вершин (используется в сочетании с Усажеиндекс), которое определяет компонент объявления вершины, который содержит исходную параметризацию в Пмешин. См. [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*Усажеиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс (используется в сочетании с использованием), который определяет компонент объявления вершины, который содержит исходную параметризацию параметров в Пмешин. \_Для новой параметризации требуется сочетание D3DDECLUSAGE текскурд и индекса 0; может использоваться любая другая комбинация использования или индекса.

</dd> <dt>

*птекстуреаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Перевыборка текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Параметризация в случае этой функции представляет собой набор координат текстуры, который сопоставляет треугольники сетки с треугольниками на текстуре. Новая параметризация — это набор координат текстуры, содержащихся в вспомогательном интерфейсе переплета, а исходная параметризация — это набор координат текстуры, содержащихся во входной сетке.

Предполагается, что координаты текстуры находятся в диапазоне от 0 до 1 включительно, а новая параметризация должна быть объявлена в объявлении вершины в качестве индекса координаты текстуры 0. Исходная текстура и текстура с интерполяцией должны иметь одинаковую ширину и высоту.

Например, для подготовки к повторной выборки текстуры:

-   Создайте исходный интерфейс текстуры (Поригиналтекс ниже) с помощью функции, такой как [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).
-   Создайте новый интерфейс текстуры для текстуры с интерполяцией (Пресампледтекс ниже). Размер этой текстуры должен соответствовать размеру (ширине и высоте) вспомогательной текстуры переплета.
-   Вызовите [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) , чтобы получить новую параметризацию, как показано ниже:


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



Одним из распространенных сценариев может быть использование Уватлас для создания текстуры Atlas и последующее использование Ресамплетекс для повторной выборки текстуры в новой параметризации. Дополнительные сведения о атласов см. [в разделе Использование уватлас (Direct3D 9)](using-uvatlas.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)
</dt> </dl>

 

 
