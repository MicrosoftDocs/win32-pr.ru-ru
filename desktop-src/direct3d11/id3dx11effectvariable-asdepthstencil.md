---
title: Метод ID3DX11EffectVariable АсдепсстенЦил (D3dx11effect. h)
description: Возвращает переменную с набором элементов глубины.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- Метод АсдепсстенЦил Direct3D 11
- Метод АсдепсстенЦил Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод АсдепсстенЦил
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771f22b6b757b9144fca7e2637a3a702232b3d2a4a837938454b2acd5237cfae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729134"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a>Метод ID3DX11EffectVariable:: АсдепсстенЦил

Возвращает переменную с набором элементов глубины.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***

Указатель на переменную шаблона глубины. См. [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).

## <a name="remarks"></a>Remarks

АсдепсстенЦил Возвращает версию переменной Effect, которая была специализированной для переменной шаблона глубины. Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит данных шаблона глубины.

Приложения могут проверить возвращаемый объект на допустимость, вызвав [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





