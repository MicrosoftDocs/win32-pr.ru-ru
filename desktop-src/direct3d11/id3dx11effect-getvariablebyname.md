---
title: Метод ID3DX11Effect Жетвариаблебинаме (D3dx11effect. h)
description: Получить переменную по имени.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Метод Жетвариаблебинаме Direct3D 11
- Метод Жетвариаблебинаме Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетвариаблебинаме
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998609"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>Метод ID3DX11Effect:: Жетвариаблебинаме

Получить переменную по имени.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя*; 
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Имя переменной.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Возвращает недопустимую переменную, если указанное имя не найдено.

## <a name="remarks"></a>Примечания

Результат может содержать одну или несколько переменных. Переменные за пределами метода считаются глобальными для всех эффектов, а те, которые находятся внутри метода, являются локальными для этого метода. Можно получить доступ к переменной Effect, используя ее имя или индекс.

Метод возвращает указатель на [**интерфейс переменной влияния**](id3dx11effectvariable.md) независимо от того, найдена ли переменная. [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) следует вызывать, чтобы проверить, существует ли имя.

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

 

