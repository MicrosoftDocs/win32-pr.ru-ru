---
description: 'Дополнительные сведения: метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)'
title: Метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100879
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc3950db60b4d7fb52309e246555802f1624d6a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693492"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-uint32"></a><span data-ttu-id="941f7-103">Метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</span><span class="sxs-lookup"><span data-stu-id="941f7-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</span></span>

<span data-ttu-id="941f7-104">Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</span><span class="sxs-lookup"><span data-stu-id="941f7-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="941f7-105">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="941f7-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="941f7-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="941f7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="941f7-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="941f7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="941f7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="941f7-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As UInteger _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As UIntegerApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    uint data
)
```

#### <a name="parameters"></a><span data-ttu-id="941f7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="941f7-109">Parameters</span></span>

  - <span data-ttu-id="941f7-110">сесид</span><span class="sxs-lookup"><span data-stu-id="941f7-110">sesid</span></span>  
    <span data-ttu-id="941f7-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="941f7-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="941f7-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="941f7-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="941f7-113">TableID</span><span class="sxs-lookup"><span data-stu-id="941f7-113">tableid</span></span>  
    <span data-ttu-id="941f7-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="941f7-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="941f7-115">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="941f7-115">The cursor to update.</span></span> <span data-ttu-id="941f7-116">Необходимо подготовить обновление.</span><span class="sxs-lookup"><span data-stu-id="941f7-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="941f7-117">columnid</span><span class="sxs-lookup"><span data-stu-id="941f7-117">columnid</span></span>  
    <span data-ttu-id="941f7-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="941f7-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="941f7-119">Устанавливаемое значение columnid.</span><span class="sxs-lookup"><span data-stu-id="941f7-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="941f7-120">.</span><span class="sxs-lookup"><span data-stu-id="941f7-120">data</span></span>  
    <span data-ttu-id="941f7-121">Тип: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="941f7-121">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="941f7-122">Задаваемые данные.</span><span class="sxs-lookup"><span data-stu-id="941f7-122">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="941f7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="941f7-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="941f7-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="941f7-124">Reference</span></span>

[<span data-ttu-id="941f7-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="941f7-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="941f7-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="941f7-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="941f7-127">Перегрузка Сетколумн</span><span class="sxs-lookup"><span data-stu-id="941f7-127">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="941f7-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="941f7-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
