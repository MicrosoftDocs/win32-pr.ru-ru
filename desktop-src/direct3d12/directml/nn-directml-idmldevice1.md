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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803737"
---
# <a name="idmldevice1-interface-directmlh"></a><span data-ttu-id="50a57-103">Интерфейс IDMLDevice1 (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="50a57-103">IDMLDevice1 interface (directml.h)</span></span>

<span data-ttu-id="50a57-104">Представляет устройство Директмл, которое используется для создания операторов, привязки таблиц, средств записи команд и других объектов.</span><span class="sxs-lookup"><span data-stu-id="50a57-104">Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.</span></span> <span data-ttu-id="50a57-105">Интерфейс **IDMLDevice1** наследует от [идмлдевице](/windows/win32/api/directml/nn-directml-idmldevice).</span><span class="sxs-lookup"><span data-stu-id="50a57-105">The **IDMLDevice1** interface inherits from [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

<span data-ttu-id="50a57-106">Устройство Директмл всегда связано только с одним базовым устройством Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="50a57-106">A DirectML device is always associated with exactly one underlying Direct3D 12 device.</span></span> <span data-ttu-id="50a57-107">Все объекты, созданные устройством Директмл, поддерживают строгую ссылку на их родительское устройство.</span><span class="sxs-lookup"><span data-stu-id="50a57-107">All objects created by the DirectML device maintain a strong reference to their parent device.</span></span> <span data-ttu-id="50a57-108">В отличие от устройства Direct3D 12, устройство DML не является Singleton-классом.</span><span class="sxs-lookup"><span data-stu-id="50a57-108">Unlike the Direct3D 12 device, the DML device is not a singleton.</span></span> <span data-ttu-id="50a57-109">Таким образом, можно создать несколько устройств Директмл на одном устройстве Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="50a57-109">Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device.</span></span> <span data-ttu-id="50a57-110">Однако это не рекомендуется делать, так как устройство Директмл не имеет изменяющегося состояния, поэтому существует небольшое преимущество создания нескольких устройств DML на одном устройстве Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="50a57-110">However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.</span></span>

<span data-ttu-id="50a57-111">Этот объект является потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="50a57-111">This object is thread-safe.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50a57-112">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="50a57-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="50a57-113">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="50a57-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="availability"></a><span data-ttu-id="50a57-114">Доступность</span><span class="sxs-lookup"><span data-stu-id="50a57-114">Availability</span></span>
<span data-ttu-id="50a57-115">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="50a57-115">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="50a57-116">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="50a57-116">Tensor constraints</span></span>
<span data-ttu-id="50a57-117">**Целевая платформа**: Windows</span><span class="sxs-lookup"><span data-stu-id="50a57-117">**Target Platform**: Windows</span></span>


## <a name="inheritance"></a><span data-ttu-id="50a57-118">Наследование</span><span class="sxs-lookup"><span data-stu-id="50a57-118">Inheritance</span></span>


<span data-ttu-id="50a57-119">Интерфейс IDMLDevice1 наследуется от интерфейса Идмлдевице.</span><span class="sxs-lookup"><span data-stu-id="50a57-119">The IDMLDevice1 interface inherits from the IDMLDevice interface.</span></span>



## <a name="methods"></a><span data-ttu-id="50a57-120">Методы</span><span class="sxs-lookup"><span data-stu-id="50a57-120">Methods</span></span>

<p><span data-ttu-id="50a57-121">Интерфейс <b>IDMLDevice1</b> содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="50a57-121">The <b>IDMLDevice1</b> interface has these methods.</span></span></p>

| <span data-ttu-id="50a57-122">Метод</span><span class="sxs-lookup"><span data-stu-id="50a57-122">Method</span></span> | <span data-ttu-id="50a57-123">Описание</span><span class="sxs-lookup"><span data-stu-id="50a57-123">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="50a57-124">IDMLDevice1:: Компилеграф</span><span class="sxs-lookup"><span data-stu-id="50a57-124">IDMLDevice1::CompileGraph</span></span>](../directml/nf-directml-idmldevice1-compilegraph.md) | <span data-ttu-id="50a57-125">Компилирует граф операторов Директмл в объект, который можно отправить в GPU.</span><span class="sxs-lookup"><span data-stu-id="50a57-125">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span> |


## <a name="requirements"></a><span data-ttu-id="50a57-126">Требования</span><span class="sxs-lookup"><span data-stu-id="50a57-126">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="50a57-127">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="50a57-127">**Target Platform**</span></span> | <span data-ttu-id="50a57-128">Windows</span><span class="sxs-lookup"><span data-stu-id="50a57-128">Windows</span></span> |
| <span data-ttu-id="50a57-129">**Header**</span><span class="sxs-lookup"><span data-stu-id="50a57-129">**Header**</span></span> | <span data-ttu-id="50a57-130">директмл. h</span><span class="sxs-lookup"><span data-stu-id="50a57-130">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="50a57-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50a57-131">See also</span></span>

[<span data-ttu-id="50a57-132">Интерфейс Идмлдевице</span><span class="sxs-lookup"><span data-stu-id="50a57-132">IDMLDevice interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)