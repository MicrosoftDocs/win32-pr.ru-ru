---
title: Основные интерфейсы (графика Direct3D 12)
description: Следующие интерфейсы объявляются в d3d12. h.
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: f204484b3565564f72e815bd21cf8e449ee55e4c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884298"
---
# <a name="core-interfaces"></a>Базовые интерфейсы

Следующие интерфейсы объявляются в d3d12. h.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | Представляет выделение памяти для команд графического процессора (GPU). |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | Интерфейс, от которого наследуется [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) . Он представляет упорядоченный набор команд, выполняемых GPU, и позволяет расширению поддерживать другие списки команд, чем просто для графики (например, для вычислений и копирования). |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | Предоставляет методы для отправки списков команд, синхронизации выполнения списка команд, инструментирования очереди команд и обновления сопоставлений плиток ресурсов. |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | Объект сигнатуры команды позволяет приложениям указывать косвенное рисование, включая формат буфера, тип команды и привязки ресурсов, которые будут использоваться. |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | Куча дескрипторов — это набор смежных выделений дескрипторов, по одному выделению для каждого из них. Кучи дескрипторов содержат множество типов объектов, которые не являются частью объекта состояния конвейера (PSO), например представления ресурсов шейдера (СРВС), неупорядоченные представления доступа (Уавс), представления постоянного буфера (КБВС) и пробы. |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | Представляет виртуальный адаптер; Он используется для создания распределителя команд, списков команд, очередей команд, ограждений, ресурсов, объектов состояния конвейера, куч, корневых подписей, проб и многих представлений ресурсов. |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | Представляет виртуальный адаптер и разворачивается в диапазоне методов, предоставляемых [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device). |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | Представляет виртуальный адаптер. Этот интерфейс расширяет [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) для создания объектов состояния конвейера из описаний потока состояния конвейера. |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | Представляет виртуальный адаптер. Этот интерфейс расширяет [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) для поддержки создания специальных диагностических куч в системной памяти, которые сохраняются даже в случае сбоя GPU или устройств. |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | Представляет виртуальный адаптер. Этот интерфейс расширяет [ID3D12Device3](/windows/win32/api/d3d12/nn-d3d12-id3d12device3). |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | Представляет виртуальный адаптер. Этот интерфейс расширяет [ID3D12Device4](/windows/win32/api/d3d12/nn-d3d12-id3d12device4). |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | Представляет виртуальный адаптер. Этот интерфейс расширяет [ID3D12Device5](/windows/win32/api/d3d12/nn-d3d12-id3d12device5). |
| [**ID3D12Device7**](/windows/win32/api/d3d12/nn-d3d12-id3d12device7) | Представляет виртуальный адаптер. Этот интерфейс расширяет [ID3D12Device6](/windows/win32/api/d3d12/nn-d3d12-id3d12device6). |
| [**ID3D12Device8**](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) | Представляет виртуальный адаптер. Этот интерфейс расширяет [ID3D12Device7](/windows/win32/api/d3d12/nn-d3d12-id3d12device7). |
| [**ID3D12Device9**](/windows/win32/api/d3d12/nn-d3d12-id3d12device9) | Представляет виртуальный адаптер. Этот интерфейс расширяет [ID3D12Device8](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) , добавляя методы для управления кэшами шейдеров. |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | Интерфейс, от которого наследуются другие базовые интерфейсы, включая [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary), [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist), [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)и [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature). Он предоставляет метод для возврата к объекту устройства, для которого он был создан. |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | Предоставляет доступ среды выполнения к удаленным устройствам данных расширенных данных (НАПРАВЛЯТЬ). |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | Этот интерфейс управляет устройствами, удаленными с параметрами расширенных данных (НАПРАВЛЯТЬ). |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | Представляет ограждение, объект, используемый для синхронизации ЦП и один или несколько GPU.  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | Представляет ограждение. Этот интерфейс расширяет [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)и поддерживает получение флагов, используемых для создания исходной границы.  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | Инкапсулирует список графических команд для подготовки к просмотру. Включает API для инструментирования выполнения списка команд, а также для настройки и очистки состояния конвейера. |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | Инкапсулирует список графических команд для подготовки к просмотру, расширяя реализовывать для поддержки программируемых положений выборки, атомарных копий для реализации методов поздней блокировки и необязательного тестирования с учетом глубины. |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | Инкапсулирует список графических команд для подготовки к просмотру, расширяя интерфейс для поддержки записи непосредственных значений непосредственно в буфер. |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | Инкапсулирует список графических команд для подготовки к просмотру. |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | Инкапсулирует список графических команд для подготовки к просмотру, расширяя интерфейс для поддержки трассировки лучей и прохода прорисовки. |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | Куча представляет собой абстракцию непрерывного выделения памяти, используемой для управления физической памятью. Эту кучу можно использовать с объектами [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) для поддержки размещенных ресурсов или зарезервированных ресурсов. |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | Представляет определенный приложением обратный вызов, используемый для получения уведомлений об изменениях времени существования объекта. |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | Представляет средства для управления временем существования объекта, отслеживающего время существования. |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | Представляет мета-команду. Meta-команда — это объект Direct3D 12, представляющий алгоритм, который ускоряется независимыми поставщиками оборудования (IHV). Это непрозрачная ссылка на генератор команд, реализованный драйвером. |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | Интерфейс, от которого наследуются [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) и [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) . Он предоставляет методы для связывания закрытых данных и добавления аннотаций к именам объектов. |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | Интерфейс, от которого наследуются многие другие базовые интерфейсы. Он указывает, что тип объекта инкапсулирует некоторый объем доступной памяти GPU; но не строго указывает, может ли приложение манипулировать местонахождение объекта.  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | Управляет библиотекой конвейера при определенной загрузке и извлечении отдельных псос. |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | Управляет библиотекой конвейера. Этот интерфейс расширяет [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) для загрузки псос из описания потока состояния конвейера. |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | Представляет состояние всех текущих заданных шейдеров, а также определенных объектов состояния фиксированной функции. |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | Управляет кучей запроса. Куча запросов содержит массив запросов, на которые ссылаются индексы. |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | Инкапсулирует обобщенные возможности ЦП и GPU для чтения и записи в физическую память или кучи. Он содержит абстракции для Организации и управления простыми массивами данных, а также многомерные данные, оптимизированные для выборки шейдера. |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | Корневая подпись определяет, какие ресурсы привязаны к графическому конвейеру. Корневая подпись настраивается приложением и связывает списки команд с ресурсами, которые требуются шейдеру. В настоящее время для каждого приложения существует одна графика и одна из корневых подписей вычислений. |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | Содержит метод, возвращающий десериализованную структуру данных [**D3D12-root-Signature-DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) для сериализованной корневой сигнатуры версии 1,0.  |
| [**ID3D12SDKConfiguration**](/windows/win32/api/d3d12/nn-d3d12-id3d12sdkconfiguration) | Предоставляет методы конфигурации пакета SDK. |
| [**ID3D12ShaderCacheSession**](/windows/win32/api/d3d12/nn-d3d12-id3d12shadercachesession) | Представляет сеанс кэша шейдера. |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | Представляет переменный объем состояния конфигурации, включая шейдеры, которые приложение управляет как единое целое и которое предоставляется драйверу для атомарного выполнения, например для компиляции или оптимизации.  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | Предоставляет методы для получения и установки свойств объекта [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject).  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | Этот интерфейс используется для настройки среды выполнения для таких средств, как PIX. Он не предназначен для любого другого сценария или не поддерживается. |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | Содержит методы для возврата десериализованной структуры данных [**D3D12-root-Signature-DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) для любой версии сериализованной корневой сигнатуры.  |

## <a name="related-topics"></a>Связанные темы

* [Справочник по коду](direct3d-12-core-reference.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)
* [Иерархия интерфейса](interface-hierarchy.md)
