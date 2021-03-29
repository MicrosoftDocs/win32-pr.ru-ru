---
title: Интерфейс ID3DX11EffectTechnique (D3dx11effect. h)
description: Интерфейс ID3DX11EffectTechnique — это коллекция проходов. Время существования объекта ID3DX11EffectTechnique равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Интерфейс ID3DX11EffectTechnique Direct3D 11
- Интерфейс ID3DX11EffectTechnique Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987194"
---
# <a name="id3dx11effecttechnique-interface"></a>Интерфейс ID3DX11EffectTechnique

Интерфейс **ID3DX11EffectTechnique** — это коллекция проходов.

Время существования объекта **ID3DX11EffectTechnique** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectTechnique** содержит следующие методы.



| Метод                                                                        | Описание                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**компутестатеблоккмаск**](id3dx11effecttechnique-computestateblockmask.md) | Вычислите маску блока состояния, чтобы разрешить или запретить изменение состояния.<br/> |
| [**жетаннотатионбиндекс**](id3dx11effecttechnique-getannotationbyindex.md)   | Получение заметки по индексу.<br/>                                |
| [**жетаннотатионбинаме**](id3dx11effecttechnique-getannotationbyname.md)     | Получение заметки по имени.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Получите описание метода.<br/>                               |
| [**жетпассбиндекс**](id3dx11effecttechnique-getpassbyindex.md)               | Получение передаваемого по индексу.<br/>                                       |
| [**жетпассбинаме**](id3dx11effecttechnique-getpassbyname.md)                 | Получение передачи по имени.<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | Протестируйте метод, чтобы проверить, содержит ли он допустимый синтаксис.<br/>       |



 

## <a name="remarks"></a>Примечания

Результат содержит один или несколько методов. Каждый прием содержит один или несколько проходов; Каждый этап содержит назначения состояний.

Чтобы получить интерфейс методики влияния, вызовите метод, например [**ID3DX11Effect:: жеттечникуебинаме**](id3dx11effect-gettechniquebyname.md).

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

 

 





