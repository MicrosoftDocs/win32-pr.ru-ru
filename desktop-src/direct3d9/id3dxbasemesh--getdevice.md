---
description: Извлекает устройство, связанное с сеткой.
ms.assetid: 16ff5267-0c64-4c3d-925d-6fc10f54c9c4
title: Метод ID3DXBaseMesh::-Device (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53870ab3d0de46a90dcca8f9c90e9ad94d762a835a93e0843af0f03cdc344386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893654"
---
# <a name="id3dxbasemeshgetdevice-method"></a>Метод ID3DXBaseMesh:: of Device

Извлекает устройство, связанное с сеткой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдевице* \[ out, retval\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства Direct3D, связанный с сеткой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Не забудьте вызвать [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , когда вы завершите работу с этим интерфейсом **IDirect3DDevice9** , или у вас будет утечка памяти.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
