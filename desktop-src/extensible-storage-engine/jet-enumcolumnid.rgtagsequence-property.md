---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMNID. Ргтагсекуенце'
title: Свойство JET_ENUMCOLUMNID. Ргтагсекуенце
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d61d69fb9f22a31f07ee2eb0b4116a13761d961
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808543"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a><span data-ttu-id="738c7-103">Свойство JET_ENUMCOLUMNID. Ргтагсекуенце</span><span class="sxs-lookup"><span data-stu-id="738c7-103">JET_ENUMCOLUMNID.rgtagSequence property</span></span>

<span data-ttu-id="738c7-104">Возвращает или задает массив индексов, отсчитываемый от единицы, в массиве значений столбцов для данного столбца.</span><span class="sxs-lookup"><span data-stu-id="738c7-104">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="738c7-105">Единственный элемент — это Итагсекуенце, который определен в JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="738c7-105">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="738c7-106">Итагсекуенце 0 (ноль) означает "Skip".</span><span class="sxs-lookup"><span data-stu-id="738c7-106">An itagSequence of 0 (zero) means "skip".</span></span> <span data-ttu-id="738c7-107">Итагсекуенце 1 означает возврат значения первого столбца столбца, 2 — второй и т. д.</span><span class="sxs-lookup"><span data-stu-id="738c7-107">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

<span data-ttu-id="738c7-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="738c7-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="738c7-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="738c7-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="738c7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="738c7-110">Syntax</span></span>

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="738c7-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="738c7-111">Property value</span></span>

<span data-ttu-id="738c7-112">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="738c7-112">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="738c7-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="738c7-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="738c7-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="738c7-114">Reference</span></span>

[<span data-ttu-id="738c7-115">Класс JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="738c7-115">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="738c7-116">Элементы JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="738c7-116">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="738c7-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="738c7-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
