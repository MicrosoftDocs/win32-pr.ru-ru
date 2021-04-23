---
description: Дополнительные сведения о методе API. Жетроллбакк
title: API. Жетроллбакк, метод
TOCTitle: 'JetRollback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRollback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrollback(v=EXCHG.10)
ms:contentKeyID: 55100794
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9144bade272ddaea7501be5622c7263268c0f1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343055"
---
# <a name="apijetrollback-method"></a><span data-ttu-id="3abe5-103">API. Жетроллбакк, метод</span><span class="sxs-lookup"><span data-stu-id="3abe5-103">Api.JetRollback method</span></span>

<span data-ttu-id="3abe5-104">Отменяет изменения, внесенные в состояние базы данных, и возвращает его в последнюю точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="3abe5-104">Undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="3abe5-105">Жетроллбакк также закроет курсоры, открытые во время точки сохранения.</span><span class="sxs-lookup"><span data-stu-id="3abe5-105">JetRollback will also close any cursors opened during the save point.</span></span> <span data-ttu-id="3abe5-106">Если внешняя точка сохранения отменена, сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="3abe5-106">If the outermost save point is undone, the session will exit the transaction.</span></span>

<span data-ttu-id="3abe5-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3abe5-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3abe5-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3abe5-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3abe5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3abe5-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRollback ( _
    sesid As JET_SESID, _
    grbit As RollbackTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As RollbackTransactionGrbitApi.JetRollback(sesid, grbit)
```

``` csharp
public static void JetRollback(
    JET_SESID sesid,
    RollbackTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3abe5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3abe5-110">Parameters</span></span>

  - <span data-ttu-id="3abe5-111">сесид</span><span class="sxs-lookup"><span data-stu-id="3abe5-111">sesid</span></span>  
    <span data-ttu-id="3abe5-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3abe5-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3abe5-113">Сеанс для отката транзакции.</span><span class="sxs-lookup"><span data-stu-id="3abe5-113">The session to rollback the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="3abe5-114">грбит</span><span class="sxs-lookup"><span data-stu-id="3abe5-114">grbit</span></span>  
    <span data-ttu-id="3abe5-115">Тип: [Microsoft. ISAM. ESENT. Interop. роллбакктрансактионгрбит](./rollbacktransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3abe5-115">Type: [Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3abe5-116">Параметры отката.</span><span class="sxs-lookup"><span data-stu-id="3abe5-116">Rollback options.</span></span>

## <a name="see-also"></a><span data-ttu-id="3abe5-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3abe5-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3abe5-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="3abe5-118">Reference</span></span>

[<span data-ttu-id="3abe5-119">Класс API</span><span class="sxs-lookup"><span data-stu-id="3abe5-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3abe5-120">Члены API</span><span class="sxs-lookup"><span data-stu-id="3abe5-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3abe5-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3abe5-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
