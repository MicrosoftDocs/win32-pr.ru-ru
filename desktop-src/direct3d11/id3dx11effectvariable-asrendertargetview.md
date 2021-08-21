---
title: Метод ID3DX11EffectVariable Асрендертаржетвиев (D3dx11effect. h)
description: Получает переменную визуализации-целевого представления.
ms.assetid: 1eec342e-267a-4eab-886a-a309758065c7
keywords:
- Метод Асрендертаржетвиев Direct3D 11
- Метод Асрендертаржетвиев Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асрендертаржетвиев
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRenderTargetView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a8b44b3ed67b6293d4b4add329eef532fdc44cb12cea9e84b1ddf43fb72cc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531425"
---
# <a name="id3dx11effectvariableasrendertargetview-method"></a>Метод ID3DX11EffectVariable:: Асрендертаржетвиев

Получает переменную визуализации-целевого представления.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectRenderTargetViewVariable* AsRenderTargetView();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***

Указатель на переменную визуализации целевого представления. См. [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).

## <a name="remarks"></a>Remarks

Этот метод возвращает версию переменной Effect, которая была специализированной для переменной визуализации-целевого представления. Как и в приведении, эта специализация вернет недопустимый объект, если переменная действия не содержит данные представления целевого объекта визуализации.

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

 

 





