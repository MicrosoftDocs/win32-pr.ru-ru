---
title: Метод ID3DX11EffectType Жетмембертипебиндекс (D3dx11effect. h)
description: Получение типа элемента по индексу.
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- Метод Жетмембертипебиндекс Direct3D 11
- Метод Жетмембертипебиндекс Direct3D 11, интерфейс ID3DX11EffectType
- Интерфейс ID3DX11EffectType Direct3D 11, метод Жетмембертипебиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53500ec94791ff534bf6b3c9a2e7d46a51b7b69bc889f35515e9b653c5bbb422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532326"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a>Метод ID3DX11EffectType:: Жетмембертипебиндекс

Получение типа элемента по индексу.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

