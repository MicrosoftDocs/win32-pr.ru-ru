---
description: Дополнительные сведения о методе Instance.Init (Инитгрбит)
title: Метод Instance.Init (Инитгрбит)
TOCTitle: Init method (InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103295
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f87247a77cb89e6e5e9e20048b04f8d9fae36ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265579"
---
# <a name="instanceinit-method-initgrbit"></a><span data-ttu-id="fb967-103">Метод Instance.Init (Инитгрбит)</span><span class="sxs-lookup"><span data-stu-id="fb967-103">Instance.Init method (InitGrbit)</span></span>

<span data-ttu-id="fb967-104">Инициализируйте JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="fb967-104">Initialize the JET_INSTANCE.</span></span>

<span data-ttu-id="fb967-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fb967-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fb967-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fb967-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fb967-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb967-107">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim grbit As InitGrbit

instance.Init(grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="fb967-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb967-108">Parameters</span></span>

  - <span data-ttu-id="fb967-109">грбит</span><span class="sxs-lookup"><span data-stu-id="fb967-109">grbit</span></span>  
    <span data-ttu-id="fb967-110">Тип: [Microsoft.Isam.Esent.Interop.Iniтгрбит](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fb967-110">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="fb967-111">Параметры инициализации.</span><span class="sxs-lookup"><span data-stu-id="fb967-111">Initialization options.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb967-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb967-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fb967-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="fb967-113">Reference</span></span>

[<span data-ttu-id="fb967-114">Класс экземпляра</span><span class="sxs-lookup"><span data-stu-id="fb967-114">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="fb967-115">Члены экземпляра</span><span class="sxs-lookup"><span data-stu-id="fb967-115">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="fb967-116">Перегрузка init</span><span class="sxs-lookup"><span data-stu-id="fb967-116">Init overload</span></span>](./instance.init-method2.md)

[<span data-ttu-id="fb967-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fb967-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
