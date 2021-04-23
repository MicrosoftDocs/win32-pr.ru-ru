---
description: 'Дополнительные сведения о методе: Вистаапи. Жетжетсреадстатс'
title: Вистаапи. Жетжетсреадстатс, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetThreadStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetthreadstats(v=EXCHG.10)
ms:contentKeyID: 55104192
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92572fd538f0c6c2643e7b40a07ac168ae6980d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701903"
---
# <a name="vistaapijetgetthreadstats-method"></a><span data-ttu-id="6fefa-103">Вистаапи. Жетжетсреадстатс, метод</span><span class="sxs-lookup"><span data-stu-id="6fefa-103">VistaApi.JetGetThreadStats method</span></span>

<span data-ttu-id="6fefa-104">Получает сведения о производительности из ядра СУБД для текущего потока.</span><span class="sxs-lookup"><span data-stu-id="6fefa-104">Retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="6fefa-105">Для сбора статистики, отражающей активность ядра СУБД в этом потоке между этими вызовами, можно использовать несколько вызовов.</span><span class="sxs-lookup"><span data-stu-id="6fefa-105">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="6fefa-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6fefa-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="6fefa-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6fefa-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6fefa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fefa-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetThreadStats ( _
    <OutAttribute> ByRef threadstats As JET_THREADSTATS _
)
'Usage
Dim threadstats As JET_THREADSTATSVistaApi.JetGetThreadStats(threadstats)
```

``` csharp
public static void JetGetThreadStats(
    out JET_THREADSTATS threadstats
)
```

#### <a name="parameters"></a><span data-ttu-id="6fefa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fefa-109">Parameters</span></span>

  - <span data-ttu-id="6fefa-110">среадстатс</span><span class="sxs-lookup"><span data-stu-id="6fefa-110">threadstats</span></span>  
    <span data-ttu-id="6fefa-111">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="6fefa-111">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="6fefa-112">Возвращает статистические данные потока.</span><span class="sxs-lookup"><span data-stu-id="6fefa-112">Returns the thread statistics data.</span></span>

## <a name="see-also"></a><span data-ttu-id="6fefa-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fefa-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6fefa-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="6fefa-114">Reference</span></span>

[<span data-ttu-id="6fefa-115">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="6fefa-115">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="6fefa-116">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="6fefa-116">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="6fefa-117">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="6fefa-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
