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
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694134"
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

## <a name="remarks"></a>Комментарии

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

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>См. также раздел

[Предварительно вычисленные функции пересылки Радианце](dx9-graphics-reference-d3dx-functions-prt.md)
