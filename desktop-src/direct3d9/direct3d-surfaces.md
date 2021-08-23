---
description: Поверхность представляет собой линейную область отображения памяти и обычно находится в отображаемой памяти видеокарты, хотя поверхности могут существовать в системной памяти. Поверхности управляются интерфейсом IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Поверхности Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529320673eca39cf4b9afdb96377295d595191fd79cd81c316b258841d82ae6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988204"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Поверхности Direct3D (Direct3D 9)

Поверхность представляет собой линейную область отображения памяти и обычно находится в отображаемой памяти видеокарты, хотя поверхности могут существовать в системной памяти. Поверхности управляются интерфейсом [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .

-   Интерфейсный буфер. Прямоугольник памяти, который преобразуется графическим адаптером и отображается на мониторе. В Direct3D приложение никогда не записывает данные непосредственно в передний буфер.
-   Задний буфер. Прямоугольник памяти, в который приложение может непосредственно выполнять запись. Задний буфер никогда не отображается на мониторе напрямую.
-   Зеркальное отображение поверхностей. Процесс перемещения заднего буфера в передний буфер.
-   Цепочка буфера обмена. Коллекция из одного или нескольких задних буферов, которые могут быть последовательно представлены в интерфейсном буфере.

## <a name="getting-a-surface"></a>Получение поверхности

Создайте поверхность, вызвав любой из следующих методов:

-   [**креатедепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**креатеоффскринплаинсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**креатерендертаржет**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

Форматы поверхности определяют, как интерпретируется данные для каждого пикселя в памяти поверхности. Для описания формата поверхности Direct3D использует элемент [D3DFORMAT](d3dformat.md) структуры [**D3DSURFACE \_ DESC**](d3dsurface-desc.md) . Можно получить формат существующей поверхности, вызвав [**метод WebMethod**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .

После создания поверхности можно получить указатель на него, вызвав любой из следующих методов:

-   [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**жетбаккбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**жетдепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**жетфронтбуффердата**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**жетрендертаржет**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**жетбаккбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**жетсурфацелевел**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

Интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) позволяет косвенно обращаться к памяти с помощью метода [**упдатесурфаце**](/windows/desktop/api) . Этот метод позволяет копировать прямоугольную область пикселей из одного интерфейса **IDirect3DSurface9** в другой интерфейс **IDirect3DSurface9** . Интерфейс Surface также имеет методы для прямого доступа к отображаемой памяти. Например, можно использовать метод [**локкрект**](/windows/desktop/api) , чтобы заблокировать прямоугольную область экрана памяти. Важно вызвать [**унлоккрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) после завершения работы с заблокированной прямоугольной областью на поверхности.

## <a name="additional-surface-topics"></a>Дополнительные разделы о контактах

Узнайте больше об использовании поверхностей с любым из следующих разделов:

-   [Форматы поверхностей (Direct3D 9)](surface-formats.md)
-   [Что такое цепочка подкачки? (Direct3D 9)](what-is-a-swap-chain-.md)
-   [Ширина и шаг (Direct3D 9)](width-vs--pitch.md)
-   [Зеркальное отображение поверхностей (Direct3D 9)](flipping-surfaces.md)
-   [Перелистывание страниц и обратная буферизация (Direct3D 9)](page-flipping-and-back-buffering.md)
-   [Копирование на поверхности (Direct3D 9)](copying-to-surfaces.md)
-   [Копирование поверхностей (Direct3D 9)](copying-surfaces.md)
-   [Прямой доступ к памяти Surface (Direct3D 9)](accessing-surface-memory-directly.md)
-   [Частные данные поверхности (Direct3D 9)](private-surface-data.md)
-   [Элементы управления гамма (Direct3D 9)](gamma-controls.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Начало работы](getting-started.md)
</dt> </dl>

 

 
