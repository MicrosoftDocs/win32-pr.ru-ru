---
title: Интерфейс ID3DX11EffectVariable (D3dx11effect. h)
description: Интерфейс ID3DX11EffectVariable является базовым классом для всех переменных эффектов. Время существования объекта ID3DX11EffectVariable равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Интерфейс ID3DX11EffectVariable Direct3D 11
- Интерфейс ID3DX11EffectVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821285"
---
# <a name="id3dx11effectvariable-interface"></a>Интерфейс ID3DX11EffectVariable

Интерфейс **ID3DX11EffectVariable** является базовым классом для всех переменных эффектов.

Время существования объекта **ID3DX11EffectVariable** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectVariable** содержит следующие методы.



| Метод                                                                           | Описание                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**асбленд**](id3dx11effectvariable-asblend.md)                                 | Получить переменную Effect.<br/>                |
| [**асклассинстанце**](id3dx11effectvariable-asclassinstance.md)                 | Получение переменной экземпляра класса.<br/>              |
| [**асконстантбуффер**](id3dx11effectvariable-asconstantbuffer.md)               | Получение буфера константы.<br/>                      |
| [**асдепсстенЦил**](id3dx11effectvariable-asdepthstencil.md)                   | Возвращает переменную с набором элементов глубины.<br/>               |
| [**асдепсстенЦилвиев**](id3dx11effectvariable-asdepthstencilview.md)           | Получите переменную представления с глубиной набора элементов.<br/>          |
| [**асинтерфаце**](id3dx11effectvariable-asinterface.md)                         | Возвращает переменную интерфейса.<br/>                  |
| [**асматрикс**](id3dx11effectvariable-asmatrix.md)                               | Возвращает переменную матрицы.<br/>                      |
| [**асрастеризер**](id3dx11effectvariable-asrasterizer.md)                       | Получение переменной средства программной прорисовки.<br/>                  |
| [**асрендертаржетвиев**](id3dx11effectvariable-asrendertargetview.md)           | Получает переменную визуализации-целевого представления.<br/>          |
| [**ассамплер**](id3dx11effectvariable-assampler.md)                             | Получить переменную образца.<br/>                     |
| [**асскалар**](id3dx11effectvariable-asscalar.md)                               | Получить скалярную переменную.<br/>                      |
| [**асшадер**](id3dx11effectvariable-asshader.md)                               | Получение переменной шейдера.<br/>                      |
| [**асшадерресаурце**](id3dx11effectvariable-asshaderresource.md)               | Получение переменной-ресурса шейдера.<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | Получение строковой переменной.<br/>                      |
| [**асунордередакцессвиев**](id3dx11effectvariable-asunorderedaccessview.md)     | Возвращает неупорядоченную переменную с доступом к представлениям.<br/>      |
| [**асвектор**](id3dx11effectvariable-asvector.md)                               | Получение переменной Vector.<br/>                      |
| [**жетаннотатионбиндекс**](id3dx11effectvariable-getannotationbyindex.md)       | Получение заметки по индексу.<br/>                 |
| [**жетаннотатионбинаме**](id3dx11effectvariable-getannotationbyname.md)         | Получение заметки по имени.<br/>                  |
| [**GetDesc**](id3dx11effectvariable-getdesc.md)                                 | Получить описание.<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | Получение элемента массива.<br/>                       |
| [**жетмембербиндекс**](id3dx11effectvariable-getmemberbyindex.md)               | Получение члена структуры по индексу.<br/>            |
| [**жетмембербинаме**](id3dx11effectvariable-getmemberbyname.md)                 | Получение члена структуры по имени.<br/>             |
| [**жетмембербисемантик**](id3dx11effectvariable-getmemberbysemantic.md)         | Получение члена структуры по семантике.<br/>         |
| [**жетпарентконстантбуффер**](id3dx11effectvariable-getparentconstantbuffer.md) | Получение буфера константы.<br/>                      |
| [**жетраввалуе**](id3dx11effectvariable-getrawvalue.md)                         | Получение данных.<br/>                                   |
| [**GetType**](id3dx11effectvariable-gettype.md)                                 | Получение сведений о типе.<br/>                       |
| [**IsValid**](id3dx11effectvariable-isvalid.md)                                 | Сравните тип данных с хранимыми данными.<br/> |
| [**сетраввалуе**](id3dx11effectvariable-setrawvalue.md)                         | Настройка данных.<br/>                                   |



 

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

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





