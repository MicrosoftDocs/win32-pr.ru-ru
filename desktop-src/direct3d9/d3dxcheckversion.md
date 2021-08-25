---
description: Функция D3DXCheckVersion. Убедитесь, что версия D3DX, которая была скомпилирована с помощью, является версией, которую вы используете.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Функция D3DXCheckVersion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26831f3a1a5f08494a7382cd412c30dcd24c1482c01dca684962a580068d380d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894124"
---
# <a name="d3dxcheckversion-function"></a>Функция D3DXCheckVersion

Убедитесь, что версия D3DX, которая была скомпилирована с помощью, — это версия, которую вы используете.

## <a name="syntax"></a>Синтаксис


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*D3DSDKVersion* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Используйте \_ версию пакета SDK для D3D \_ . См. примечания.

</dd> <dt>

*D3DXSDKVersion* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Используйте \_ версию пакета SDK для D3DX \_ . См. примечания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Возвращает **значение true** , если версия D3DX, с которой выполнялась компиляция, является версией, с которой вы работаете; в противном случае возвращается **значение false** .

## <a name="remarks"></a>Remarks

Используйте эту функцию во время инициализации приложения следующим образом:


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



Используйте [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) , чтобы убедиться, что установлена правильная среда выполнения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции общего назначения](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
