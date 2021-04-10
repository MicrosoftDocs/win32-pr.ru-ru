---
description: Дополнительные сведения о методе API. Жетбегинсессион
title: API. Жетбегинсессион, метод
TOCTitle: 'JetBeginSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginSession(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID@,System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginsession(v=EXCHG.10)
ms:contentKeyID: 55107223
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39174c27043f62de4c1a78685876e79de513b804
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143360"
---
# <a name="apijetbeginsession-method"></a><span data-ttu-id="b4ac1-103">API. Жетбегинсессион, метод</span><span class="sxs-lookup"><span data-stu-id="b4ac1-103">Api.JetBeginSession method</span></span>

<span data-ttu-id="b4ac1-104">Инициализируйте новый сеанс ESENT.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-104">Initialize a new ESENT session.</span></span>

<span data-ttu-id="b4ac1-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4ac1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4ac1-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4ac1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ac1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4ac1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginSession ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef sesid As JET_SESID, _
    username As String, _
    password As String _
)
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim username As String
Dim password As StringApi.JetBeginSession(instance, sesid, _
    username, password)
```

``` csharp
public static void JetBeginSession(
    JET_INSTANCE instance,
    out JET_SESID sesid,
    string username,
    string password
)
```

#### <a name="parameters"></a><span data-ttu-id="b4ac1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4ac1-108">Parameters</span></span>

  - <span data-ttu-id="b4ac1-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="b4ac1-109">instance</span></span>  
    <span data-ttu-id="b4ac1-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b4ac1-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b4ac1-111">Инициализированный экземпляр, в котором создается сеанс.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-111">The initialized instance to create the session in.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4ac1-112">сесид</span><span class="sxs-lookup"><span data-stu-id="b4ac1-112">sesid</span></span>  
    <span data-ttu-id="b4ac1-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b4ac1-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b4ac1-114">Возвращает созданный сеанс.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-114">Returns the created session.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4ac1-115">username</span><span class="sxs-lookup"><span data-stu-id="b4ac1-115">username</span></span>  
    <span data-ttu-id="b4ac1-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b4ac1-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b4ac1-117">Параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-117">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4ac1-118">password</span><span class="sxs-lookup"><span data-stu-id="b4ac1-118">password</span></span>  
    <span data-ttu-id="b4ac1-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b4ac1-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b4ac1-120">Параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-120">The parameter is not used.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4ac1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4ac1-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4ac1-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="b4ac1-122">Reference</span></span>

[<span data-ttu-id="b4ac1-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="b4ac1-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b4ac1-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="b4ac1-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b4ac1-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b4ac1-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
