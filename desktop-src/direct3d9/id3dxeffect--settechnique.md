---
description: Задает активный метод.
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: 'Метод ID3DXEffect:: Сеттечникуе (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7b10190df7c4527535a35c2c352933ec652452d51804e23b8aad338e6ca40522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987552"
---
# <a name="id3dxeffectsettechnique-method"></a>Метод ID3DXEffect:: Сеттечникуе

Задает активный метод.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хтечникуе* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный описатель для метода. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




