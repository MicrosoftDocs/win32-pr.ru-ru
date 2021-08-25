---
title: Метод ID3DX11EffectTechnique Компутестатеблоккмаск (D3dx11effect. h)
description: Вычислите маску блока состояния, чтобы разрешить или запретить изменение состояния.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Метод Компутестатеблоккмаск Direct3D 11
- Метод Компутестатеблоккмаск Direct3D 11, интерфейс ID3DX11EffectTechnique
- Интерфейс ID3DX11EffectTechnique Direct3D 11, метод Компутестатеблоккмаск
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7a221cd685eb31b068ae6144514adb70ffa42c654d9e1a3249db5302e0aa6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894764"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a>Метод ID3DX11EffectTechnique:: Компутестатеблоккмаск

Вычислите маску блока состояния, чтобы разрешить или запретить изменение состояния.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстатеблоккмаск* 
</dt> <dd>

Тип: **[ **D3DX11 \_ \_ \_ Маска блока состояния**](d3dx11-state-block-mask.md)\***

Указатель на маску блока State (см. раздел [**\_ \_ \_ Маска блока состояния D3DX11**](d3dx11-state-block-mask.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





