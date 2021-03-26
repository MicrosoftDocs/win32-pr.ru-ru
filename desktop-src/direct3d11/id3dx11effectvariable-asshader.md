---
title: Метод ID3DX11EffectVariable Асшадер (D3dx11effect. h)
description: Получение переменной шейдера.
ms.assetid: 660ba087-5320-44f7-946f-e500101fc6bb
keywords:
- Метод Асшадер Direct3D 11
- Метод Асшадер Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асшадер
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c8d9f1a487e4003bd032180d1f815e4a48fe0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998588"
---
# <a name="id3dx11effectvariableasshader-method"></a>Метод ID3DX11EffectVariable:: Асшадер

Получение переменной шейдера.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectShaderVariable* AsShader();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

Указатель на переменную шейдера. См. [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md).

## <a name="remarks"></a>Примечания

Асшадер Возвращает версию переменной Effect, которая была специализированной для переменной шейдера. Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит данных шейдера.

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

 

 





