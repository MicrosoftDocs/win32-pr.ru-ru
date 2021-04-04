---
description: Дополнительные сведения о методе API. Жетсетколумнс
title: API. Жетсетколумнс, метод
TOCTitle: 'JetSetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_SETCOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumns(v=EXCHG.10)
ms:contentKeyID: 55100800
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 59d1d16a21996937357d0358625772a4b6712019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809215"
---
# <a name="apijetsetcolumns-method"></a><span data-ttu-id="29c11-103">API. Жетсетколумнс, метод</span><span class="sxs-lookup"><span data-stu-id="29c11-103">Api.JetSetColumns method</span></span>

<span data-ttu-id="29c11-104">Позволяет приложению задавать несколько значений столбцов в одной операции.</span><span class="sxs-lookup"><span data-stu-id="29c11-104">Allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="29c11-105">Массив структур [JET_SETCOLUMN](./jet-setcolumn-class.md) используется для описания набора значений столбцов, которые необходимо задать, а также для описания входных буферов для каждого устанавливаемого значения столбца.</span><span class="sxs-lookup"><span data-stu-id="29c11-105">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

<span data-ttu-id="29c11-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="29c11-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="29c11-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="29c11-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="29c11-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29c11-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Shared Function JetSetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    setcolumns As JET_SETCOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim setcolumns As JET_SETCOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumns(sesid, _
    tableid, setcolumns, numColumns)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public static JET_wrn JetSetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_SETCOLUMN[] setcolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="29c11-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="29c11-109">Parameters</span></span>

  - <span data-ttu-id="29c11-110">сесид</span><span class="sxs-lookup"><span data-stu-id="29c11-110">sesid</span></span>  
    <span data-ttu-id="29c11-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="29c11-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="29c11-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="29c11-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="29c11-113">TableID</span><span class="sxs-lookup"><span data-stu-id="29c11-113">tableid</span></span>  
    <span data-ttu-id="29c11-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="29c11-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="29c11-115">Курсор, для которого задаются столбцы.</span><span class="sxs-lookup"><span data-stu-id="29c11-115">The cursor to set the columns on.</span></span>

<!-- end list -->

  - <span data-ttu-id="29c11-116">SetColumns</span><span class="sxs-lookup"><span data-stu-id="29c11-116">setcolumns</span></span>  
    <span data-ttu-id="29c11-117">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="29c11-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="29c11-118">Массив структур [JET_SETCOLUMN](./jet-setcolumn-class.md) , описывающих данные, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="29c11-118">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures describing the data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="29c11-119">нумколумнс</span><span class="sxs-lookup"><span data-stu-id="29c11-119">numColumns</span></span>  
    <span data-ttu-id="29c11-120">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="29c11-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="29c11-121">Число записей в параметре SetColumns.</span><span class="sxs-lookup"><span data-stu-id="29c11-121">Number of entries in the setcolumns parameter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="29c11-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29c11-122">Return value</span></span>

<span data-ttu-id="29c11-123">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="29c11-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="29c11-124">Предупреждение.</span><span class="sxs-lookup"><span data-stu-id="29c11-124">A warning.</span></span> <span data-ttu-id="29c11-125">Если последний набор столбцов содержит предупреждение, это предупреждение будет возвращаться из самого Жетсетколумнс.</span><span class="sxs-lookup"><span data-stu-id="29c11-125">If the last column set has a warning, then this warning will be returned from JetSetColumns itself.</span></span>  

## <a name="see-also"></a><span data-ttu-id="29c11-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29c11-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="29c11-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="29c11-127">Reference</span></span>

[<span data-ttu-id="29c11-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="29c11-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="29c11-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="29c11-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="29c11-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="29c11-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
