---
title: Метод ID3DX11EffectVariable Асконстантбуффер (D3dx11effect. h)
description: Получение буфера константы. | Метод ID3DX11EffectVariable Асконстантбуффер (D3dx11effect. h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Метод Асконстантбуффер Direct3D 11
- Метод Асконстантбуффер Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асконстантбуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4caca60216df0c04a773da22150dbc6f7be717
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998432"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a>Метод ID3DX11EffectVariable:: Асконстантбуффер

Получение буфера константы.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Указатель на буфер константы. См. [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Примечания

Асконстантбуффер Возвращает версию переменной Effect, которая была специализированной для буфера констант. Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит данные буфера констант.

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

 

 





