---
description: 'Дополнительные сведения о методе: Instance.Init (JET_RSTINFO, Инитгрбит)'
title: Метод Instance.Init (JET_RSTINFO, Инитгрбит)
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1945b0119053a2759b57b8781b86cf682b3a364c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701727"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a><span data-ttu-id="9fcdf-103">Метод Instance.Init (JET_RSTINFO, Инитгрбит)</span><span class="sxs-lookup"><span data-stu-id="9fcdf-103">Instance.Init method (JET_RSTINFO, InitGrbit)</span></span>

<span data-ttu-id="9fcdf-104">Инициализируйте JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="9fcdf-104">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="9fcdf-105">Для этого API требуется по крайней мере версия ESENT для Vista.</span><span class="sxs-lookup"><span data-stu-id="9fcdf-105">This API requires at least the Vista version of ESENT.</span></span>

<span data-ttu-id="9fcdf-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9fcdf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9fcdf-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9fcdf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9fcdf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fcdf-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9fcdf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fcdf-109">Parameters</span></span>

  - <span data-ttu-id="9fcdf-110">рековерйоптионс</span><span class="sxs-lookup"><span data-stu-id="9fcdf-110">recoveryOptions</span></span>  
    <span data-ttu-id="9fcdf-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="9fcdf-111">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="9fcdf-112">Дополнительные параметры восстановления для повторного сопоставления баз данных во время восстановления, расположение для отмены восстановления или состояние восстановления.</span><span class="sxs-lookup"><span data-stu-id="9fcdf-112">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="9fcdf-113">грбит</span><span class="sxs-lookup"><span data-stu-id="9fcdf-113">grbit</span></span>  
    <span data-ttu-id="9fcdf-114">Тип: [Microsoft.Isam.Esent.Interop.Iniтгрбит](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9fcdf-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9fcdf-115">Параметры инициализации.</span><span class="sxs-lookup"><span data-stu-id="9fcdf-115">Initialization options.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fcdf-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fcdf-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9fcdf-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="9fcdf-117">Reference</span></span>

[<span data-ttu-id="9fcdf-118">Класс экземпляра</span><span class="sxs-lookup"><span data-stu-id="9fcdf-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="9fcdf-119">Члены экземпляра</span><span class="sxs-lookup"><span data-stu-id="9fcdf-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="9fcdf-120">Перегрузка init</span><span class="sxs-lookup"><span data-stu-id="9fcdf-120">Init overload</span></span>](./instance.init-method2.md)

[<span data-ttu-id="9fcdf-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9fcdf-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
