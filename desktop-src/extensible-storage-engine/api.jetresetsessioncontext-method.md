---
description: Дополнительные сведения о методе API. Жетресетсессионконтекст
title: API. Жетресетсессионконтекст, метод
TOCTitle: 'JetResetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100785
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a34a6c2922c0041f0720b498855b15c4aed23f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693625"
---
# <a name="apijetresetsessioncontext-method"></a><span data-ttu-id="5a755-103">API. Жетресетсессионконтекст, метод</span><span class="sxs-lookup"><span data-stu-id="5a755-103">Api.JetResetSessionContext method</span></span>

<span data-ttu-id="5a755-104">Отменяет связь сеанса с текущим потоком.</span><span class="sxs-lookup"><span data-stu-id="5a755-104">Disassociates a session from the current thread.</span></span> <span data-ttu-id="5a755-105">Его следует использовать вместе с [жетсетсессионконтекст (JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md).</span><span class="sxs-lookup"><span data-stu-id="5a755-105">This should be used in conjunction with [JetSetSessionContext(JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md).</span></span>

<span data-ttu-id="5a755-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a755-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a755-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a755-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a755-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a755-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetSessionContext ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetResetSessionContext(sesid)
```

``` csharp
public static void JetResetSessionContext(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="5a755-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a755-109">Parameters</span></span>

  - <span data-ttu-id="5a755-110">сесид</span><span class="sxs-lookup"><span data-stu-id="5a755-110">sesid</span></span>  
    <span data-ttu-id="5a755-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5a755-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5a755-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="5a755-112">The session to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a755-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a755-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a755-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="5a755-114">Reference</span></span>

[<span data-ttu-id="5a755-115">Класс API</span><span class="sxs-lookup"><span data-stu-id="5a755-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5a755-116">Члены API</span><span class="sxs-lookup"><span data-stu-id="5a755-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5a755-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5a755-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
