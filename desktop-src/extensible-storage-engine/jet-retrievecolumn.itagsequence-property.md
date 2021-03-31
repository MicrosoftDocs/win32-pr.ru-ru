---
description: 'Дополнительные сведения о свойстве: JET_RETRIEVECOLUMN. Итагсекуенце'
title: Свойство JET_RETRIEVECOLUMN. Итагсекуенце
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103882
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f2885d5bf467d282ef97172323a8de44980ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911755"
---
# <a name="jet_retrievecolumnitagsequence-property"></a><span data-ttu-id="69048-103">Свойство JET_RETRIEVECOLUMN. Итагсекуенце</span><span class="sxs-lookup"><span data-stu-id="69048-103">JET_RETRIEVECOLUMN.itagSequence property</span></span>

<span data-ttu-id="69048-104">Возвращает или задает порядковый номер значений, содержащихся в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="69048-104">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="69048-105">Если значение Итагсекуенце равно 0, то вместо данных столбца возвращается число экземпляров многозначного столбца.</span><span class="sxs-lookup"><span data-stu-id="69048-105">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span>

<span data-ttu-id="69048-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69048-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69048-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69048-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69048-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69048-108">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="69048-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="69048-109">Property value</span></span>

<span data-ttu-id="69048-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="69048-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="69048-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69048-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69048-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="69048-112">Reference</span></span>

[<span data-ttu-id="69048-113">Класс JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="69048-113">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="69048-114">Элементы JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="69048-114">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="69048-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="69048-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
