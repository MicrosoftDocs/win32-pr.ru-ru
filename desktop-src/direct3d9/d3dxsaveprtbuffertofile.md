---
description: Сохраняет предварительно вычисленный буфер радианценой пересылки (PRT) на диск.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Функция D3DXSavePRTBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfa3d06970d138ff1c868403c20bb41cf14f0a5cbb7116cbe0f0843a51258dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524534"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>Функция D3DXSavePRTBufferToFile

Сохраняет предварительно вычисленный буфер радианценой пересылки (PRT) на диск.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>Параметры

*пфиленаме* \[ окне\]

Тип: **[LPCSTR](../winprog/windows-data-types.md)**

Имя файла, в который будет сохранен буфер.

*pBuffer* \[ окне\]

Тип: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

Адрес указателя на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="return-value"></a>Возвращаемое значение

Тип: **[HRESULT](../com/structure-of-com-error-codes.md)**

Если метод выполнен успешно, возвращается значение **D3D \_ ОК**. В случае сбоя метода возвращаемое значение может быть **D3DERR \_ инвалидкалл**.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в [D3DXSavePRTBufferToFileW](). В противном случае вызов функции разрешается в **D3DXSavePRTBufferToFileA**.

Формат файла PRT представляет собой двоичный файл в виде заголовка, а затем блок данных.

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

В случае, если *бистекс* не равен нулю, *нумсамплес* должен равняться `TexWidth * TexHeight` .

Блок данных, следующий за заголовком, — это `NumSamples * NumCoeffs * NumChannels * sizeof(float)` байты.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>См. также раздел

[Предварительно вычисленные функции пересылки Радианце](dx9-graphics-reference-d3dx-functions-prt.md)
