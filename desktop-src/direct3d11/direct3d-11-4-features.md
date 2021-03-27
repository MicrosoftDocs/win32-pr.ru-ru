---
title: Функции Direct3D 11,4
description: В Direct3D 11,4 добавлены следующие функциональные возможности.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987668"
---
# <a name="direct3d-114-features"></a>Функции Direct3D 11,4

В Direct3D 11,4 добавлены следующие функциональные возможности.

Также посмотрите [, где находится пакет SDK DirectX?](../directx-sdk--august-2009-.md)

## <a name="direct3d-device-removal"></a>Удаление устройства Direct3D

Методы [**регистердевицеремоведевент**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)и [**унрегистердевицеремовед**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) поддерживаются новым интерфейсом [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4)для поддержки получения асинхронного уведомления о событии при удалении устройства Direct3D.

## <a name="multithreaded-protection"></a>Многопоточная защита

Чтобы гарантировать, что команды графики в частности выполняются в определенном порядке, интерфейс [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) имеет методы для включения и отключения многопотоковой защиты, а также методы для входа и выхода из критического кода, которому требуется эта защита.

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>Ограждения для синхронизации нескольких устройств и взаимодействия с Direct3D 12

[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) и [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) предоставляют те же функции ограждения, что и Direct3D 12 для Direct3D 11. Границы используются для синхронизации нескольких устройств Direct3D11 и для взаимодействия между Direct3D 11 и Direct3D 12. Границы поддерживаются в обновлении Windows 10 для дизайнеров.

## <a name="extended-nv12-texture-support"></a>Расширенная поддержка текстур NV12

Текстуры NV12 с возможностями записи и кодирования видео теперь поддерживают совместное использование. Более старые флаги текстуры D3D11 для кодирования и записи видео являются устаревшими для NV12, так как они будут установлены в течение всего времени для новых драйверов. Такие текстуры могут использоваться не только с D3D11, но и с D3D12. В D3D12 новые флаги не представляют эти возможности текстуры.

См. логический параметр в [**D3D11 \_ Data Feature \_ \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).

## <a name="shader-caching"></a>Кэширование шейдера

Драйверы могут поддерживать кэширование шейдера, управляемого операционной системой, для Direct3D11 приложений в обновлении Windows 10 Creators Update.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Новые возможности Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 