---
description: 'Дополнительные сведения о: конструктор Дураблекоммиткаллбакк'
title: Конструктор Дураблекоммиткаллбакк (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'DurableCommitCallback constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.durablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.DurableCommitCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade1952615b98d9ea41a7a1b83d0bf1a3c6fc8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817576"
---
# <a name="durablecommitcallback-constructor"></a><span data-ttu-id="e0adc-103">Конструктор Дураблекоммиткаллбакк</span><span class="sxs-lookup"><span data-stu-id="e0adc-103">DurableCommitCallback constructor</span></span>

<span data-ttu-id="e0adc-104">Инициализирует новый экземпляр класса [дураблекоммиткаллбакк](./durablecommitcallback-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e0adc-104">Initializes a new instance of the [DurableCommitCallback](./durablecommitcallback-class.md) class.</span></span>

<span data-ttu-id="e0adc-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e0adc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="e0adc-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e0adc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e0adc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0adc-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE, _
    wrappedCallback As JET_PFNDURABLECOMMITCALLBACK _
)
'Usage
Dim instance As JET_INSTANCE
Dim wrappedCallback As JET_PFNDURABLECOMMITCALLBACK

Dim instance As New DurableCommitCallback(instance, _
    wrappedCallback)
```

``` csharp
public DurableCommitCallback(
    JET_INSTANCE instance,
    JET_PFNDURABLECOMMITCALLBACK wrappedCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="e0adc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0adc-108">Parameters</span></span>

  - <span data-ttu-id="e0adc-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="e0adc-109">instance</span></span>  
    <span data-ttu-id="e0adc-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e0adc-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="e0adc-111">Экземпляр, с которым необходимо связать обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="e0adc-111">The instance with which to associate the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="e0adc-112">враппедкаллбакк</span><span class="sxs-lookup"><span data-stu-id="e0adc-112">wrappedCallback</span></span>  
    <span data-ttu-id="e0adc-113">Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="e0adc-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span></span>  
    
    <span data-ttu-id="e0adc-114">Обратный вызов управляемого кода для вызова.</span><span class="sxs-lookup"><span data-stu-id="e0adc-114">The managed code callback to call.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0adc-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0adc-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e0adc-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="e0adc-116">Reference</span></span>

[<span data-ttu-id="e0adc-117">Класс Дураблекоммиткаллбакк</span><span class="sxs-lookup"><span data-stu-id="e0adc-117">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="e0adc-118">Элементы Дураблекоммиткаллбакк</span><span class="sxs-lookup"><span data-stu-id="e0adc-118">DurableCommitCallback members</span></span>](./durablecommitcallback-members.md)

[<span data-ttu-id="e0adc-119">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="e0adc-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
