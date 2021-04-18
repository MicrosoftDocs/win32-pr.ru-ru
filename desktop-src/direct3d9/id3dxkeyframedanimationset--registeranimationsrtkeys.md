---
description: Зарегистрируйте данные опорного кадра шкалы, вращения и перевода (SRT) для анимации.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'Метод ID3DXKeyframedAnimationSet:: Регистераниматионсрткэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713943"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a>Метод ID3DXKeyframedAnimationSet:: Регистераниматионсрткэйс

Зарегистрируйте данные опорного кадра шкалы, вращения и перевода (SRT) для анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на имя анимации.

</dd> <dt>

*Нумскалекэйс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество ключей масштабирования.

</dd> <dt>

*Нумротатионкэйс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число ключей вращения.

</dd> <dt>

*Нумтранслатионкэйс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число ключей перевода.

</dd> <dt>

*пскалекэйс* \[ окне\]
</dt> <dd>

Тип: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Адрес указателя на выделенный пользователем массив векторов [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) , который метод заполняет данными масштабирования.

</dd> <dt>

*протатионкэйс* \[ окне\]
</dt> <dd>

Тип: **const [**LPD3DXKEY \_ кватернион**](d3dxkey-quaternion.md) \***

Адрес указателя на выделенный пользователем массив [**D3DXKEY \_ кватернион**](d3dxkey-quaternion.md) , который заполняется методом данными вращения.

</dd> <dt>

*птранслатионкэйс* \[ окне\]
</dt> <dd>

Тип: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Адрес указателя на выделенный пользователем массив [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) векторов, который заполняется методом данными перевода.

</dd> <dt>

*паниматиониндекс* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Возвращает индекс анимации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: Жетнумскалекэйс**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: Жетнумротатионкэйс**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: Жетнумтранслатионкэйс**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
