---
description: 'Дополнительные сведения о методе: Windows8Api. JetStopServiceInstance2'
title: Windows8Api. JetStopServiceInstance2, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetStopServiceInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetstopserviceinstance2(v=EXCHG.10)
ms:contentKeyID: 55104460
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0821a00016eb9cd2c511ee37889e0ddaa0b76edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080409"
---
# <a name="windows8apijetstopserviceinstance2-method"></a><span data-ttu-id="91100-103">Windows8Api. JetStopServiceInstance2, метод</span><span class="sxs-lookup"><span data-stu-id="91100-103">Windows8Api.JetStopServiceInstance2 method</span></span>

<span data-ttu-id="91100-104">Подготавливает экземпляр к завершению.</span><span class="sxs-lookup"><span data-stu-id="91100-104">Prepares an instance for termination.</span></span> <span data-ttu-id="91100-105">Также можно использовать для возобновления предыдущего замораживания.</span><span class="sxs-lookup"><span data-stu-id="91100-105">Can also be used to resume a previous quiescing.</span></span>

<span data-ttu-id="91100-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="91100-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="91100-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="91100-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="91100-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91100-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetStopServiceInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As StopServiceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As StopServiceGrbitWindows8Api.JetStopServiceInstance2(instance, _
    grbit)
```

``` csharp
public static void JetStopServiceInstance2(
    JET_INSTANCE instance,
    StopServiceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="91100-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="91100-109">Parameters</span></span>

  - <span data-ttu-id="91100-110">экземпляр</span><span class="sxs-lookup"><span data-stu-id="91100-110">instance</span></span>  
    <span data-ttu-id="91100-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="91100-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="91100-112">Используемый экземпляр (выполняющийся).</span><span class="sxs-lookup"><span data-stu-id="91100-112">The (running) instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="91100-113">грбит</span><span class="sxs-lookup"><span data-stu-id="91100-113">grbit</span></span>  
    <span data-ttu-id="91100-114">Тип: [Microsoft. ISAM. ESENT. Interop. Windows8. стопсервицегрбит](./stopservicegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="91100-114">Type: [Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit](./stopservicegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="91100-115">Параметры для завершения или возобновления работы экземпляра.</span><span class="sxs-lookup"><span data-stu-id="91100-115">The options to stop or resume the instance.</span></span>

## <a name="see-also"></a><span data-ttu-id="91100-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91100-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="91100-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="91100-117">Reference</span></span>

[<span data-ttu-id="91100-118">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="91100-118">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="91100-119">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="91100-119">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="91100-120">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="91100-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
