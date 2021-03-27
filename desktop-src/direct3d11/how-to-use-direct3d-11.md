---
title: Использование Direct3D 11
description: В этом разделе показано, как использовать API Microsoft Direct3D 11 для выполнения нескольких распространенных задач.
ms.assetid: 9BDEDB68-3484-4683-85AF-B583971382C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45bc4dad63c5fc12f2077481172061fc317135a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792438"
---
# <a name="how-to-use-direct3d-11"></a>Использование Direct3D 11

В этом разделе показано, как использовать API Microsoft Direct3D 11 для выполнения нескольких распространенных задач.



| Раздел                                                                                                                         | Описание                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Как создать эталонное устройство](overviews-direct3d-11-devices-create-ref.md)<br/>                                  | В этом разделе показано, как создать эталонное устройство, которое реализует строго точную программную реализацию среды выполнения.<br/>                                                                                                                                                    |
| [Как создать устройство деформации](overviews-direct3d-11-devices-create-warp.md)<br/>                                      | В этом разделе показано, как создать устройство деформации, которое реализует средство программной прорисовки с высокой скоростью.<br/>                                                                                                                                                                                  |
| [Как создать цепочку буферов](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                 | В этом разделе показано, как создать цепочку подкачки, которая инкапсулирует два или больше буферов, используемых для отрисовки и отображения. <br/>                                                                                                                                                      |
| [Руководство. Перечисление адаптеров](overviews-direct3d-11-devices-enum.md)<br/>                                               | В этом разделе показано, как использовать графическую инфраструктуру Microsoft DirectX (DXGI) для перечисления доступных графических адаптеров на компьютере.<br/>                                                                                                                                        |
| [Как получить режимы отображения адаптера](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                            | В этом разделе показано, как использовать DXGI для получения допустимых режимов отображения, связанных с адаптером.<br/>                                                                                                                                                                                     |
| [Как создать устройство и немедленный контекст](overviews-direct3d-11-devices-initialize.md)<br/>                      | В этом разделе показано, как инициализировать [устройство](overviews-direct3d-11-devices-intro.md).<br/>                                                                                                                                                                                        |
| [Как получить уровень функций устройства](overviews-direct3d-11-devices-downlevel-get.md)<br/>                            | В этом разделе показано, как получить максимальный [уровень функций](overviews-direct3d-11-devices-downlevel-intro.md) , поддерживаемый [устройством](overviews-direct3d-11-devices-intro.md).<br/>                                                                                                   |
| [Как создать буфер вершин](overviews-direct3d-11-resources-buffers-vertex-how-to.md)<br/>                        | В этом разделе показано, как инициализировать статический [буфер вершин](overviews-direct3d-11-resources-buffers-intro.md), то есть буфер вершин, который не изменяется.<br/>                                                                                                                  |
| [Как создать буфер индексов](overviews-direct3d-11-resources-buffers-index-how-to.md)<br/>                         | В этом разделе показано, как инициализировать [буфер индексов](overviews-direct3d-11-resources-buffers-intro.md) при подготовке к подготовке к просмотру.<br/>                                                                                                                                           |
| [Как создать буфер константы](overviews-direct3d-11-resources-buffers-constant-how-to.md)<br/>                    | В этом разделе показано, как инициализировать [Константный буфер](overviews-direct3d-11-resources-buffers-intro.md) при подготовке к подготовке к просмотру.<br/>                                                                                                                                         |
| [Как создать текстуру](overviews-direct3d-11-resources-textures-create.md)<br/>                                    | В этом разделе показано, как создать текстуру.<br/>                                                                                                                                                                                                                                       |
| [Как программно инициализировать текстуру](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)<br/> | В этом разделе есть несколько примеров, показывающих, как инициализировать текстуры, созданные с использованием различных типов использования.<br/>                                                                                                                                                             |
| [Как инициализировать текстуру из файла](overviews-direct3d-11-resources-textures-how-to.md)<br/>                    | В этом разделе показано, как использовать компонент Windows Imaging Component (WIC) для создания текстуры и представления отдельно.<br/>                                                                                                                                                                      |
| [Как использовать динамические ресурсы](how-to--use-dynamic-resources.md)<br/>                                                 | Вы создаете и используете динамические ресурсы, когда приложению требуется изменить данные в этих ресурсах. Можно создавать текстуры и буферы для динамического использования.<br/>                                                                                                                              |
| [Как создать вычисление шейдера](direct3d-11-advanced-stages-compute-create.md)<br/>                                  | В этом разделе показано, как создать вычисление шейдера.<br/>                                                                                                                                                                                                                                |
| [Руководство. Проектирование шейдера поверхности](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                 | В этом разделе показано, как спроектировать поверхности шейдер.<br/>                                                                                                                                                                                                                                  |
| [Руководство. Создание шейдера поверхности](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                 | В этом разделе показано, как создать шейдер поверхности.<br/>                                                                                                                                                                                                                                   |
| [Поэтапное руководство. Инициализация этапа тесселяции](direct3d-11-advanced-stages-tessellator-initialize.md)<br/>                 | В этом разделе показано, как инициализировать этап тесселяции.<br/>                                                                                                                                                                                                                       |
| [Руководство. Проектирование шейдера доменов](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                             | В этом разделе показано, как спроектировать Шейдер доменов.<br/>                                                                                                                                                                                                                                |
| [Как создать Шейдер доменов](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                             | В этом разделе показано, как создать шейдер домена.<br/>                                                                                                                                                                                                                                 |
| [Как скомпилировать шейдер](how-to--compile-a-shader.md)<br/>                                                           | В этом разделе показано, как использовать функцию [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) во время выполнения для компиляции кода шейдера.<br/>                                                                                                                                          |
| [Как записать список команд](overviews-direct3d-11-render-multi-thread-command-list-record.md)<br/>                 | В этом разделе показано, как создать и записать [список команд](overviews-direct3d-11-render-multi-thread-command-list.md).<br/>                                                                                                                                                         |
| [Как воспроизвести список команд](overviews-direct3d-11-render-multi-thread-command-list-play.md)<br/>                | В этом разделе показано, как воспроизвести [список команд](overviews-direct3d-11-render-multi-thread-command-list.md).<br/>                                                                                                                                                                 |
| [Как проверить наличие поддержки драйверов](overviews-direct3d-11-render-multi-thread-support.md)<br/>                          | В этом разделе показано, как определить, поддерживаются ли для аппаратного ускорения возможности многопотоковой обработки (включая [Создание ресурсов](overviews-direct3d-11-render-multi-thread-intro.md) и [списки команд](overviews-direct3d-11-render-multi-thread-command-list.md)).<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Графика Direct3D 11](atoc-dx-graphics-direct3d-11.md)
</dt> </dl>

 

