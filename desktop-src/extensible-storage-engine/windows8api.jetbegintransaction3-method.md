---
description: 'Дополнительные сведения о методе: Windows8Api. JetBeginTransaction3'
title: Windows8Api. JetBeginTransaction3, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetBeginTransaction3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3(Microsoft.Isam.Esent.Interop.JET_SESID,System.Int64,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetbegintransaction3(v=EXCHG.10)
ms:contentKeyID: 55107825
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7605cdb44c66d929e6663caaad9e40d3c98737b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543650"
---
# <a name="windows8apijetbegintransaction3-method"></a><span data-ttu-id="c9ec1-103">Windows8Api. JetBeginTransaction3, метод</span><span class="sxs-lookup"><span data-stu-id="c9ec1-103">Windows8Api.JetBeginTransaction3 method</span></span>

<span data-ttu-id="c9ec1-104">Заставляет сеанс войти в транзакцию или создать новую точку сохранения в существующей транзакции.</span><span class="sxs-lookup"><span data-stu-id="c9ec1-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="c9ec1-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9ec1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="c9ec1-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9ec1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ec1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9ec1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction3 ( _
    sesid As JET_SESID, _
    userTransactionId As Long, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim userTransactionId As Long
Dim grbit As BeginTransactionGrbitWindows8Api.JetBeginTransaction3(sesid, _
    userTransactionId, grbit)
```

``` csharp
public static void JetBeginTransaction3(
    JET_SESID sesid,
    long userTransactionId,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c9ec1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9ec1-108">Parameters</span></span>

  - <span data-ttu-id="c9ec1-109">сесид</span><span class="sxs-lookup"><span data-stu-id="c9ec1-109">sesid</span></span>  
    <span data-ttu-id="c9ec1-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9ec1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c9ec1-111">Сеанс, для которого начинается транзакция.</span><span class="sxs-lookup"><span data-stu-id="c9ec1-111">The session to begin the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9ec1-112">усертрансактионид</span><span class="sxs-lookup"><span data-stu-id="c9ec1-112">userTransactionId</span></span>  
    <span data-ttu-id="c9ec1-113">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="c9ec1-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="c9ec1-114">Необязательный идентификатор, предоставленный пользователем для идентификации транзакции.</span><span class="sxs-lookup"><span data-stu-id="c9ec1-114">An optional identifier supplied by the user for identifying the transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9ec1-115">грбит</span><span class="sxs-lookup"><span data-stu-id="c9ec1-115">grbit</span></span>  
    <span data-ttu-id="c9ec1-116">Тип: [Microsoft. ISAM. ESENT. Interop. бегинтрансактионгрбит](./begintransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c9ec1-116">Type: [Microsoft.Isam.Esent.Interop.BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c9ec1-117">Параметры транзакций.</span><span class="sxs-lookup"><span data-stu-id="c9ec1-117">Transaction options.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9ec1-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9ec1-118">Remarks</span></span>

<span data-ttu-id="c9ec1-119">Впервые появился в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c9ec1-119">Introduced in Windows 8.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9ec1-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9ec1-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9ec1-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="c9ec1-121">Reference</span></span>

[<span data-ttu-id="c9ec1-122">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c9ec1-122">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="c9ec1-123">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c9ec1-123">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="c9ec1-124">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="c9ec1-124">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
