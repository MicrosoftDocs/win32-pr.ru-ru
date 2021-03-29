---
title: Метод ID3DX11EffectVariable Асклассинстанце (D3dx11effect. h)
description: Получение переменной экземпляра класса.
ms.assetid: c1d4adb5-7cd2-4ba2-9a91-3d03f9596a10
keywords:
- Метод Асклассинстанце Direct3D 11
- Метод Асклассинстанце Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асклассинстанце
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17dc9124f4b9a24ead503694c10a4a2d2205ed3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998321"
---
# <a name="id3dx11effectvariableasclassinstance-method"></a>Метод ID3DX11EffectVariable:: Асклассинстанце

Получение переменной экземпляра класса.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectClassInstanceVariable* AsClassInstance();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***

Указатель на переменную экземпляра класса. См. [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md).

## <a name="remarks"></a>Примечания

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

 

 





