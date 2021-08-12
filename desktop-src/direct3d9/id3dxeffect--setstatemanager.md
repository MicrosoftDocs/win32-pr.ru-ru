---
description: Задайте диспетчер состояний эффектов.
ms.assetid: 87409687-03f1-4593-ae58-3a8ba08e592b
title: 'Метод ID3DXEffect:: Сетстатеманажер (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 06b6a7404f664e8ec18247b2eda57c5097cd575a3556853bfe8a9eb67705d071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295907"
---
# <a name="id3dxeffectsetstatemanager-method"></a>Метод ID3DXEffect:: Сетстатеманажер

Задайте диспетчер состояний эффектов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetStateManager(
  [in] LPD3DXEFFECTSTATEMANAGER pManager
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пманажер* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**

Указатель на диспетчер состояний. См. [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) — это реализованный пользователем интерфейс, который обеспечивает обратные вызовы в приложение для установки состояния устройства с самого влияния.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: Жетстатеманажер**](id3dxeffect--getstatemanager.md)
</dt> </dl>

 

 




