---
title: Метод ID3DX11EffectVariable Асбленд (D3dx11effect. h)
description: Получить переменную Effect.
ms.assetid: e9670d13-e006-408b-9cdf-352bcfa66a52
keywords:
- Метод Асбленд Direct3D 11
- Метод Асбленд Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асбленд
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsBlend
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fd9f6f76c0e3aa46e176b2f35960196fcc73eb021d4e5a250be4a5b245a5ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531606"
---
# <a name="id3dx11effectvariableasblend-method"></a>Метод ID3DX11EffectVariable:: Асбленд

Получить переменную Effect.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectBlendVariable* AsBlend();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)\***

Указатель на переменную смешения эффектов. См. [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md).

## <a name="remarks"></a>Remarks

Асбленд Возвращает версию переменной Effect, которая была специализированной для переменной Effect-Blend. Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит данных о силе.

Приложения могут проверить возвращаемый объект на допустимость, вызвав [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





