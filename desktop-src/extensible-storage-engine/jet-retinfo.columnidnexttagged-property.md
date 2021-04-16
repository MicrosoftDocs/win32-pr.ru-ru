---
description: 'Дополнительные сведения о свойстве: JET_RETINFO. Колумниднексттагжед'
title: Свойство JET_RETINFO. Колумниднексттагжед
TOCTitle: 'columnidNextTagged property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.columnidnexttagged(v=EXCHG.10)
ms:contentKeyID: 55103802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_columnidNextTagged
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64114b1e998d47a2610e414304e7837ecbb17fe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702697"
---
# <a name="jet_retinfocolumnidnexttagged-property"></a><span data-ttu-id="fc60a-103">Свойство JET_RETINFO. Колумниднексттагжед</span><span class="sxs-lookup"><span data-stu-id="fc60a-103">JET_RETINFO.columnidNextTagged property</span></span>

<span data-ttu-id="fc60a-104">Получает значение columnid полученного помеченного, многозначного или разреженного столбца, когда все отмеченные столбцы извлекаются путем передачи 0 в качестве значения columnid в Жетретриевеколумн.</span><span class="sxs-lookup"><span data-stu-id="fc60a-104">Gets the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to JetRetrieveColumn.</span></span>

<span data-ttu-id="fc60a-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fc60a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fc60a-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fc60a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fc60a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc60a-107">Syntax</span></span>

``` vb
'Declaration
Public Property columnidNextTagged As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_RETINFO
Dim value As JET_COLUMNID

value = instance.columnidNextTagged
```

``` csharp
public JET_COLUMNID columnidNextTagged { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="fc60a-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fc60a-108">Property value</span></span>

<span data-ttu-id="fc60a-109">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fc60a-109">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="fc60a-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc60a-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fc60a-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="fc60a-111">Reference</span></span>

[<span data-ttu-id="fc60a-112">Класс JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="fc60a-112">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="fc60a-113">Элементы JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="fc60a-113">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="fc60a-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fc60a-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
