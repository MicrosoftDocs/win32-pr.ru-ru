---
title: Метод ID3DX11EffectVariable Асшадерресаурце (D3dx11effect. h)
description: Получение переменной-ресурса шейдера.
ms.assetid: 02db94eb-980a-4677-af89-3006aef6faca
keywords:
- Метод Асшадерресаурце Direct3D 11
- Метод Асшадерресаурце Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асшадерресаурце
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShaderResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef87874c005f12d3e49962ee438f516df3631c12ff17fc4db27e0a82fe1a654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531387"
---
# <a name="id3dx11effectvariableasshaderresource-method"></a>Метод ID3DX11EffectVariable:: Асшадерресаурце

Получение переменной-ресурса шейдера.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectShaderResourceVariable* AsShaderResource();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***

Указатель на переменную-ресурс шейдера. См. [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).

## <a name="remarks"></a>Remarks

Асшадерресаурце Возвращает версию переменной Effect, которая была специализированной для переменной-ресурса шейдера. Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит данных о ресурсах шейдера.

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

 

 





