---
description: Дополнительные сведения о методе API. Жетинит
title: API. Жетинит, метод
TOCTitle: 'JetInit method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit(Microsoft.Isam.Esent.Interop.JET_INSTANCE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit(v=EXCHG.10)
ms:contentKeyID: 55100760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27b0ad5fa640b853b46cd39ae595a1f486812adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913356"
---
# <a name="apijetinit-method"></a><span data-ttu-id="83ab7-103">API. Жетинит, метод</span><span class="sxs-lookup"><span data-stu-id="83ab7-103">Api.JetInit method</span></span>

<span data-ttu-id="83ab7-104">Инициализируйте ядро СУБД ESENT.</span><span class="sxs-lookup"><span data-stu-id="83ab7-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="83ab7-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="83ab7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="83ab7-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="83ab7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="83ab7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83ab7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetInit ( _
    ByRef instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetInit(instance)
```

``` csharp
public static void JetInit(
    ref JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="83ab7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83ab7-108">Parameters</span></span>

  - <span data-ttu-id="83ab7-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="83ab7-109">instance</span></span>  
    <span data-ttu-id="83ab7-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="83ab7-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="83ab7-111">Экземпляр для инициализации.</span><span class="sxs-lookup"><span data-stu-id="83ab7-111">The instance to initialize.</span></span> <span data-ttu-id="83ab7-112">Если экземпляр не был выделен, создается новый, а ядро работает в режиме с одним экземпляром.</span><span class="sxs-lookup"><span data-stu-id="83ab7-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="83ab7-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83ab7-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="83ab7-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="83ab7-114">Reference</span></span>

[<span data-ttu-id="83ab7-115">Класс API</span><span class="sxs-lookup"><span data-stu-id="83ab7-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="83ab7-116">Члены API</span><span class="sxs-lookup"><span data-stu-id="83ab7-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="83ab7-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="83ab7-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
