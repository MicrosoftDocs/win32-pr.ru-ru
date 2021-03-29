---
title: Метод ID3DX11EffectType Жетмемберсемантик (D3dx11effect. h)
description: Возвращает семантическую присоединение к элементу.
ms.assetid: e0666d4e-7510-4496-849e-a0531238b5f8
keywords:
- Метод Жетмемберсемантик Direct3D 11
- Метод Жетмемберсемантик Direct3D 11, интерфейс ID3DX11EffectType
- Интерфейс ID3DX11EffectType Direct3D 11, метод Жетмемберсемантик
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberSemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6255860dc9f7dc5cf12742e6f40b7e5148a3f27c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998384"
---
# <a name="id3dx11effecttypegetmembersemantic-method"></a>Метод ID3DX11EffectType:: Жетмемберсемантик

Возвращает семантическую присоединение к элементу.

## <a name="syntax"></a>Синтаксис


```C++
LPCSTR GetMemberSemantic(
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

Строка, содержащая семантику.

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

 

