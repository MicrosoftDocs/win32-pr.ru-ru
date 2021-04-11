---
title: Метод ID3DX11Effect Жетвариаблебисемантик (D3dx11effect. h)
description: Получить переменную по семантике.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Метод Жетвариаблебисемантик Direct3D 11
- Метод Жетвариаблебисемантик Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетвариаблебисемантик
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273908"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a>Метод ID3DX11Effect:: Жетвариаблебисемантик

Получить переменную по семантике.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Семантическ* 
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Семантическое имя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Указатель на переменную действия, определяемую семантикой. См. [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Примечания

Каждая переменная Effect может иметь семантическую присоединение, которая представляет собой строку метаданных, определяемую пользователем. Некоторые [семантики системных значений](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) являются зарезервированными словами, которые инициируют встроенные функции стадией конвейера.

Метод возвращает указатель на [**интерфейс переменной влияния**](id3dx11effectvariable.md) , если переменная не найдена. можно вызвать [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) , чтобы проверить, существует ли семантическая семантика.

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

 

