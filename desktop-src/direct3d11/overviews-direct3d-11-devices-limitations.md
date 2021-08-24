---
title: Ограничения на создание ИСКРИВЛЕНных и эталонных устройств
description: Существуют некоторые ограничения на создание ИСКРИВЛЕНных и ссылочных устройств в Direct3D 10,1 и Direct3D 11,0. В этом разделе обсуждаются эти ограничения.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483ed6d5fd7348df39a4f3064f377845d6bfae1fe46abc47be5acd99e191c29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608614"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>Ограничения на создание ИСКРИВЛЕНных и эталонных устройств

Существуют некоторые ограничения на создание ИСКРИВЛЕНных и ссылочных устройств в Direct3D 10,1 и Direct3D 11,0. В этом разделе обсуждаются эти ограничения.

Типы драйверов типов драйвера D3D10 \_ \_ и драйвера D3D10 для типов драйверов \_ \_ \_ \_ не поддерживаются на \_ уровне компонентов D3D10 с \_ уровня \_ 9 \_ 1 до D3D10 компонентов уровня \_ \_ \_ \_ 4 3 в Direct3D 10,1. Кроме того, тип драйвера " \_ деформация" типа драйвера D3D \_ \_ не поддерживается на \_ уровне функции D3D \_ \_ 11 \_ 0 в Direct3D 11,0. Это значит, что при вызове [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) для создания устройства Direct3D 10,1 или при вызове [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) для создания устройства Direct3D 11,0, если указать сочетание одного из этих типов драйверов с одним из этих уровней функций в вызове, вызов будет недопустимым. Для деформации и ссылочных устройств допустимы только следующие сочетания уровней компонентов, сред выполнения и типов драйверов:

-   \_тип драйвера \_ D3D \_ перекоса на всех уровнях компонентов в Direct3D 11,1, которые Windows 8 включают

    \_ \_ Справочник по типам драйверов D3D \_ на всех уровнях компонентов в Direct3D 11,1

    При вызове [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) для создания устройства Direct3D 11,1 вызов допустим, если указать сочетание одного из этих типов драйверов с одним из этих уровней.

-   \_Тип драйвера D3D. \_ \_ деформация на \_ уровне компонента D3D \_ \_ 9 \_ 1 через \_ уровни компонентов D3D \_ уровня \_ 10 \_ 1 в Direct3D 11

    \_ \_ Справочник по типам драйверов D3D \_ на \_ уровне D3D-функции \_ \_ 9 с на \_ уровнях компонентов D3D \_ \_ уровня \_ 11 \_ 0 в Direct3D 11

    При вызове [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) для создания устройства Direct3D 11 вызов допустим, если указать сочетание одного из этих типов драйверов с одним из этих уровней.

-   \_Тип драйвера D3D10. \_ \_ \_ \_ Справочник по типам драйверов D3D10 \_ для D3D10 \_ на \_ уровне \_ 10 \_ 0 до D3D10 уровня компонентов 10 \_ \_ \_ \_ 1 в Direct3D 10,1

    При вызове [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) для создания устройства Direct3D 10,1 вызов допустим, если указать сочетание одного из этих типов драйверов с одним из этих уровней.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Устройства](overviews-direct3d-11-devices.md)
</dt> <dt>

[Введение в Direct3D 11 на оборудовании нижнего уровня](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[Как создать устройство деформации](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[Как создать эталонное устройство](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**\_Тип драйвера \_ D3D10**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**D3D10 \_ функция \_ level1**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**\_Тип драйвера \_ D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**\_Уровень компонента \_ D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 