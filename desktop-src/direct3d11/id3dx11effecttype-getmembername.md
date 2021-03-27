---
title: Метод ID3DX11EffectType Жетмембернаме (D3dx11effect. h)
description: Возвращает имя элемента.
ms.assetid: cd231741-09e1-4e69-9384-5cdfbf83fc8b
keywords:
- Метод Жетмембернаме Direct3D 11
- Метод Жетмембернаме Direct3D 11, интерфейс ID3DX11EffectType
- Интерфейс ID3DX11EffectType Direct3D 11, метод Жетмембернаме
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4aa9a24067d8ef19680ca58e41659da850659b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355170"
---
# <a name="id3dx11effecttypegetmembername-method"></a>Метод ID3DX11EffectType:: Жетмембернаме

Возвращает имя элемента.

## <a name="syntax"></a>Синтаксис


```C++
LPCSTR GetMemberName(
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

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Имя элемента.

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

