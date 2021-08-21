---
description: Сохраняет сжатый предварительно вычисленный радианце передаваемой (PRT) буфер на диск.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Функция D3DXSavePRTCompBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a62bd164ce8eb8175c62658b19dd5ce6282d6c75b081db45f8b0af4994322579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524514"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>Функция D3DXSavePRTCompBufferToFile

Сохраняет сжатый предварительно вычисленный радианце передаваемой (PRT) буфер на диск.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Параметры

*пфиленаме* \[ окне\]

Тип: **[LPCSTR](../winprog/windows-data-types.md)**

Имя файла, в который будет сохранен сжатый буфер.

*pBuffer* \[ окне\]

Тип: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Адрес указателя на входной объект [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

## <a name="return-value"></a>Возвращаемое значение

Тип: **[HRESULT](../com/structure-of-com-error-codes.md)**

Если метод выполнен успешно, возвращается значение **D3D \_ ОК**. В случае сбоя метода возвращаемое значение может быть **D3DERR \_ инвалидкалл**.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в [D3DXSavePRTCompBufferToFileW](). В противном случае вызов функции разрешается в **D3DXSavePRTCompBufferToFileA**.

Формат файла PCA представляет собой двоичный файл в виде заголовка, а затем два или три блока данных.

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

В случае, если *бистекс* не равен нулю, *нумсамплес* должен равняться `TexWidth * TexHeight` .

Базовый блок данных, следующий за заголовком, — это `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` байты.

Ниже приведен блок данных веса PCA, который представляет собой `NumPCA * NumSamples * sizeof(float)` байты.

Если *нумклустерс* больше 1, то файл заканчивается блоком данных идентификаторов кластеров (байт) `NumSamples * sizeof(UINT)` .

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>См. также

[Предварительно вычисленные функции пересылки Радианце](dx9-graphics-reference-d3dx-functions-prt.md)
