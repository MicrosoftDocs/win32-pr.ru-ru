---
description: 'Дополнительные сведения о свойстве: JET_SETINFO. Итагсекуенце'
title: Свойство JET_SETINFO. Итагсекуенце
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c409903f90633f15daa8d289c72530db943f1c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144239"
---
# <a name="jet_setinfoitagsequence-property"></a><span data-ttu-id="6ae9a-103">Свойство JET_SETINFO. Итагсекуенце</span><span class="sxs-lookup"><span data-stu-id="6ae9a-103">JET_SETINFO.itagSequence property</span></span>

<span data-ttu-id="6ae9a-104">Возвращает или задает порядковый номер значения в столбце с несколькими значениями, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="6ae9a-104">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="6ae9a-105">Массив значений является исходным.</span><span class="sxs-lookup"><span data-stu-id="6ae9a-105">The array of values is one-based.</span></span> <span data-ttu-id="6ae9a-106">Первое значение — Sequence 1, а не 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="6ae9a-106">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="6ae9a-107">Если столбец записи имеет только одно значение, то значение 1 должно передаваться как Итагсекуенце при замене этого значения.</span><span class="sxs-lookup"><span data-stu-id="6ae9a-107">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="6ae9a-108">Значение 0 (ноль) означает, что новый экземпляр значения столбца добавляется в конец последовательности значений столбцов.</span><span class="sxs-lookup"><span data-stu-id="6ae9a-108">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="6ae9a-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6ae9a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6ae9a-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6ae9a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae9a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ae9a-111">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="6ae9a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6ae9a-112">Property value</span></span>

<span data-ttu-id="6ae9a-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6ae9a-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ae9a-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ae9a-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6ae9a-115">Справочник</span><span class="sxs-lookup"><span data-stu-id="6ae9a-115">Reference</span></span>

[<span data-ttu-id="6ae9a-116">Класс JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="6ae9a-116">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="6ae9a-117">Элементы JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="6ae9a-117">JET_SETINFO members</span></span>](./jet-setinfo-members.md)

[<span data-ttu-id="6ae9a-118">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6ae9a-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
