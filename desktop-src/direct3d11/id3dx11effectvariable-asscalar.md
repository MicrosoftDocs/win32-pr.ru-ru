---
title: Метод ID3DX11EffectVariable Асскалар (D3dx11effect. h)
description: Получить скалярную переменную.
ms.assetid: 5cc02fb3-351a-4309-9145-1ed7d759a650
keywords:
- Метод Асскалар Direct3D 11
- Метод Асскалар Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асскалар
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsScalar
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e455250ae99075af449793d634fd6b3c2fafc4b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821541"
---
# <a name="id3dx11effectvariableasscalar-method"></a>Метод ID3DX11EffectVariable:: Асскалар

Получить скалярную переменную.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectScalarVariable* AsScalar();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***

Указатель на скалярную переменную. См. [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md).

## <a name="remarks"></a>Примечания

Асскалар Возвращает версию переменной Effect, которая была специализированной для скалярной переменной. Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит скалярных данных.

Приложения могут проверить возвращаемый объект на допустимость, вызвав [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





