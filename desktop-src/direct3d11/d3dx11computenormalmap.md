---
title: Функция D3DX11ComputeNormalMap (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Компутенормалмап.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- D3DX11ComputeNormalMap функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273894"
---
# <a name="d3dx11computenormalmap-function"></a>Функция D3DX11ComputeNormalMap

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

> [!Note]  
> Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **компутенормалмап**.

 

Преобразует карту высоты в обычную карту. Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекст* \[ окне\]
</dt> <dd>

Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Указатель на интерфейс [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) , представляющий текстуру исходной карты с высотой.

</dd> <dt>

*псрктекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Указатель на интерфейс [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , представляющий текстуру исходной карты с высотой.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Один или несколько \_ флагов НОРМАЛМАП D3DX, управляющих созданием обычных карт.

</dd> <dt>

*Канал* \[ связи окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Один \_ флаг канала D3DX, указывающий источник сведений о высоте.

</dd> <dt>

*Амплитуда* \[ окне\]
</dt> <dd>

Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

Коэффициент величины постоянного значения, увеличивающий (или уменьшающий) значения в нормальном сопоставлении. Более высокие значения обычно делают выпуклости более видимыми, а более низкие значения обычно делают невидимыми более выпуклости.

</dd> <dt>

*пдесттекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Указатель на интерфейс [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , представляющий текстуру назначения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может иметь следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Примечания

Этот метод рассчитывает нормальную работу, используя Центральное различие с размером ядра 3X3. Каналы RGB в назначении содержат смещенные компоненты (x, y, z) нормали. Центральный разностный знаменатель жестко закодирован в 2,0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

