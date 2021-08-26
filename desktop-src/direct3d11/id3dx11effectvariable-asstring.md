---
title: Метод ID3DX11EffectVariable AsString (D3dx11effect. h)
description: Получение строковой переменной.
ms.assetid: 60f8a730-bf95-4577-9259-7348d479ac3d
keywords:
- Метод AsString Direct3D 11
- Метод AsString Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод AsString
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c69eecaabec6b7da49f7f36f6c75677fdd20cdb462f26fe5e02650e6746c01f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069614"
---
# <a name="id3dx11effectvariableasstring-method"></a>Метод ID3DX11EffectVariable:: AsString

Получение строковой переменной.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectStringVariable* AsString();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***

Указатель на строковую переменную. См. [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).

## <a name="remarks"></a>Remarks

AsString Возвращает версию переменной Effect, которая была специализированной для строковой переменной. Как и в приведении, эта специализация вернет недопустимый объект, если переменная действия не содержит строковые данные.

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

 

 





