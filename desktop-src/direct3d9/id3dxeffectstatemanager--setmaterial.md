---
description: Функция обратного вызова, которая должна быть реализована пользователем для задания состояния материала.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'Метод ID3DXEffectStateManager:: Сетматериал (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694208"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a>Метод ID3DXEffectStateManager:: Сетматериал

Функция обратного вызова, которая должна быть реализована пользователем для задания состояния материала.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пматериал* \[ окне\]
</dt> <dd>

Тип: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***

Указатель на состояние материала. См. [**D3DMATERIAL9**](d3dmaterial9.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Метод, реализуемый пользователем, должен возвращать значение S \_ ОК. Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.

-   При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.
-   Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетматериал**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) завершится ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
