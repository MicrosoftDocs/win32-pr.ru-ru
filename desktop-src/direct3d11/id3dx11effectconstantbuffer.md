---
title: Интерфейс ID3DX11EffectConstantBuffer (D3dx11effect. h)
description: Интерфейс постоянного буфера обращается к постоянным буферам или буферам текстур.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355253"
---
# <a name="id3dx11effectconstantbuffer-interface"></a>Интерфейс ID3DX11EffectConstantBuffer

Интерфейс постоянного буфера обращается к постоянным буферам или буферам текстур.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectConstantBuffer** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectConstantBuffer** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectConstantBuffer** содержит следующие методы.



| Метод                                                                             | Описание                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**жетконстантбуффер**](id3dx11effectconstantbuffer-getconstantbuffer.md)         | Получение постоянного буфера.<br/>                    |
| [**жеттекстуребуффер**](id3dx11effectconstantbuffer-gettexturebuffer.md)           | Получение буфера текстуры.<br/>                     |
| [**сетконстантбуффер**](id3dx11effectconstantbuffer-setconstantbuffer.md)         | Установите константный буфер.<br/>                    |
| [**сеттекстуребуффер**](id3dx11effectconstantbuffer-settexturebuffer.md)           | Задайте буфер текстуры.<br/>                     |
| [**ундосетконстантбуффер**](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | Восстанавливает ранее установленный буфер констант.<br/> |
| [**ундосеттекстуребуффер**](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | Восстанавливает ранее установленный буфер текстуры.<br/>  |



 

## <a name="remarks"></a>Примечания

Используйте буферы констант для хранения многих констант эффектов; Группирование констант в буферы на основе частоты обновления. Это позволяет максимально сокращать количество изменений состояния, а также упростить изменение состояния минимальных вызовов API. Оба эти фактора приводят к повышению производительности.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





