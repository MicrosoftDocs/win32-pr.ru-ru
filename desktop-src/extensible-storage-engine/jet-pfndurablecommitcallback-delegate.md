---
description: 'Дополнительные сведения о: JET_PFNDURABLECOMMITCALLBACK делегата'
title: JET_PFNDURABLECOMMITCALLBACK делегат (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JET_PFNDURABLECOMMITCALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_pfndurablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104327
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.Invoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK..ctor
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.BeginInvoke
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9ff2f613138103be56db3fe7084202965a949cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913564"
---
# <a name="jet_pfndurablecommitcallback-delegate"></a><span data-ttu-id="7419f-103">JET_PFNDURABLECOMMITCALLBACK делегат</span><span class="sxs-lookup"><span data-stu-id="7419f-103">JET_PFNDURABLECOMMITCALLBACK delegate</span></span>

<span data-ttu-id="7419f-104">Обратный вызов для JET_paramDurableCommitCallback.</span><span class="sxs-lookup"><span data-stu-id="7419f-104">Callback for JET_paramDurableCommitCallback.</span></span>

<span data-ttu-id="7419f-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7419f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="7419f-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7419f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7419f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7419f-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNDURABLECOMMITCALLBACK ( _
    instance As JET_INSTANCE, _
    pCommitIdSeen As JET_COMMIT_ID, _
    grbit As DurableCommitCallbackGrbit _
) As JET_err
'Usage
Dim instance As New JET_PFNDURABLECOMMITCALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNDURABLECOMMITCALLBACK(
    JET_INSTANCE instance,
    JET_COMMIT_ID pCommitIdSeen,
    DurableCommitCallbackGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7419f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7419f-108">Parameters</span></span>

  - <span data-ttu-id="7419f-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="7419f-109">instance</span></span>  
    <span data-ttu-id="7419f-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7419f-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7419f-111">Используемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="7419f-111">Instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7419f-112">пкоммитидсин</span><span class="sxs-lookup"><span data-stu-id="7419f-112">pCommitIdSeen</span></span>  
    <span data-ttu-id="7419f-113">Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="7419f-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="7419f-114">Commit-ID, который только что был сброшен.</span><span class="sxs-lookup"><span data-stu-id="7419f-114">Commit-id that has just been flushed.</span></span>

<!-- end list -->

  - <span data-ttu-id="7419f-115">грбит</span><span class="sxs-lookup"><span data-stu-id="7419f-115">grbit</span></span>  
    <span data-ttu-id="7419f-116">Тип: [Microsoft. ISAM. ESENT. Interop. Windows8. дураблекоммиткаллбаккгрбит](./durablecommitcallbackgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7419f-116">Type: [Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7419f-117">Сейчас зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="7419f-117">Reserved currently.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7419f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7419f-118">Return value</span></span>

<span data-ttu-id="7419f-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7419f-119">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7419f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7419f-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7419f-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="7419f-121">Reference</span></span>

[<span data-ttu-id="7419f-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="7419f-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
