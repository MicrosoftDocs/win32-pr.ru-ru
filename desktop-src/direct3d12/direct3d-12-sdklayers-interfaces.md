---
title: Интерфейсы слоя отладки
description: Следующие интерфейсы объявляются в d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d7e16d6c593f2dcfcc46266102ac15a61386ef
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812876"
---
# <a name="debug-layer-interfaces"></a>Интерфейсы слоя отладки

Следующие интерфейсы определяются в `d3d12sdklayers.h` .

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**ID3D12Debug**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Интерфейс отладки управляет параметрами отладки и проверяет состояние конвейера. Его можно использовать только в том случае, если включен слой отладки. |
| [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Добавляется проверка на основе GPU и зависимая очередь команд на уровне отладки. |
| [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Добавляет настраиваемые уровни проверки GPU-Based. |
| [**ID3D12Debug3**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Добавляет в отладочный слой проверку на основе GPU, зависимую синхронизацию очереди команд и настраиваемые уровни проверки на основе GPU. |
| [**ID3D12Debug4**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug4) | Добавляет возможность отключения слоя отладки. |
| [**ID3D12Debug5**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug5) | Добавляет к слою отладки возможность настройки автоматического именования объектов. |
| [**ID3D12DebugCommandList**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Предоставляет методы для мониторинга и отладки списка команд. |
| [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Этот интерфейс позволяет изменять параметры слоя отладки дополнительных списков команд. |
| [**ID3D12DebugCommandQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Предоставляет методы для мониторинга и отладки очереди команд. |
| [**ID3D12DebugDevice**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Этот интерфейс представляет графическое устройство для отладки. |
| [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Задает параметры уровня отладки для всего устройства. |
| [**ID3D12InfoQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Интерфейс очереди информации хранит, извлекает и фильтрует сообщения отладки. Очередь состоит из очереди сообщений, дополнительного стека фильтра хранилища и дополнительного стека фильтров получения. |
| [**ID3D12SharingContract**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Часть контракта между диагностическими слоями D3D11On12 и инструментами диагностики графики. |

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка среды программирования для Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Справочник по слою отладки](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Справочник по Direct3D 12](direct3d-12-reference.md)
</dt> </dl>