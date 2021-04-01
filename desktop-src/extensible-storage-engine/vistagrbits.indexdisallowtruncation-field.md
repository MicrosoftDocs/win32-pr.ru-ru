---
description: 'Дополнительные сведения о: Вистагрбитс. Индексдисалловтрункатион поле'
title: Поле Вистагрбитс. Индексдисалловтрункатион (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: IndexDisallowTruncation field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexDisallowTruncation
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexdisallowtruncation(v=EXCHG.10)
ms:contentKeyID: 55104424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexDisallowTruncation
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexDisallowTruncation
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d359acea8de5b72bc7137feefbc1d1281c07ed57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081621"
---
# <a name="vistagrbitsindexdisallowtruncation-field"></a><span data-ttu-id="16a7e-103">Вистагрбитс. Индексдисалловтрункатион, поле</span><span class="sxs-lookup"><span data-stu-id="16a7e-103">VistaGrbits.IndexDisallowTruncation field</span></span>

<span data-ttu-id="16a7e-104">При указании этого флага любое обновление индекса приведет к сбою усечения ключа с [кэйтрункатед](./jet-err-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="16a7e-104">Specifying this flag will cause any update to the index that would result in a truncated key to fail with [KeyTruncated](./jet-err-enumeration.md).</span></span> <span data-ttu-id="16a7e-105">В противном случае ключи будут обрезаны без уведомления.</span><span class="sxs-lookup"><span data-stu-id="16a7e-105">Otherwise, keys will be silently truncated.</span></span>

<span data-ttu-id="16a7e-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="16a7e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="16a7e-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="16a7e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="16a7e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16a7e-108">Syntax</span></span>

``` vb
'Declaration
Public Const IndexDisallowTruncation As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexDisallowTruncation
```

``` csharp
public const CreateIndexGrbit IndexDisallowTruncation
```

## <a name="see-also"></a><span data-ttu-id="16a7e-109">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16a7e-109">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="16a7e-110">Справочник</span><span class="sxs-lookup"><span data-stu-id="16a7e-110">Reference</span></span>

[<span data-ttu-id="16a7e-111">Класс Вистагрбитс</span><span class="sxs-lookup"><span data-stu-id="16a7e-111">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="16a7e-112">Элементы Вистагрбитс</span><span class="sxs-lookup"><span data-stu-id="16a7e-112">VistaGrbits members</span></span>](./vistagrbits-members.md)

[<span data-ttu-id="16a7e-113">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="16a7e-113">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
