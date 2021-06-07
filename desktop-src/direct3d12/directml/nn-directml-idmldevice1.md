---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Представляет устройство Директмл, которое используется для создания операторов, привязки таблиц, средств записи команд и других объектов.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417444"
---
# <a name="idmldevice1-interface-directmlh"></a>Интерфейс IDMLDevice1 (директмл. h)

Представляет устройство Директмл, которое используется для создания операторов, привязки таблиц, средств записи команд и других объектов. Интерфейс **IDMLDevice1** наследует от [идмлдевице](/windows/win32/api/directml/nn-directml-idmldevice).

Устройство Директмл всегда связано только с одним базовым устройством Direct3D 12. Все объекты, созданные устройством Директмл, поддерживают строгую ссылку на их родительское устройство. В отличие от устройства Direct3D 12, устройство DML не является Singleton-классом. Таким образом, можно создать несколько устройств Директмл на одном устройстве Direct3D 12. Однако это не рекомендуется делать, так как устройство Директмл не имеет изменяющегося состояния, поэтому существует небольшое преимущество создания нескольких устройств DML на одном устройстве Direct3D 12.

Этот объект является потокобезопасным.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="availability"></a>Доступность
Этот API появился в версии Директмл `1.1.0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
**Целевая платформа**: Windows


## <a name="inheritance"></a>Наследование


Интерфейс IDMLDevice1 наследуется от интерфейса Идмлдевице.



## <a name="methods"></a>Методы

<p>Интерфейс <b>IDMLDevice1</b> содержит следующие методы.</p>

| Метод | Описание |
| ---- |:---- |
| [IDMLDevice1:: Компилеграф](../directml/nf-directml-idmldevice1-compilegraph.md) | Компилирует граф операторов Директмл в объект, который можно отправить в GPU. |


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | директмл. h |

## <a name="see-also"></a>См. также раздел

[Интерфейс Идмлдевице](/windows/win32/api/directml/nn-directml-idmldevice)