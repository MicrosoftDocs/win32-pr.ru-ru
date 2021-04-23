---
description: 'Дополнительные сведения: метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)'
title: Метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Single)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100877
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
ms.openlocfilehash: e57a42a46b9247133c1427f3ae270645f6133523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143336"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-single"></a><span data-ttu-id="138b5-103">Метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</span><span class="sxs-lookup"><span data-stu-id="138b5-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</span></span>

<span data-ttu-id="138b5-104">Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.</span><span class="sxs-lookup"><span data-stu-id="138b5-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="138b5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="138b5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="138b5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="138b5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="138b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="138b5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Single _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As SingleApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    float data
)
```

#### <a name="parameters"></a><span data-ttu-id="138b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="138b5-108">Parameters</span></span>

  - <span data-ttu-id="138b5-109">сесид</span><span class="sxs-lookup"><span data-stu-id="138b5-109">sesid</span></span>  
    <span data-ttu-id="138b5-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="138b5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="138b5-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="138b5-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="138b5-112">TableID</span><span class="sxs-lookup"><span data-stu-id="138b5-112">tableid</span></span>  
    <span data-ttu-id="138b5-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="138b5-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="138b5-114">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="138b5-114">The cursor to update.</span></span> <span data-ttu-id="138b5-115">Необходимо подготовить обновление.</span><span class="sxs-lookup"><span data-stu-id="138b5-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="138b5-116">columnid</span><span class="sxs-lookup"><span data-stu-id="138b5-116">columnid</span></span>  
    <span data-ttu-id="138b5-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="138b5-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="138b5-118">Устанавливаемое значение columnid.</span><span class="sxs-lookup"><span data-stu-id="138b5-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="138b5-119">.</span><span class="sxs-lookup"><span data-stu-id="138b5-119">data</span></span>  
    <span data-ttu-id="138b5-120">Тип: [System. Single](/dotnet/api/system.single)</span><span class="sxs-lookup"><span data-stu-id="138b5-120">Type: [System.Single](/dotnet/api/system.single)</span></span>  
    
    <span data-ttu-id="138b5-121">Задаваемые данные.</span><span class="sxs-lookup"><span data-stu-id="138b5-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="138b5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="138b5-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="138b5-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="138b5-123">Reference</span></span>

[<span data-ttu-id="138b5-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="138b5-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="138b5-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="138b5-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="138b5-126">Перегрузка Сетколумн</span><span class="sxs-lookup"><span data-stu-id="138b5-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="138b5-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="138b5-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
