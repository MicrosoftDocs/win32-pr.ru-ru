---
description: Дополнительные сведения о методе API. Жеттерм
title: API. Жеттерм, метод
TOCTitle: 'JetTerm method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm(v=EXCHG.10)
ms:contentKeyID: 55100813
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c8e028ecdc6456521b7aaa671cb4f5199e8751e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272728"
---
# <a name="apijetterm-method"></a><span data-ttu-id="68e76-103">API. Жеттерм, метод</span><span class="sxs-lookup"><span data-stu-id="68e76-103">Api.JetTerm method</span></span>

<span data-ttu-id="68e76-104">Завершите работу экземпляра, созданного с помощью [жетинит (JET_INSTANCE)](./api.jetinit-method.md) или [жеткреатеинстанце (JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="68e76-104">Terminate an instance that was created with [JetInit(JET_INSTANCE)](./api.jetinit-method.md) or [JetCreateInstance(JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span></span>

<span data-ttu-id="68e76-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68e76-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="68e76-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="68e76-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68e76-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68e76-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTerm ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTerm(instance)
```

``` csharp
public static void JetTerm(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="68e76-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68e76-108">Parameters</span></span>

  - <span data-ttu-id="68e76-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="68e76-109">instance</span></span>  
    <span data-ttu-id="68e76-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68e76-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="68e76-111">Экземпляр для завершения.</span><span class="sxs-lookup"><span data-stu-id="68e76-111">The instance to terminate.</span></span>

## <a name="see-also"></a><span data-ttu-id="68e76-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68e76-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68e76-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="68e76-113">Reference</span></span>

[<span data-ttu-id="68e76-114">Класс API</span><span class="sxs-lookup"><span data-stu-id="68e76-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="68e76-115">Члены API</span><span class="sxs-lookup"><span data-stu-id="68e76-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="68e76-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="68e76-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
