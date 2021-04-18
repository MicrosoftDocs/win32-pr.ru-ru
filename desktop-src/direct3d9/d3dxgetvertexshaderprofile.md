---
description: Возвращает имя высокоуровневого профиля языка шейдеров (HLSL), поддерживаемого данным устройством.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Функция D3DXGetVertexShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713661"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>Функция D3DXGetVertexShaderProfile

Возвращает имя высокоуровневого профиля языка шейдеров (HLSL), поддерживаемого данным устройством.

## <a name="syntax"></a>Синтаксис


```C++
LPCSTR D3DXGetVertexShaderProfile(
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

Если устройство не поддерживает шейдеры вершин, функция возвращает **значение NULL**.

## <a name="remarks"></a>Комментарии

Профиль шейдера указывает версию шейдера сборки для использования и возможности, доступные компилятору HLSL при компиляции шейдера. В следующей таблице перечислены поддерживаемые профили шейдеров вершин.



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
<td>vs_1_1</td>
<td>Компилировать до vs_1_1 версии.</td>
</tr>
<tr class="even">
<td>vs_2_0</td>
<td>Компилировать до vs_2_0 версии.</td>
</tr>
<tr class="odd">
<td>vs_2_a</td>
<td>То же, что и профиль vs_2_0, со следующими дополнительными возможностями, доступными для целевого компилятора:
<ul>
<li>Количество временных регистров (r #) больше или равно 13.</li>
<li>Динамическая Инструкция по управлению потоком.</li>
<li>Затенения.</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_3_0</td>
<td>Компилировать до vs_3_0 версии.</td>
</tr>
</tbody>
</table>



 

Дополнительные сведения о различиях между версиями шейдера см. в разделе [различия шейдеров вершин](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
