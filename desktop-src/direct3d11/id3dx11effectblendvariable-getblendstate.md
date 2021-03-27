---
title: Метод ID3DX11EffectBlendVariable Жетблендстате (D3dx11effect. h)
description: Получает указатель на интерфейс состояния смешения.
ms.assetid: ab4ee765-b5ad-4dc3-9b00-48052528d3bd
keywords:
- Метод Жетблендстате Direct3D 11
- Метод Жетблендстате Direct3D 11, интерфейс ID3DX11EffectBlendVariable
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11, метод Жетблендстате
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48092b496fa8a38be7c9dd8aea67a26e8b56f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355523"
---
# <a name="id3dx11effectblendvariablegetblendstate-method"></a>Метод ID3DX11EffectBlendVariable:: Жетблендстате

Получает указатель на интерфейс состояния смешения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBlendState(
   UINT             Index,
   ID3D11BlendState **ppBlendState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс в массиве интерфейсов состояния смешения. Если имеется только один интерфейс состояния Blend, используйте значение 0.

</dd> <dt>

*ппблендстате* 
</dt> <dd>

Тип: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***

Адрес указателя на интерфейс состояния смешения (см. [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

