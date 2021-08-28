---
title: Общие сведения об устройстве в Direct3D 11
description: Объектная модель Direct3D 11 разделяет функции создания и отрисовки ресурсов в устройство и один или несколько контекстов. Это разделение предназначено для упрощения многопоточности.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9459574ad7d8732714ac54519294ae232e4d8d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475710"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a>Общие сведения об устройстве в Direct3D 11

Объектная модель Direct3D 11 разделяет функции создания и отрисовки ресурсов в устройство и один или несколько контекстов. Это разделение предназначено для упрощения многопоточности.

-   [Устройство](#introduction-to-a-device-in-direct3d-11)
-   [Контекст устройства](#device-context)
    -   [Контекст интерпретации](#immediate-context)
    -   [Отложенный контекст](#deferred-context)
-   [Особенности работы с потоками](#threading-considerations)
-   [Связанные темы](#related-topics)

## <a name="device"></a>Устройство

Устройство используется для создания ресурсов и перечисления возможностей видеоадаптера. В Direct3D 11 устройство представлено с интерфейсом [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .

К каждого приложения должно быть хотя бы одно устройство; большинство приложений создают только одно устройство. Создайте устройство для одного из драйверов оборудования, установленных на компьютере, вызвав [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) или [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) и указав тип драйвера с флагом [**\_ \_ типа драйвера D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Каждое устройство можно использовать один или несколько контекстов устройств, в зависимости от требуемой функциональности.

## <a name="device-context"></a>Контекст устройства

Контекст устройства содержит условия или настройки, в которых используется устройство. В частности, контекст устройства используется для задания состояния конвейера и создания команд отрисовки с использованием ресурсов, принадлежащих устройству. В Direct3D 11 реализованы два типа контекстов устройств: один для немедленной визуализации, другой — для отложенной отрисовки. Оба контекста представлены интерфейсом [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

### <a name="immediate-context"></a>Контекст интерпретации

Непосредственный контекст переводится непосредственно в драйвер. Каждое устройство имеет только один непосредственный контекст, который может получать данные из GPU. Непосредственный контекст можно использовать для немедленного отображения (или воспроизведения) [списка команд](overviews-direct3d-11-render-multi-thread-command-list.md).

Существует два способа получить непосредственный контекст:

-   Путем вызова либо [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) , либо [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).
-   Путем вызова [**ID3D11Device:: жетиммедиатеконтекст**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).

### <a name="deferred-context"></a>Отложенный контекст

Отложенный контекст записывает команды GPU в [список команд](overviews-direct3d-11-render-multi-thread-command-list.md). Отложенный контекст в основном используется для многопоточности и не является обязательным для однопотокового приложения. Отложенный контекст обычно используется рабочим потоком вместо основного потока отрисовки. При создании отложенного контекста он не наследует никаких состояний от непосредственных контекстов.

Чтобы получить отложенный контекст, вызовите метод [**ID3D11Device:: креатедеферредконтекст**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Любой контекст — немедленное или отложенное — может использоваться в любом потоке, если контекст используется только в одном потоке за раз.

## <a name="threading-considerations"></a>Особенности работы с потоками

В этой таблице показаны различия в модели потоков в Direct3D 11 от предыдущих версий Direct3D.




| | | Различия между Direct3D 11 и предыдущими версиями Direct3D:<br /> Все методы интерфейса <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> являются свободными потоками, что означает, что несколько потоков могут вызывать функции одновременно.<br /><ul><li>Все интерфейсы, производные от <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>и т. д.), являются свободными потоками.</li><li>Direct3D 11 разделяет ресурсы на создание и визуализацию в двух интерфейсах. Сопоставление, отмена сопоставления, начало, конец и метод GetData реализуются в <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ссылку ID3D11DeviceContext</strong></a> , так как <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> строго определяет порядок операций. Интерфейсы <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> и <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> также реализуют методы для операций, выполняемых в произвольных потоках.</li><li>Методы <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ссылку ID3D11DeviceContext</strong></a> (за исключением тех, которые существуют в <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) не являются потокобезопасными, то есть для них требуется единая Организация. Только один поток может безопасно вызывать любой из его методов (рисования, копирования, сопоставлений и т. д.) за раз.</li><li>Как правило, при свободной многопоточности уменьшается количество используемых примитивов синхронизации, а также их длительность. Однако приложение, которое использует синхронизацию в течение длительного времени, может напрямую влиять на то, сколько параллелизма может быть достигнуто приложением.</li></ul>Методы интерфейса ID3D10Device не предназначены для бессвинцовых потоков. ID3D10Device реализует все функции создания и отрисовки (как и ID3D9Device в Direct3D 9). Map и unend реализуются в интерфейсах, производных от ID3D10Resource, Begin, End и GetData реализуются в интерфейсах, производных от ID3D10Asynchronous.<br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Устройства](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





