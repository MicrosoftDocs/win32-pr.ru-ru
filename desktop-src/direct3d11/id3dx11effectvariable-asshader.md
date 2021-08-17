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
ms.openlocfilehash: 050ed69e9a4f498cb28062dcf493f88f4132e7578b436e3c0f54420d57264fd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119376484"
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

## <a name="remarks"></a>Remarks

Асшадер Возвращает версию переменной Effect, которая была специализированной для переменной шейдера. Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит данных шейдера.

Приложения могут проверить возвращаемый объект на допустимость, вызвав [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





