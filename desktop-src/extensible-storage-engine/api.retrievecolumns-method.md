---
description: Дополнительные сведения о методе API. Ретриевеколумнс
title: API. Ретриевеколумнс, метод
TOCTitle: 'RetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100867
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c981ad8b8e90db10bb8735aa349315b769e6641f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539689"
---
# <a name="apiretrievecolumns-method"></a><span data-ttu-id="bc8dc-103">API. Ретриевеколумнс, метод</span><span class="sxs-lookup"><span data-stu-id="bc8dc-103">Api.RetrieveColumns method</span></span>

<span data-ttu-id="bc8dc-104">Извлекает столбцы в объекты Колумнвалуе.</span><span class="sxs-lookup"><span data-stu-id="bc8dc-104">Retrieves columns into ColumnValue objects.</span></span>

<span data-ttu-id="bc8dc-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bc8dc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bc8dc-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bc8dc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8dc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc8dc-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub RetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.RetrieveColumns(sesid, tableid, _
    values)
```

``` csharp
public static void RetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="bc8dc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc8dc-108">Parameters</span></span>

  - <span data-ttu-id="bc8dc-109">сесид</span><span class="sxs-lookup"><span data-stu-id="bc8dc-109">sesid</span></span>  
    <span data-ttu-id="bc8dc-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bc8dc-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bc8dc-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="bc8dc-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc8dc-112">TableID</span><span class="sxs-lookup"><span data-stu-id="bc8dc-112">tableid</span></span>  
    <span data-ttu-id="bc8dc-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bc8dc-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bc8dc-114">Курсор получает данные из.</span><span class="sxs-lookup"><span data-stu-id="bc8dc-114">The cursor retrieve the data from.</span></span> <span data-ttu-id="bc8dc-115">Курсор должен быть размещен в записи.</span><span class="sxs-lookup"><span data-stu-id="bc8dc-115">The cursor should be positioned on a record.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc8dc-116">значения</span><span class="sxs-lookup"><span data-stu-id="bc8dc-116">values</span></span>  
    <span data-ttu-id="bc8dc-117">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="bc8dc-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="bc8dc-118">Извлекаемые значения.</span><span class="sxs-lookup"><span data-stu-id="bc8dc-118">The values to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc8dc-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc8dc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bc8dc-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="bc8dc-120">Reference</span></span>

[<span data-ttu-id="bc8dc-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="bc8dc-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bc8dc-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="bc8dc-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bc8dc-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bc8dc-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
