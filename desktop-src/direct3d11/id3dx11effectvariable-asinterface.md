---
title: Метод ID3DX11EffectVariable Асинтерфаце (D3dx11effect. h)
description: Возвращает переменную интерфейса.
ms.assetid: 5b1e5d05-ab36-42c2-9990-154baff5e9a4
keywords:
- Метод Асинтерфаце Direct3D 11
- Метод Асинтерфаце Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асинтерфаце
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsInterface
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95fd7000e8529d04054ccaed84642e12d55417929789c569cc1f9893c2726f4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565654"
---
# <a name="id3dx11effectvariableasinterface-method"></a>Метод ID3DX11EffectVariable:: Асинтерфаце

Возвращает переменную интерфейса.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectInterfaceVariable* AsInterface();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***

Указатель на переменную интерфейса. См. [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md).

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

 

 





