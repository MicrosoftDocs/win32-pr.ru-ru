---
description: 'Дополнительные сведения о свойстве: JET_THREADSTATS. Кпажепререад'
title: Свойство JET_THREADSTATS. Кпажепререад (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cPagePreread property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPagePreread
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpagepreread(v=EXCHG.10)
ms:contentKeyID: 39510638
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPagePreread
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPagePreread
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPagePreread
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPagePreread
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd004407fcc7474435b8b2e12dc7eff9555b0e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266026"
---
# <a name="jet_threadstatscpagepreread-property"></a><span data-ttu-id="47fba-103">Свойство JET_THREADSTATS. Кпажепререад</span><span class="sxs-lookup"><span data-stu-id="47fba-103">JET_THREADSTATS.cPagePreread property</span></span>

<span data-ttu-id="47fba-104">Возвращает общее число страниц базы данных, выбранных с диска ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="47fba-104">Gets the total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="47fba-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="47fba-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="47fba-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="47fba-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="47fba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47fba-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPagePreread As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPagePreread
```

``` csharp
public int cPagePreread { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="47fba-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="47fba-108">Property value</span></span>

<span data-ttu-id="47fba-109">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="47fba-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="47fba-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47fba-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="47fba-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="47fba-111">Reference</span></span>

[<span data-ttu-id="47fba-112">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="47fba-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="47fba-113">Элементы JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="47fba-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="47fba-114">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="47fba-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
