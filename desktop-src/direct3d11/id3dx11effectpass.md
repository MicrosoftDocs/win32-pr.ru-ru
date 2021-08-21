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
ms.openlocfilehash: 33b24fe0154e447cd993e8e7e939a9a023ed37183a56980dab8f5d803a0ea41e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045982"
---
# <a name="id3dx11effectpass-interface"></a>Интерфейс ID3DX11EffectPass

Интерфейс **ID3DX11EffectPass** инкапсулирует назначения состояний в рамках метода.

Время существования объекта **ID3DX11EffectPass** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectPass** содержит следующие методы.



| Метод                                                                   | Описание                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Касаться**](id3dx11effectpass-apply.md)                                 | Задайте состояние, которое содержится в передаче на устройство.<br/>       |
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



 

## <a name="remarks"></a>Remarks

Проход — это блок кода, который задает объекты состояния рендеринга и шейдеры. В методе объявляется проход.

Чтобы получить интерфейс передачи эффектов, вызовите метод, например [**ID3DX11EffectTechnique:: жетпассбинаме**](id3dx11effecttechnique-getpassbyname.md).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





