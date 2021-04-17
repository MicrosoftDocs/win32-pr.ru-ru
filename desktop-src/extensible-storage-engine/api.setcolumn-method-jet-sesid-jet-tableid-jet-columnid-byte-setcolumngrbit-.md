---
description: 'Дополнительные сведения: метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Сетколумнгрбит)'
title: Метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Сетколумнгрбит)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , SetColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],Microsoft.Isam.Esent.Interop.SetColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100881
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e345db028422733d37d50f51cfd0c940823f9f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693540"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--setcolumngrbit"></a><span data-ttu-id="810c0-103">Метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Сетколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="810c0-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , SetColumnGrbit)</span></span>

<span data-ttu-id="810c0-104">Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</span><span class="sxs-lookup"><span data-stu-id="810c0-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="810c0-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="810c0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="810c0-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="810c0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="810c0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="810c0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    grbit As SetColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim grbit As SetColumnGrbitApi.SetColumn(sesid, tableid, columnid, _
    data, grbit)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    SetColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="810c0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="810c0-108">Parameters</span></span>

  - <span data-ttu-id="810c0-109">сесид</span><span class="sxs-lookup"><span data-stu-id="810c0-109">sesid</span></span>  
    <span data-ttu-id="810c0-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="810c0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="810c0-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="810c0-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="810c0-112">TableID</span><span class="sxs-lookup"><span data-stu-id="810c0-112">tableid</span></span>  
    <span data-ttu-id="810c0-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="810c0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="810c0-114">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="810c0-114">The cursor to update.</span></span> <span data-ttu-id="810c0-115">Необходимо подготовить обновление.</span><span class="sxs-lookup"><span data-stu-id="810c0-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="810c0-116">columnid</span><span class="sxs-lookup"><span data-stu-id="810c0-116">columnid</span></span>  
    <span data-ttu-id="810c0-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="810c0-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="810c0-118">Устанавливаемое значение columnid.</span><span class="sxs-lookup"><span data-stu-id="810c0-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="810c0-119">.</span><span class="sxs-lookup"><span data-stu-id="810c0-119">data</span></span>  
    <span data-ttu-id="810c0-120">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="810c0-120">Type: \[\]</span></span>  
    
    <span data-ttu-id="810c0-121">Задаваемые данные.</span><span class="sxs-lookup"><span data-stu-id="810c0-121">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="810c0-122">грбит</span><span class="sxs-lookup"><span data-stu-id="810c0-122">grbit</span></span>  
    <span data-ttu-id="810c0-123">Тип: [Microsoft. ISAM. ESENT. Interop. сетколумнгрбит](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="810c0-123">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="810c0-124">Параметры Сетколумн.</span><span class="sxs-lookup"><span data-stu-id="810c0-124">SetColumn options.</span></span>

## <a name="see-also"></a><span data-ttu-id="810c0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="810c0-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="810c0-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="810c0-126">Reference</span></span>

[<span data-ttu-id="810c0-127">Класс API</span><span class="sxs-lookup"><span data-stu-id="810c0-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="810c0-128">Члены API</span><span class="sxs-lookup"><span data-stu-id="810c0-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="810c0-129">Перегрузка Сетколумн</span><span class="sxs-lookup"><span data-stu-id="810c0-129">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="810c0-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="810c0-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
