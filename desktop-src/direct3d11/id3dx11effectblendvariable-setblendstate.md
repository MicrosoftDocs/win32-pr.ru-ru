---
title: Метод ID3DX11EffectBlendVariable Сетблендстате (D3dx11effect. h)
description: Задает состояние смешения для действия.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Метод Сетблендстате Direct3D 11
- Метод Сетблендстате Direct3D 11, интерфейс ID3DX11EffectBlendVariable
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11, метод Сетблендстате
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a8f945faaf7f07846ea58b91378bbf2e6c06eeb1c3d0d041a6e0a71e2e9ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046502"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a>Метод ID3DX11EffectBlendVariable:: Сетблендстате

Задает состояние смешения для действия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс в массиве интерфейсов состояния смешения. Если имеется только один интерфейс состояния Blend, используйте значение 0.

</dd> <dt>

*пблендстате* 
</dt> <dd>

Тип: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***

Указатель на интерфейс [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) , содержащий заданное состояние смешения.

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

