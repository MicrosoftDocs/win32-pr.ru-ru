---
description: Получение диспетчера состояний эффектов.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'Метод ID3DXEffect:: Жетстатеманажер (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703704"
---
# <a name="id3dxeffectgetstatemanager-method"></a>Метод ID3DXEffect:: Жетстатеманажер

Получение диспетчера состояний эффектов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппманажер* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***

Возвращает указатель на диспетчер состояний. См. [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Комментарии

[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) — это реализованный пользователем интерфейс, который обеспечивает обратные вызовы в приложение для установки состояния устройства с самого влияния.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: Сетстатеманажер**](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




