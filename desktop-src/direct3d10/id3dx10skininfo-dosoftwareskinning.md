---
description: Выпустить программное обеспечение на массиве вершин.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: 'ID3DX10SkinInfo: метод:D Ософтварескиннинг (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20f68f51d6886d53d74cd31691e52c362c60d2bf9be2beb0656564cb20fcb80a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729814"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>ID3DX10SkinInfo: метод:D Ософтварескиннинг

Выпустить программное обеспечение на массиве вершин.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Стартвертекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс в Псрквертицес.

</dd> <dt>

*Вертекскаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число вершин для преобразования.

</dd> <dt>

*псрквертицес* \[ окне\]
</dt> <dd>

Тип: **void \***

Указатель на массив вершин для преобразования.

</dd> <dt>

*Сркстриде* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Размер (в байтах) вершины в Псрквертицес.

</dd> <dt>

*пдествертицес* \[ в, out\]
</dt> <dd>

Тип: **void \***

Указатель на массив вершин, который будет заполнен преобразованными вершинами.

</dd> <dt>

*Дестстриде* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Размер (в байтах) вершины в Пдествертицес.

</dd> <dt>

*пбонематрицес* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Массив матриц, который будет использоваться для преобразования точек, сопоставленных с каждой костью, например, если вершины, сопоставленные с костью i, будут преобразованы \[ \] с помощью пбонематрицес \[ i \] . Этот массив будет использоваться для преобразования матриц, только если значение "IsFalse" в Пчаннелдескс равно **false**, в противном случае будет использоваться пинверсетранспосебонематрицес.

</dd> <dt>

*пинверсетранспосебонематрицес* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Если это значение равно **null**, оно будет установлено равным пбонематрицес. Этот массив матриц будет использоваться для преобразования вершин только в том случае, если значение IsTrue в Пчаннелдескс равно **true**, в противном случае будет использоваться пбонематрицес.

</dd> <dt>

*пчаннелдескс* \[ окне\]
</dt> <dd>

Тип: **[ **\_ \_ канал обложки D3DX10**](d3dx10-skinning-channel.md)\***

Указатель на \_ структуру каналов обложки D3DX10 \_ , которая определяет член decl, на котором будет выполняться Обложка по.

</dd> <dt>

*Нумчаннелс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число \_ структур каналов обложки D3DX10 \_ в пчаннелдескс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается со сбоем, возвращаемое значение может быть следующим: E \_ INVALIDARG.

## <a name="remarks"></a>Remarks

Ниже приведен пример использования программных описаний.


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
