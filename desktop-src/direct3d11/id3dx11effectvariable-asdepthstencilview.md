---
title: Метод ID3DX11EffectVariable АсдепсстенЦилвиев (D3dx11effect. h)
description: Получите переменную представления с глубиной набора элементов.
ms.assetid: 491ca6e1-a74c-4996-a25c-ea40910f0f36
keywords:
- Метод АсдепсстенЦилвиев Direct3D 11
- Метод АсдепсстенЦилвиев Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод АсдепсстенЦилвиев
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencilView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dc0ce53478da8d7057c142c87daea5fb83503b4ac7cd1a0dee5edda89246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531515"
---
# <a name="id3dx11effectvariableasdepthstencilview-method"></a>Метод ID3DX11EffectVariable:: АсдепсстенЦилвиев

Получите переменную представления с глубиной набора элементов.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectDepthStencilViewVariable* AsDepthStencilView();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)\***

Указатель на переменную представления с набором элементов depth. См. [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md).

## <a name="remarks"></a>Remarks

Этот метод возвращает версию переменной Effect, которая была специализированной для переменной представления глубины-трафарет-View. Как и в приведении, эта специализация вернет недопустимый объект, если переменная действия не содержит данных представления глубины-трафарета.

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

 

 





