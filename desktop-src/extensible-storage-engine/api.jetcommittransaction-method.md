---
description: Дополнительные сведения о методе API. Жеткоммиттрансактион
title: API. Жеткоммиттрансактион, метод
TOCTitle: 'JetCommitTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcommittransaction(v=EXCHG.10)
ms:contentKeyID: 55100665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edf0799af53c3da422f92f981f7a28ee7a283d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710852"
---
# <a name="apijetcommittransaction-method"></a><span data-ttu-id="391e5-103">API. Жеткоммиттрансактион, метод</span><span class="sxs-lookup"><span data-stu-id="391e5-103">Api.JetCommitTransaction method</span></span>

<span data-ttu-id="391e5-104">Фиксирует изменения, внесенные в состояние базы данных во время текущей точки сохранения, и переносит их в предыдущую точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="391e5-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="391e5-105">При фиксации самой внешней точки сохранения изменения, внесенные во время этой точки сохранения, будут зафиксированы в состоянии базы данных, и сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="391e5-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="391e5-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="391e5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="391e5-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="391e5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="391e5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="391e5-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbitApi.JetCommitTransaction(sesid, _
    grbit)
```

``` csharp
public static void JetCommitTransaction(
    JET_SESID sesid,
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="391e5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="391e5-109">Parameters</span></span>

  - <span data-ttu-id="391e5-110">сесид</span><span class="sxs-lookup"><span data-stu-id="391e5-110">sesid</span></span>  
    <span data-ttu-id="391e5-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="391e5-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="391e5-112">Сеанс, для которого зафиксирована транзакция.</span><span class="sxs-lookup"><span data-stu-id="391e5-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="391e5-113">грбит</span><span class="sxs-lookup"><span data-stu-id="391e5-113">grbit</span></span>  
    <span data-ttu-id="391e5-114">Тип: [Microsoft. ISAM. ESENT. Interop. коммиттрансактионгрбит](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="391e5-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="391e5-115">Параметры фиксации.</span><span class="sxs-lookup"><span data-stu-id="391e5-115">Commit options.</span></span>

## <a name="see-also"></a><span data-ttu-id="391e5-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="391e5-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="391e5-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="391e5-117">Reference</span></span>

[<span data-ttu-id="391e5-118">Класс API</span><span class="sxs-lookup"><span data-stu-id="391e5-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="391e5-119">Члены API</span><span class="sxs-lookup"><span data-stu-id="391e5-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="391e5-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="391e5-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
