---
description: Включает или отключает запись в контроллере анимации.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'Метод ID3DXAnimationController:: Сеттраккенабле (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081916"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a>Метод ID3DXAnimationController:: Сеттраккенабле

Включает или отключает запись в контроллере анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор смешанной записи.

</dd> <dt>

*Включить* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Включить значение. Задайте значение **true** , чтобы включить эту запись в контроллере, или **значение false** , чтобы предотвратить смешанный режим.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Для смешивания дорожек с другими дорожками флаг enable должен иметь значение **true**. И наоборот, установка флага в **значение false** предотвратит смешение дорожки с другими дорожками.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
