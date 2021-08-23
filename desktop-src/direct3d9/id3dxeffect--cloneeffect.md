---
description: Создает копию результата.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'Метод ID3DXEffect:: Клониффект (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ab5ebe2898c1525d3a539121d1e57708c4713df3a06b43bfa41572f0e7b23b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494264"
---
# <a name="id3dxeffectcloneeffect-method"></a>Метод ID3DXEffect:: Клониффект

Создает копию результата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с этим действием.

</dd> <dt>

*ппеффект* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Указатель на интерфейс [**ID3DXEffect**](id3dxeffect.md) , содержащий клонированный результат.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

> [!Note]  
> Эта функция не будет клонировать результат, если пользователь указывает, что [D3DXFX \_ не может \_ клонироваться](d3dxfx.md) во время создания результата.

 

Сведения об обновлении общих и необщих параметров в активном методе клонированного результата см. в разделе [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
