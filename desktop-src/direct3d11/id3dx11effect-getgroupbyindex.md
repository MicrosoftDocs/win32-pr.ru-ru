---
title: Метод ID3DX11Effect Жетграупбиндекс (D3dx11effect. h)
description: Возвращает группу эффектов по индексу.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Метод Жетграупбиндекс Direct3D 11
- Метод Жетграупбиндекс Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетграупбиндекс
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd0f629a60255ed28aa5cc426b99198867e0b23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000467"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a>Метод ID3DX11Effect:: Жетграупбиндекс

Возвращает группу эффектов по индексу.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс группы эффектов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***

Указатель на интерфейс [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

