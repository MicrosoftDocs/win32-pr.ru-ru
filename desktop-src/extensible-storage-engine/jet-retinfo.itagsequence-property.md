---
description: 'Дополнительные сведения о свойстве: JET_RETINFO. Итагсекуенце'
title: Свойство JET_RETINFO. Итагсекуенце
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103876
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_itagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df42b6a52b34ec265aceb5b069b06f39c0663b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272400"
---
# <a name="jet_retinfoitagsequence-property"></a><span data-ttu-id="37f07-103">Свойство JET_RETINFO. Итагсекуенце</span><span class="sxs-lookup"><span data-stu-id="37f07-103">JET_RETINFO.itagSequence property</span></span>

<span data-ttu-id="37f07-104">Возвращает или задает порядковый номер значения в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="37f07-104">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="37f07-105">Массив значений является исходным.</span><span class="sxs-lookup"><span data-stu-id="37f07-105">The array of values is one-based.</span></span> <span data-ttu-id="37f07-106">Первое значение — Sequence 1, а не 0.</span><span class="sxs-lookup"><span data-stu-id="37f07-106">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="37f07-107">Если столбец записи имеет только одно значение, то в качестве Итагсекуенце передается 1.</span><span class="sxs-lookup"><span data-stu-id="37f07-107">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<span data-ttu-id="37f07-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="37f07-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="37f07-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="37f07-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="37f07-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37f07-110">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="37f07-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="37f07-111">Property value</span></span>

<span data-ttu-id="37f07-112">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="37f07-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="37f07-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37f07-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="37f07-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="37f07-114">Reference</span></span>

[<span data-ttu-id="37f07-115">Класс JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="37f07-115">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="37f07-116">Элементы JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="37f07-116">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="37f07-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="37f07-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
