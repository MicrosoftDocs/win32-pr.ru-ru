---
description: Заполняет массив данными ключа, используемыми для анимации ключевых кадров.
ms.assetid: ecb791ad-e586-4057-9239-facd37a47637
title: 'Метод ID3DXKeyframedAnimationSet:: Жеттранслатионкэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39b2c086442b6a235730f9ec228b377f0a8b8f39a83d7c5043cfbca56dae2345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987364"
---
# <a name="id3dxkeyframedanimationsetgettranslationkeys-method"></a>Метод ID3DXKeyframedAnimationSet:: Жеттранслатионкэйс

Заполняет массив данными ключа, используемыми для анимации ключевых кадров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTranslationKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pTranslationKeys
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Анимация* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс анимации.

</dd> <dt>

*птранслатионкэйс* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Указатель на выделенный пользователем массив векторов [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) , который метод должен заполнять данными преобразования анимации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: Жетнумтранслатионкэйс**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
