---
title: Метод ID3DX11Effect Жетвариаблебиндекс (D3dx11effect. h)
description: Возвращает переменную по индексу.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Метод Жетвариаблебиндекс Direct3D 11
- Метод Жетвариаблебиндекс Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетвариаблебиндекс
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998615"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a>Метод ID3DX11Effect:: Жетвариаблебиндекс

Возвращает переменную по индексу.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый с нуля индекс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Примечания

Результат может содержать одну или несколько переменных. Переменные за пределами метода считаются глобальными для всех эффектов, а те, которые находятся внутри метода, являются локальными для этого метода. Можно получить доступ к любой локальной переменной с нестатическим действием, используя ее имя или индекс.

Метод возвращает указатель на [**интерфейс переменной влияния**](id3dx11effectvariable.md) , если переменная не найдена. можно вызвать [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) , чтобы проверить, существует ли индекс.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

