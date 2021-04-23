---
description: Дополнительные сведения о методе API. JetTerm2
title: API. JetTerm2, метод
TOCTitle: 'JetTerm2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm2(v=EXCHG.10)
ms:contentKeyID: 55100829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e8a4aa8c96f9a4d0242657fe7126abf1388a7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674347"
---
# <a name="apijetterm2-method"></a><span data-ttu-id="3fe53-103">API. JetTerm2, метод</span><span class="sxs-lookup"><span data-stu-id="3fe53-103">Api.JetTerm2 method</span></span>

<span data-ttu-id="3fe53-104">Завершите работу экземпляра, созданного с помощью [жетинит (JET_INSTANCE)](./api.jetinit-method.md) или [жеткреатеинстанце (JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="3fe53-104">Terminate an instance that was created with [JetInit(JET_INSTANCE)](./api.jetinit-method.md) or [JetCreateInstance(JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span></span>

<span data-ttu-id="3fe53-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3fe53-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3fe53-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3fe53-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3fe53-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fe53-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTerm2 ( _
    instance As JET_INSTANCE, _
    grbit As TermGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As TermGrbitApi.JetTerm2(instance, grbit)
```

``` csharp
public static void JetTerm2(
    JET_INSTANCE instance,
    TermGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3fe53-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fe53-108">Parameters</span></span>

  - <span data-ttu-id="3fe53-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="3fe53-109">instance</span></span>  
    <span data-ttu-id="3fe53-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3fe53-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="3fe53-111">Экземпляр для завершения.</span><span class="sxs-lookup"><span data-stu-id="3fe53-111">The instance to terminate.</span></span>

<!-- end list -->

  - <span data-ttu-id="3fe53-112">грбит</span><span class="sxs-lookup"><span data-stu-id="3fe53-112">grbit</span></span>  
    <span data-ttu-id="3fe53-113">Тип: [Microsoft. ISAM. ESENT. Interop. термгрбит](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3fe53-113">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3fe53-114">Параметры завершения.</span><span class="sxs-lookup"><span data-stu-id="3fe53-114">Termination options.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fe53-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fe53-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3fe53-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="3fe53-116">Reference</span></span>

[<span data-ttu-id="3fe53-117">Класс API</span><span class="sxs-lookup"><span data-stu-id="3fe53-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3fe53-118">Члены API</span><span class="sxs-lookup"><span data-stu-id="3fe53-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3fe53-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3fe53-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
