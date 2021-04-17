---
description: Дополнительные сведения о методе API. Жетсетсессионконтекст
title: API. Жетсетсессионконтекст, метод
TOCTitle: 'JetSetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID,System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100820
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d73a382a2b8e176e2d1ce6fa13585a6b5fa103e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693496"
---
# <a name="apijetsetsessioncontext-method"></a><span data-ttu-id="28df1-103">API. Жетсетсессионконтекст, метод</span><span class="sxs-lookup"><span data-stu-id="28df1-103">Api.JetSetSessionContext method</span></span>

<span data-ttu-id="28df1-104">Связывает сеанс с текущим потоком, используя заданный маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="28df1-104">Associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="28df1-105">Эта ассоциация переопределяет требование к подсистеме по умолчанию, что транзакция для данного сеанса должна полностью выполняться в том же потоке.</span><span class="sxs-lookup"><span data-stu-id="28df1-105">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span> <span data-ttu-id="28df1-106">Чтобы удалить связь, используйте [жетресетсессионконтекст (JET_SESID)](./api.jetresetsessioncontext-method.md) .</span><span class="sxs-lookup"><span data-stu-id="28df1-106">Use [JetResetSessionContext(JET_SESID)](./api.jetresetsessioncontext-method.md) to remove the association.</span></span>

<span data-ttu-id="28df1-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="28df1-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="28df1-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="28df1-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="28df1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28df1-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionContext ( _
    sesid As JET_SESID, _
    context As IntPtr _
)
'Usage
Dim sesid As JET_SESID
Dim context As IntPtrApi.JetSetSessionContext(sesid, _
    context)
```

``` csharp
public static void JetSetSessionContext(
    JET_SESID sesid,
    IntPtr context
)
```

#### <a name="parameters"></a><span data-ttu-id="28df1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="28df1-110">Parameters</span></span>

  - <span data-ttu-id="28df1-111">сесид</span><span class="sxs-lookup"><span data-stu-id="28df1-111">sesid</span></span>  
    <span data-ttu-id="28df1-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="28df1-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="28df1-113">Сеанс, для которого задается контекст.</span><span class="sxs-lookup"><span data-stu-id="28df1-113">The session to set the context on.</span></span>

<!-- end list -->

  - <span data-ttu-id="28df1-114">контекст</span><span class="sxs-lookup"><span data-stu-id="28df1-114">context</span></span>  
    <span data-ttu-id="28df1-115">Тип: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="28df1-115">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="28df1-116">Заданный контекст.</span><span class="sxs-lookup"><span data-stu-id="28df1-116">The context to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="28df1-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28df1-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="28df1-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="28df1-118">Reference</span></span>

[<span data-ttu-id="28df1-119">Класс API</span><span class="sxs-lookup"><span data-stu-id="28df1-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="28df1-120">Члены API</span><span class="sxs-lookup"><span data-stu-id="28df1-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="28df1-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="28df1-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
