---
title: Интерфейс ID3DX11EffectPass (D3dx11effect. h)
description: Интерфейс ID3DX11EffectPass инкапсулирует назначения состояний в рамках метода. Время существования объекта ID3DX11EffectPass равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Интерфейс ID3DX11EffectPass Direct3D 11
- Интерфейс ID3DX11EffectPass Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273912"
---
# <a name="id3dx11effectpass-interface"></a>Интерфейс ID3DX11EffectPass

Интерфейс **ID3DX11EffectPass** инкапсулирует назначения состояний в рамках метода.

Время существования объекта **ID3DX11EffectPass** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectPass** содержит следующие методы.



| Метод                                                                   | Описание                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Применить**](id3dx11effectpass-apply.md)                                 | Задайте состояние, которое содержится в передаче на устройство.<br/>       |
| [**компутестатеблоккмаск**](id3dx11effectpass-computestateblockmask.md) | Создание маски для разрешения или запрета изменений состояния.<br/> |
| [**жетаннотатионбиндекс**](id3dx11effectpass-getannotationbyindex.md)   | Получение заметки по индексу.<br/>                            |
| [**жетаннотатионбинаме**](id3dx11effectpass-getannotationbyname.md)     | Получение заметки по имени.<br/>                             |
| [**жеткомпутешадердеск**](id3dx11effectpass-getcomputeshaderdesc.md)   | Получение описания вычислений для шейдера.<br/>                      |
| [**GetDesc**](id3dx11effectpass-getdesc.md)                             | Получите описание этапа.<br/>                                |
| [**жетдомаиншадердеск**](id3dx11effectpass-getdomainshaderdesc.md)     | Получите описание шейдера домена.<br/>                       |
| [**жетжеометришадердеск**](id3dx11effectpass-getgeometryshaderdesc.md) | Получите описание геометрического шейдера.<br/>                     |
| [**жесуллшадердеск**](id3dx11effectpass-gethullshaderdesc.md)         | Получение описания поверхности-шейдера.<br/>                           |
| [**жетпикселшадердеск**](id3dx11effectpass-getpixelshaderdesc.md)       | Получите описание пиксельного шейдера.<br/>                        |
| [**жетвертексшадердеск**](id3dx11effectpass-getvertexshaderdesc.md)     | Получите описание вершинного шейдера.<br/>                       |
| [**IsValid**](id3dx11effectpass-isvalid.md)                             | Протестируйте пройденный тест, чтобы увидеть, содержит ли он допустимый синтаксис.<br/>        |



 

## <a name="remarks"></a>Примечания

Проход — это блок кода, который задает объекты состояния рендеринга и шейдеры. В методе объявляется проход.

Чтобы получить интерфейс передачи эффектов, вызовите метод, например [**ID3DX11EffectTechnique:: жетпассбинаме**](id3dx11effecttechnique-getpassbyname.md).

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

 

 





