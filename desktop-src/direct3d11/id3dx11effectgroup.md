---
title: Интерфейс ID3DX11EffectGroup (D3dx11effect. h)
description: Интерфейс ID3DX11EffectGroup обращается к группе эффектов. Время существования объекта ID3DX11EffectGroup равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Интерфейс ID3DX11EffectGroup Direct3D 11
- Интерфейс ID3DX11EffectGroup Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986954"
---
# <a name="id3dx11effectgroup-interface"></a>Интерфейс ID3DX11EffectGroup

Интерфейс **ID3DX11EffectGroup** обращается к группе эффектов.

Время существования объекта **ID3DX11EffectGroup** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectGroup** содержит следующие методы.



| Метод                                                                  | Описание                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**жетаннотатионбиндекс**](id3dx11effectgroup-getannotationbyindex.md) | Получение заметки по индексу.<br/>                        |
| [**жетаннотатионбинаме**](id3dx11effectgroup-getannotationbyname.md)   | Получение заметки по имени.<br/>                         |
| [**GetDesc**](id3dx11effectgroup-getdesc.md)                           | Возвращает описание группы.<br/>                          |
| [**жеттечникуебиндекс**](id3dx11effectgroup-gettechniquebyindex.md)   | Получение методики по индексу.<br/>                          |
| [**жеттечникуебинаме**](id3dx11effectgroup-gettechniquebyname.md)     | Получите метод по имени.<br/>                           |
| [**IsValid**](id3dx11effectgroup-isvalid.md)                           | Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис.<br/> |



 

## <a name="remarks"></a>Примечания

Чтобы получить интерфейс **ID3DX11EffectGroup** , вызовите метод, например [**ID3DX11Effect:: жетграупбинаме**](id3dx11effect-getgroupbyname.md).

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

 

 





