---
title: Интерфейсы слоя отладки
description: Следующие интерфейсы объявляются в d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2020
ms.locfileid: "105650322"
---
# <a name="debug-layer-interfaces"></a>Интерфейсы слоя отладки

Следующие интерфейсы определяются в `d3d12sdklayers.h` .

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**ID3D12Debug**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Интерфейс отладки управляет параметрами отладки и проверяет состояние конвейера. Его можно использовать только в том случае, если включен слой отладки. |
| [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Добавляется проверка на основе GPU и зависимая очередь команд на уровне отладки. |
| [**ID3D12Debug2**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Добавляет настраиваемые уровни проверки GPU-Based. |
| [**ID3D12Debug3**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Добавляет в отладочный слой проверку на основе GPU, зависимую синхронизацию очереди команд и настраиваемые уровни проверки на основе GPU. |
| [**ID3D12DebugCommandList**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Предоставляет методы для мониторинга и отладки списка команд. |
| [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Этот интерфейс позволяет изменять параметры слоя отладки дополнительных списков команд. |
| [**ID3D12DebugCommandQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Предоставляет методы для мониторинга и отладки очереди команд. |
| [**ID3D12DebugDevice**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Этот интерфейс представляет графическое устройство для отладки. |
| [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Задает параметры уровня отладки для всего устройства. |
| [**ID3D12InfoQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Интерфейс очереди информации хранит, извлекает и фильтрует сообщения отладки. Очередь состоит из очереди сообщений, дополнительного стека фильтра хранилища и дополнительного стека фильтров получения. |
| [**ID3D12SharingContract**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Часть контракта между диагностическими слоями D3D11On12 и инструментами диагностики графики. |

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка среды программирования для Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Справочник по слою отладки](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Справочник по Direct3D 12](direct3d-12-reference.md)
</dt> </dl>