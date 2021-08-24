---
description: Функция D3DXGetVertexShaderProfile — возвращает имя наивысшего профиля высокого уровня (HLSL), поддерживаемого данным устройством.
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
ms.openlocfilehash: e5c646fb9779ca923480487cb96f184c76eff9ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473630"
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




| Профиль шейдера | Описание | 
|----------------|-------------|
| vs_1_1 | Компилировать до vs_1_1 версии. | 
| vs_2_0 | Компилировать до vs_2_0 версии. | 
| vs_2_a | То же, что и профиль vs_2_0, со следующими дополнительными возможностями, доступными для целевого компилятора:<ul><li>Количество временных регистров (r #) больше или равно 13.</li><li>Динамическая Инструкция по управлению потоком.</li><li>Затенения.</li></ul> | 
| vs_3_0 | Компилировать до vs_3_0 версии. | 




 

Дополнительные сведения о различиях между версиями шейдера см. в разделе [различия шейдеров вершин](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
