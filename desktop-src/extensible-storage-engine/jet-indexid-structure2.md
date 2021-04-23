---
description: 'Дополнительные сведения: структура JET_INDEXID'
title: Структура JET_INDEXID
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712881"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="135b3-103">Структура JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="135b3-103">JET_INDEXID structure</span></span>

<span data-ttu-id="135b3-104">Содержит идентификатор индекса.</span><span class="sxs-lookup"><span data-stu-id="135b3-104">Holds an index ID.</span></span> <span data-ttu-id="135b3-105">Идентификатор индекса — это указание, которое используется для ускорения выбора текущего индекса с помощью Жетсеткуррентиндекс.</span><span class="sxs-lookup"><span data-stu-id="135b3-105">An index ID is a hint that is used to accelerate the selection of the current index using JetSetCurrentIndex.</span></span> <span data-ttu-id="135b3-106">Это наиболее полезно при наличии очень большого количества индексов в таблице.</span><span class="sxs-lookup"><span data-stu-id="135b3-106">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="135b3-107">Идентификатор индекса можно получить с помощью Жетжетиндексинфо или Жетжеттаблеиндексинфо.</span><span class="sxs-lookup"><span data-stu-id="135b3-107">The index ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo.</span></span>

<span data-ttu-id="135b3-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="135b3-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="135b3-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="135b3-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="135b3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="135b3-110">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a><span data-ttu-id="135b3-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="135b3-111">Remarks</span></span>

<span data-ttu-id="135b3-112">Атрибут Pack необходим, так как версия C++ определена как массив байтов.</span><span class="sxs-lookup"><span data-stu-id="135b3-112">The Pack attribute is necessary because the C++ version is defined as a byte array.</span></span> <span data-ttu-id="135b3-113">Если компилятор C \# вставляет обычное заполнение между uint кбструкт и IntPtr, структура заканчивается слишком большим.</span><span class="sxs-lookup"><span data-stu-id="135b3-113">If the C\# compiler inserts the usual padding between the uint cbStruct and the IntPtr, then the structure ends up too large.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="135b3-114">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="135b3-114">Thread safety</span></span>

<span data-ttu-id="135b3-115">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="135b3-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="135b3-116">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="135b3-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="135b3-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="135b3-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="135b3-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="135b3-118">Reference</span></span>

[<span data-ttu-id="135b3-119">Элементы JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="135b3-119">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="135b3-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="135b3-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
