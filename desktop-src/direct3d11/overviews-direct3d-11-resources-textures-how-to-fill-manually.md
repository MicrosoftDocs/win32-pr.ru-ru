---
title: Программная инициализация текстуры
description: В этом разделе есть несколько примеров, показывающих, как инициализировать текстуры, созданные с использованием различных типов использования.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888660"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>Как программно инициализировать текстуру

Вы можете инициализировать текстуру во время создания объекта или заполнять объект программным способом после его создания. В этом разделе есть несколько примеров, показывающих, как инициализировать текстуры, созданные с использованием различных типов использования. В этом примере предполагается, что вы уже знакомы с [созданием текстуры](overviews-direct3d-11-resources-textures-create.md).

-   [Использование по умолчанию](#default-usage)
-   [Динамическое использование](#dynamic-usage)
-   [Использование промежуточного хранения](#staging-usage)
-   [См. также](#related-topics)

## <a name="default-usage"></a>Использование по умолчанию

Наиболее распространенным типом использования является использование по умолчанию. Чтобы заполнить текстуру по умолчанию (созданную с использованием **D3D11 \_ \_ по умолчанию**), можно выполнить одно из следующих действий.

-   Вызовите [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) и инициализируйте *пинитиалдата* , чтобы указать данные, предоставленные приложением.

    или

-   После вызова [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)используйте [**ссылку ID3D11DeviceContext:: упдатесубресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) для заполнения текстуры по умолчанию данными из указателя, предоставленного приложением.

## <a name="dynamic-usage"></a>Динамическое использование

Для заполнения динамической текстуры (созданной с использованием **D3D11 \_ \_ dynamic**):

1.  Получите указатель на память текстуры, передав при вызове [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) **D3D11- \_ \_ запись \_** .
2.  Запись данных в память.
3.  По завершении записи данных вызовите метод [**ссылку ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) uncall.

## <a name="staging-usage"></a>Использование промежуточного хранения

Для заполнения промежуточной текстуры (созданной с использованием **\_ \_ промежуточного хранения D3D11**):

1.  Получите указатель на память текстуры, передав **D3D11 \_ Map \_ Write** при вызове [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Запись данных в память.
3.  По завершении записи данных вызовите метод [**ссылку ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) uncall.

После этого промежуточная текстура может использоваться в качестве исходного параметра для [**ссылку ID3D11DeviceContext:: копиресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) или [**ссылку ID3D11DeviceContext:: кописубресаурцерегион**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) для заполнения по умолчанию или динамического ресурса.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Текстуры](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




