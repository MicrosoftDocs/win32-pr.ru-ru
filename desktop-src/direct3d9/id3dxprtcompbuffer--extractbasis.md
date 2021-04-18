---
description: Извлекает средние и абстрактные векторы для заданного кластера из сжатого буфера данных ID3DXPRTCompBuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'Метод ID3DXPRTCompBuffer:: Екстрактбасис (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713797"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a>Метод ID3DXPRTCompBuffer:: Екстрактбасис

Извлекает средние и абстрактные векторы для заданного кластера из сжатого буфера данных [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Кластер* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Кластер, для которого будет извлечена эта базисная единица.

</dd> <dt>

*пклустербасис* \[ в, out\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на массив базисных данных вектора для кластера. Размер хранимых данных с плавающей запятой будет следующим: (1 + число векторов PCA на кластер) \* (количество коэффициентов) (количество \* цветовых каналов)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
