---
description: 'Дополнительные сведения о методе: Windows8Api. JetCommitTransaction2'
title: Windows8Api. JetCommitTransaction2, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetCommitTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcommittransaction2(v=EXCHG.10)
ms:contentKeyID: 55104454
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80ddc0670b60a3f2a280ff2aca3f051242c453ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701772"
---
# <a name="windows8apijetcommittransaction2-method"></a><span data-ttu-id="9947d-103">Windows8Api. JetCommitTransaction2, метод</span><span class="sxs-lookup"><span data-stu-id="9947d-103">Windows8Api.JetCommitTransaction2 method</span></span>

<span data-ttu-id="9947d-104">Фиксирует изменения, внесенные в состояние базы данных во время текущей точки сохранения, и переносит их в предыдущую точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="9947d-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="9947d-105">При фиксации самой внешней точки сохранения изменения, внесенные во время этой точки сохранения, будут зафиксированы в состоянии базы данных, и сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="9947d-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="9947d-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9947d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="9947d-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9947d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9947d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9947d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction2 ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_IDWindows8Api.JetCommitTransaction2(sesid, _
    grbit, durableCommit, commitId)
```

``` csharp
public static void JetCommitTransaction2(
    JET_SESID sesid,
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a><span data-ttu-id="9947d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9947d-109">Parameters</span></span>

  - <span data-ttu-id="9947d-110">сесид</span><span class="sxs-lookup"><span data-stu-id="9947d-110">sesid</span></span>  
    <span data-ttu-id="9947d-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9947d-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9947d-112">Сеанс, для которого зафиксирована транзакция.</span><span class="sxs-lookup"><span data-stu-id="9947d-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="9947d-113">грбит</span><span class="sxs-lookup"><span data-stu-id="9947d-113">grbit</span></span>  
    <span data-ttu-id="9947d-114">Тип: [Microsoft. ISAM. ESENT. Interop. коммиттрансактионгрбит](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9947d-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9947d-115">Параметры фиксации.</span><span class="sxs-lookup"><span data-stu-id="9947d-115">Commit options.</span></span>

<!-- end list -->

  - <span data-ttu-id="9947d-116">дураблекоммит</span><span class="sxs-lookup"><span data-stu-id="9947d-116">durableCommit</span></span>  
    <span data-ttu-id="9947d-117">Тип: [System. TimeSpan](/dotnet/api/system.timespan)</span><span class="sxs-lookup"><span data-stu-id="9947d-117">Type: [System.TimeSpan](/dotnet/api/system.timespan)</span></span>  
    
    <span data-ttu-id="9947d-118">Длительность фиксации отложенной транзакции.</span><span class="sxs-lookup"><span data-stu-id="9947d-118">Duration to commit lazy transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="9947d-119">коммитид</span><span class="sxs-lookup"><span data-stu-id="9947d-119">commitId</span></span>  
    <span data-ttu-id="9947d-120">Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="9947d-120">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="9947d-121">Идентификатор фиксации, связанный с этой записью фиксации.</span><span class="sxs-lookup"><span data-stu-id="9947d-121">Commit-id associated with this commit record.</span></span>

## <a name="see-also"></a><span data-ttu-id="9947d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9947d-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9947d-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="9947d-123">Reference</span></span>

[<span data-ttu-id="9947d-124">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="9947d-124">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="9947d-125">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="9947d-125">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="9947d-126">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="9947d-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
