---
description: Приложение управляет ресурсами для отображения сцены.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Управление ресурсами (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0a9cf2ee85b2f8e86077eb525acffb914e60cba84082c9d610e10da9f5fa02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069054"
---
# <a name="manipulating-resources-direct3d-9"></a>Управление ресурсами (Direct3D 9)

Приложение управляет ресурсами для отображения сцены. Сначала приложению необходимо создать ресурс текстуры с помощью одного из следующих методов:

-   [**IDirect3DDevice9:: Креатекубетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**IDirect3DDevice9:: Креатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**IDirect3DDevice9:: Креатеволуметекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

Вместо этого можно создать ресурс текстуры с помощью одной из функций текстурирования D3DXCreatexxx.

Объекты текстуры, возвращаемые методами создания текстуры, являются контейнерами для поверхностей или томов. Эти контейнеры являются универсальными и называются буферами. Буферы, принадлежащие ресурсу, наследуют использование, формат и пул ресурса, но имеют собственный тип. Дополнительные сведения см. в разделе [свойства ресурсов (Direct3D 9)](resource-properties.md).

Приложение получает доступ к содержащимся в них поверхностям для загрузки иллюстраций, вызывая следующие методы. Дополнительные сведения см. в разделе [Блокировка ресурсов (Direct3D 9)](locking-resources.md).

-   [**IDirect3DCubeTexture9:: Локкрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [**IDirect3DTexture9:: Локкрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [**IDirect3DVolumeTexture9:: защищенное хранилище**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

Методы блокировки принимают аргументы, обозначающие содержащуюся поверхность, например, вложенный уровень mipmap или грань куба текстуры, а также указатели на пиксели. Обычное приложение никогда не использует объект Surface напрямую.

Создайте ресурсы, ориентированные на геометрические вызовы, вызвав [**IDirect3DDevice9:: креатеиндексбуффер**](/windows/desktop/api) или [**IDirect3DDevice9:: креатевертексбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).

Заблокируйте и заполните ресурсы буфера, вызвав либо [**IDirect3DIndexBuffer9:: Lock**](/windows/desktop/api) , либо [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), в зависимости от ресурса.

Для управляемых ресурсов текстуры процесс создания ресурса завершается здесь. Для неуправляемых ресурсов текстуры приложение передает ресурсы системной памяти в ресурсы, доступные для устройства (для аппаратного ускорения) путем вызова [**IDirect3DDevice9:: упдатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

Для отображения изображений, подготовленных к просмотру из ресурсов, приложению также требуются буферы цветов и элементов глубины. Для типичных приложений буфер цвета принадлежит цепочке подкачки устройства, которая представляет собой коллекцию поверхностей заднего буфера и неявно создается на устройстве. Поверхности набора элементов глубины могут быть неявно созданы или явно созданы с помощью метода [**IDirect3DDevice9:: креатедепсстенЦилсурфаце**](/windows/desktop/api) . Приложение связывает устройство, его глубину и буфер цвета с вызовом [**IDirect3DDevice9:: сетрендертаржет**](/windows/desktop/api) или [**IDirect3DDevice9:: сетдепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).

Дополнительные сведения о представлении окончательного образа см. в разделе [представление сцены (Direct3D 9)](presenting-a-scene.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ресурсы Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
