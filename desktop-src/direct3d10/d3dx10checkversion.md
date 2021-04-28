---
description: Функция D3DX10CheckVersion. Убедитесь, что версия D3DX, которая была скомпилирована с помощью, является версией, которую вы используете.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Функция D3DX10CheckVersion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fc8befa88fb706965a30224843745b033ea205b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105352"
---
# <a name="d3dx10checkversion-function"></a>Функция D3DX10CheckVersion

Убедитесь, что версия D3DX, которая была скомпилирована с помощью, — это версия, которую вы используете.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*D3DSdkVersion* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Используйте \_ версию пакета SDK для D3D10 \_ . См. примечания.

</dd> <dt>

*D3DX10SdkVersion* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Используйте \_ версию пакета SDK для D3DX10 \_ . См. примечания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если версия не совпадает, функция возвратит значение FALSE (число меньше или равно 0, само число не имеет смысла).

## <a name="remarks"></a>Remarks

Используйте эту функцию во время инициализации приложения.


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
