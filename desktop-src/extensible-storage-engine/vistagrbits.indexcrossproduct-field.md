---
description: 'Дополнительные сведения о: Вистагрбитс. Индекскросспродукт поле'
title: Поле Вистагрбитс. Индекскросспродукт (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1b16f741c63d455d18a887331505080aef62990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999713"
---
# <a name="vistagrbitsindexcrossproduct-field"></a><span data-ttu-id="fb017-103">Вистагрбитс. Индекскросспродукт, поле</span><span class="sxs-lookup"><span data-stu-id="fb017-103">VistaGrbits.IndexCrossProduct field</span></span>

<span data-ttu-id="fb017-104">Если задать этот флаг для индекса, имеющего более одного ключевого столбца, который является многозначным, будет создана запись индекса для каждого результата перекрестного произведения всех значений в этих ключевых столбцах.</span><span class="sxs-lookup"><span data-stu-id="fb017-104">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="fb017-105">В противном случае индекс будет иметь только одну запись для каждого многозначного ключевого столбца, который является многозначным столбцом, и каждая из этих элементов индекса будет использовать первое Многозначное значение из любых других ключевых столбцов, которые являются многозначными столбцами.</span><span class="sxs-lookup"><span data-stu-id="fb017-105">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="fb017-106">Например, если вы указали этот флаг для индекса по столбцу A, который имеет значения "Red" и "Blue", а столбец B имеет значения "1" и "2", то будут созданы следующие элементы индекса: "Red", "1"; "Red", "2"; "Blue", "1"; "Blue", "2".</span><span class="sxs-lookup"><span data-stu-id="fb017-106">For example, if you specified this flag for an index over column A that has the values "red" and "blue" and over column B that has the values "1" and "2" then the following index entries would be created: "red", "1"; "red", "2"; "blue", "1"; "blue", "2".</span></span> <span data-ttu-id="fb017-107">В противном случае будут созданы следующие записи индекса: "Red", "1"; "Blue", "1".</span><span class="sxs-lookup"><span data-stu-id="fb017-107">Otherwise, the following index entries would be created: "red", "1"; "blue", "1".</span></span>

<span data-ttu-id="fb017-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fb017-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="fb017-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fb017-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fb017-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb017-110">Syntax</span></span>

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a><span data-ttu-id="fb017-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb017-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fb017-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="fb017-112">Reference</span></span>

[<span data-ttu-id="fb017-113">Класс Вистагрбитс</span><span class="sxs-lookup"><span data-stu-id="fb017-113">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="fb017-114">Элементы Вистагрбитс</span><span class="sxs-lookup"><span data-stu-id="fb017-114">VistaGrbits members</span></span>](./vistagrbits-members.md)

[<span data-ttu-id="fb017-115">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="fb017-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
