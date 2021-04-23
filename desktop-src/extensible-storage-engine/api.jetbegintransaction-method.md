---
description: Дополнительные сведения о методе API. Жетбегинтрансактион
title: API. Жетбегинтрансактион, метод
TOCTitle: 'JetBeginTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction(v=EXCHG.10)
ms:contentKeyID: 55107225
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b8812df332734ee109ea52820346e433e747751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710963"
---
# <a name="apijetbegintransaction-method"></a><span data-ttu-id="771e5-103">API. Жетбегинтрансактион, метод</span><span class="sxs-lookup"><span data-stu-id="771e5-103">Api.JetBeginTransaction method</span></span>

<span data-ttu-id="771e5-104">Заставляет сеанс войти в транзакцию или создать новую точку сохранения в существующей транзакции.</span><span class="sxs-lookup"><span data-stu-id="771e5-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="771e5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="771e5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="771e5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="771e5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="771e5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="771e5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetBeginTransaction(sesid)
```

``` csharp
public static void JetBeginTransaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="771e5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="771e5-108">Parameters</span></span>

  - <span data-ttu-id="771e5-109">сесид</span><span class="sxs-lookup"><span data-stu-id="771e5-109">sesid</span></span>  
    <span data-ttu-id="771e5-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="771e5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="771e5-111">Сеанс, для которого начинается транзакция.</span><span class="sxs-lookup"><span data-stu-id="771e5-111">The session to begin the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="771e5-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="771e5-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="771e5-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="771e5-113">Reference</span></span>

[<span data-ttu-id="771e5-114">Класс API</span><span class="sxs-lookup"><span data-stu-id="771e5-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="771e5-115">Члены API</span><span class="sxs-lookup"><span data-stu-id="771e5-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="771e5-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="771e5-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
