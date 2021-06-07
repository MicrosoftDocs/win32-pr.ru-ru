---
title: Интерфейсы DirectML
description: Следующие интерфейсы объявляются в Директмл. h.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 64ae11c5b9a4298c340488499a5a309b71a2d48b
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521180"
---
# <a name="directml-interfaces"></a>Интерфейсы DirectML

Следующие интерфейсы объявляются в Директмл. h.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Создает устройство Директмл для данного устройства Direct3D 12. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Записывает Директмл работу в список команд Direct3D 12. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Представляет скомпилированную, эффективную форму оператора, подходящего для выполнения на GPU. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Управляет уровнем отладки Директмл. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Представляет устройство Директмл, которое используется для создания операторов, привязки таблиц, средств записи команд и других объектов. |
| [**IDMLDevice1**](/windows/desktop/api/directml/nn-directml-idmldevice1) | Представляет устройство Директмл, которое используется для создания операторов, привязки таблиц, средств записи команд и других объектов. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Интерфейс, реализованный всеми объектами, созданными на устройстве Директмл. |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Реализуется объектами, которые можно записать в список команд для диспетчеризации GPU с помощью [идмлкоммандрекордер:: рекорддиспатч](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). |
| [**IDMLObject**](/windows/desktop/api/directml/nn-directml-idmlobject) | Интерфейс, из которого [идмлдевице](/windows/win32/api/directml/nn-directml-idmldevice) и [идмлдевицечилд](/windows/desktop/api/directml/nn-directml-idmldevicechild) наследуют напрямую (и все остальные интерфейсы, косвенно). Следовательно, он предоставляет методы, общие для всех интерфейсов Директмл, а именно методы для связывания частных данных и для добавления заголовков к именам объектов. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Представляет оператор Директмл. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Представляет специализированный объект, цель которого — инициализировать скомпилированные операторы. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Реализуется объектами, которые могут быть исключены из памяти GPU, и поэтому могут быть предоставлены в [идмлдевице:: вытеснении](/windows/desktop/api/directml/nf-directml-idmldevice-evict) и [Идмлдевице:: макересидент](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident). |

## <a name="related-topics"></a>Связанные темы

* [Справочник по DirectML](direct3d-directml-reference.md)
* [Справочник по коду](direct3d-12-core-reference.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)
