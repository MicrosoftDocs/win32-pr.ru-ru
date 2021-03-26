---
title: Метод ID3DX11EffectSamplerVariable Жетбаккингсторе (D3dx11effect. h)
description: Возвращает указатель на переменную, содержащую состояние выборки.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Метод Жетбаккингсторе Direct3D 11
- Метод Жетбаккингсторе Direct3D 11, интерфейс ID3DX11EffectSamplerVariable
- Интерфейс ID3DX11EffectSamplerVariable Direct3D 11, метод Жетбаккингсторе
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355363"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a>Метод ID3DX11EffectSamplerVariable:: Жетбаккингсторе

Возвращает указатель на переменную, содержащую состояние выборки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индексировать в массив описаний образцов. Если в результате присутствует только одна переменная выборки, используйте значение 0.

</dd> <dt>

*псамплердеск* 
</dt> <dd>

Тип: **[ **D3D11 \_ образец \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***

Указатель на описание образца (см. [**D3D11ный \_ образец \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Примечания

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

