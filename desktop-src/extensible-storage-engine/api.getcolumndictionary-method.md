---
description: Дополнительные сведения о методе API. Жетколумндиктионари
title: API. Жетколумндиктионари, метод
TOCTitle: 'GetColumnDictionary method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getcolumndictionary(v=EXCHG.10)
ms:contentKeyID: 55100653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab359c5b8b163ce67f576f35250dd521eb14472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710857"
---
# <a name="apigetcolumndictionary-method"></a><span data-ttu-id="95ab0-103">API. Жетколумндиктионари, метод</span><span class="sxs-lookup"><span data-stu-id="95ab0-103">Api.GetColumnDictionary method</span></span>

<span data-ttu-id="95ab0-104">Создает словарь, который сопоставляет имена столбцов с их идентификаторами столбцов.</span><span class="sxs-lookup"><span data-stu-id="95ab0-104">Creates a dictionary which maps column names to their column IDs.</span></span>

<span data-ttu-id="95ab0-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="95ab0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="95ab0-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="95ab0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="95ab0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95ab0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetColumnDictionary ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IDictionary(Of String, JET_COLUMNID)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IDictionary(Of String, JET_COLUMNID)

returnValue = Api.GetColumnDictionary(sesid, _
    tableid)
```

``` csharp
public static IDictionary<string, JET_COLUMNID> GetColumnDictionary(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="95ab0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95ab0-108">Parameters</span></span>

  - <span data-ttu-id="95ab0-109">сесид</span><span class="sxs-lookup"><span data-stu-id="95ab0-109">sesid</span></span>  
    <span data-ttu-id="95ab0-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95ab0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="95ab0-111">Сесид для использования.</span><span class="sxs-lookup"><span data-stu-id="95ab0-111">The sesid to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="95ab0-112">TableID</span><span class="sxs-lookup"><span data-stu-id="95ab0-112">tableid</span></span>  
    <span data-ttu-id="95ab0-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95ab0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="95ab0-114">Таблица, для которой необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="95ab0-114">The table to retrieve the information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="95ab0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95ab0-115">Return value</span></span>

<span data-ttu-id="95ab0-116">Тип: [System. Collections. Generic. IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span><span class="sxs-lookup"><span data-stu-id="95ab0-116">Type: [System.Collections.Generic.IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span></span>  
<span data-ttu-id="95ab0-117">Имена столбцов сопоставления в словаре с идентификаторами столбцов.</span><span class="sxs-lookup"><span data-stu-id="95ab0-117">A dictionary mapping column names to column IDs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="95ab0-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95ab0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="95ab0-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="95ab0-119">Reference</span></span>

[<span data-ttu-id="95ab0-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="95ab0-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="95ab0-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="95ab0-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="95ab0-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="95ab0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
