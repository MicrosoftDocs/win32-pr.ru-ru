---
description: Дополнительные сведения о методе API. Жеткреатеинстанце
title: API. Жеткреатеинстанце, метод
TOCTitle: 'JetCreateInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance(v=EXCHG.10)
ms:contentKeyID: 55100672
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e865c443d4f19b14a955204840355ee73be8773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710959"
---
# <a name="apijetcreateinstance-method"></a><span data-ttu-id="22eb2-103">API. Жеткреатеинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="22eb2-103">Api.JetCreateInstance method</span></span>

<span data-ttu-id="22eb2-104">Выделяет новый экземпляр ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="22eb2-104">Allocates a new instance of the database engine.</span></span>

<span data-ttu-id="22eb2-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="22eb2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="22eb2-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="22eb2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="22eb2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22eb2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As StringApi.JetCreateInstance(instance, _
    name)
```

``` csharp
public static void JetCreateInstance(
    out JET_INSTANCE instance,
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="22eb2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="22eb2-108">Parameters</span></span>

  - <span data-ttu-id="22eb2-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="22eb2-109">instance</span></span>  
    <span data-ttu-id="22eb2-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="22eb2-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="22eb2-111">Возвращает новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="22eb2-111">Returns the new instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="22eb2-112">name</span><span class="sxs-lookup"><span data-stu-id="22eb2-112">name</span></span>  
    <span data-ttu-id="22eb2-113">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="22eb2-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="22eb2-114">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="22eb2-114">The name of the instance.</span></span> <span data-ttu-id="22eb2-115">Имена должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="22eb2-115">Names must be unique.</span></span>

## <a name="see-also"></a><span data-ttu-id="22eb2-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22eb2-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22eb2-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="22eb2-117">Reference</span></span>

[<span data-ttu-id="22eb2-118">Класс API</span><span class="sxs-lookup"><span data-stu-id="22eb2-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="22eb2-119">Члены API</span><span class="sxs-lookup"><span data-stu-id="22eb2-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="22eb2-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="22eb2-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
