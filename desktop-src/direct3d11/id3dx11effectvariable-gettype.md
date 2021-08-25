---
title: Метод GetType ID3DX11EffectVariable (D3dx11effect. h)
description: Получение сведений о типе.
ms.assetid: c9ada96a-0259-48c1-b869-ba0f51bf4600
keywords:
- Метод GetType Direct3D 11
- Метод GetType Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод GetType
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0eae9da797ee22f85234383e2e54d97f4cb1045bcdd0216e70899b294b42378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894554"
---
# <a name="id3dx11effectvariablegettype-method"></a>Метод ID3DX11EffectVariable:: GetType

Получение сведений о типе.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectType* GetType();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Указатель на [**ID3DX11EffectType**](id3dx11effecttype.md).

## <a name="remarks"></a>Remarks

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

 

 





