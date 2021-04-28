---
description: Функция D3DXGetPixelShaderProfile — возвращает имя наивысшего профиля высокого уровня (HLSL), поддерживаемого данным устройством.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Функция D3DXGetPixelShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d24e19d49a8a96f91847892f519ef6c06d25ef5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114441"
---
# <a name="d3dxgetpixelshaderprofile-function"></a>Функция D3DXGetPixelShaderProfile

Возвращает имя высокоуровневого профиля языка шейдеров (HLSL), поддерживаемого данным устройством.

## <a name="syntax"></a>Синтаксис


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на устройство. См. [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Имя профиля HLSL.

Если устройство не поддерживает шейдеры пикселей, функция возвращает **значение NULL**.

## <a name="remarks"></a>Remarks

Профиль шейдера указывает версию шейдера сборки для использования и возможности, доступные компилятору HLSL при компиляции шейдера. В следующей таблице перечислены поддерживаемые профили шейдера пикселей.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Профиль шейдера</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ps_1_1</td>
<td>Компилировать до ps_1_1 версии.</td>
</tr>
<tr class="even">
<td>ps_1_2</td>
<td>Компилировать до ps_1_2 версии.</td>
</tr>
<tr class="odd">
<td>ps_1_3</td>
<td>Компилировать до ps_1_3 версии.</td>
</tr>
<tr class="even">
<td>ps_1_4</td>
<td>Компилировать до ps_1_4 версии.</td>
</tr>
<tr class="odd">
<td>ps_2_0</td>
<td>Компилировать до ps_2_0 версии.</td>
</tr>
<tr class="even">
<td>ps_2_a</td>
<td>То же, что и профиль ps_2_0, со следующими дополнительными возможностями, доступными для целевого компилятора:
<ul>
<li>Количество временных регистров (r #) больше или равно 22.</li>
<li>Произвольный источник свиззле.</li>
<li>Инструкции по градиенту: ДСКС, ДСИ.</li>
<li>Затенения.</li>
<li>Нет ограничения на чтение зависимой текстуры.</li>
<li>Нет ограничений на количество инструкций текстуры.</li>
</ul></td>
</tr>
<tr class="odd">
<td>ps_2_b</td>
<td>То же, что и профиль ps_2_0, со следующими дополнительными возможностями, доступными для целевого компилятора:
<ul>
<li>Количество временных регистров (r #) больше или равно 32.</li>
<li>Нет ограничений на количество инструкций текстуры.</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_3_0</td>
<td>Компилировать до ps_3_0 версии.</td>
</tr>
</tbody>
</table>



 

Дополнительные сведения о различиях между версиями шейдера см. в разделе [различия шейдеров пикселей](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
