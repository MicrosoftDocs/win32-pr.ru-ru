---
title: Интерфейс ID3DX11EffectType (D3dx11effect. h)
description: Интерфейс ID3DX11EffectType обращается к переменным эффектов по типу. Время существования объекта ID3DX11EffectType равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Интерфейс ID3DX11EffectType Direct3D 11
- Интерфейс ID3DX11EffectType Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820997"
---
# <a name="id3dx11effecttype-interface"></a>Интерфейс ID3DX11EffectType

Интерфейс **ID3DX11EffectType** обращается к переменным эффектов по типу.

Время существования объекта **ID3DX11EffectType** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectType** содержит следующие методы.



| Метод                                                                       | Описание                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [**GetDesc**](id3dx11effecttype-getdesc.md)                                 | Получите описание типа Effect.<br/>        |
| [**жетмембернаме**](id3dx11effecttype-getmembername.md)                     | Возвращает имя элемента.<br/>              |
| [**жетмемберсемантик**](id3dx11effecttype-getmembersemantic.md)             | Возвращает семантическую присоединение к элементу.<br/> |
| [**GetMemberTypeByIndex**](id3dx11effecttype-getmembertypebyindex.md)       | Получение типа элемента по индексу.<br/>            |
| [**GetMemberTypeByName**](id3dx11effecttype-getmembertypebyname.md)         | Получение типа элемента по имени.<br/>            |
| [**жетмембертипебисемантик**](id3dx11effecttype-getmembertypebysemantic.md) | Получение типа члена по семантике.<br/>         |
| [**IsValid**](id3dx11effecttype-isvalid.md)                                 | Проверяет допустимость типа воздействия.<br/>   |



 

## <a name="remarks"></a>Примечания

Чтобы получить сведения о типе эффектов из переменной Effect, вызовите метод [**ID3DX11EffectVariable:: GetType**](id3dx11effectvariable-gettype.md).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





