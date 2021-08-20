---
title: Интерфейс ID3DX11EffectRasterizerVariable (D3dx11effect. h)
description: Интерфейс переменной средства прорисовки имеет доступ к состоянию программной прорисовки.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- Интерфейс ID3DX11EffectRasterizerVariable Direct3D 11
- Интерфейс ID3DX11EffectRasterizerVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4653936edc3fd2181f875b3a848e401b8fa24d318a1e48df4fa06e462ae3cf19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534190"
---
# <a name="id3dx11effectrasterizervariable-interface"></a>Интерфейс ID3DX11EffectRasterizerVariable

Интерфейс переменной средства прорисовки имеет доступ к состоянию программной прорисовки.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectRasterizerVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectRasterizerVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectRasterizerVariable** содержит следующие методы.



| Метод                                                                                   | Описание                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**жетбаккингсторе**](id3dx11effectrasterizervariable-getbackingstore.md)               | Возвращает указатель на переменную, которая содержит состояние растерисер.<br/> |
| [**жетрастеризерстате**](id3dx11effectrasterizervariable-getrasterizerstate.md)         | Получение указателя на интерфейс средства программной прорисовки.<br/>                    |
| [**сетрастеризерстате**](id3dx11effectrasterizervariable-setrasterizerstate.md)         | Задает состояние средства программной прорисовки.<br/>                                  |
| [**ундосетрастеризерстате**](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | Возвращает ранее установленное состояние средства отображения программной прорисовки.<br/>                  |



 

## <a name="remarks"></a>Remarks

Интерфейс [**ID3DX11EffectVariable**](id3dx11effectvariable.md) создается при считывании воздействия в память.

Переменные эффектов сохраняются в памяти в резервном хранилище; При применении метода значения в резервном хранилище копируются на устройство. Для возврата состояния можно использовать любой из этих методов.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





