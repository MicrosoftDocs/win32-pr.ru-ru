---
description: 'Дополнительные сведения о свойстве: Есентверсион. Суппортсларжекэйс'
title: Есентверсион. Суппортсларжекэйс, свойство
TOCTitle: 'SupportsLargeKeys property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversion.supportslargekeys(v=EXCHG.10)
ms:contentKeyID: 55103180
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
- Microsoft.Isam.Esent.Interop.EsentVersion.get_SupportsLargeKeys
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43ee88b7c0e190d9c717c087deeb5fc4556e6575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647745"
---
# <a name="esentversionsupportslargekeys-property"></a><span data-ttu-id="6229d-103">Есентверсион. Суппортсларжекэйс, свойство</span><span class="sxs-lookup"><span data-stu-id="6229d-103">EsentVersion.SupportsLargeKeys property</span></span>

<span data-ttu-id="6229d-104">Возвращает значение, указывающее, поддерживаются ли большие ( \> 255 байта) ключи.</span><span class="sxs-lookup"><span data-stu-id="6229d-104">Gets a value that indicates whether large (\> 255 byte) keys are supported.</span></span> <span data-ttu-id="6229d-105">Размер ключа для индекса можно указать в объекте [JET_INDEXCREATE](./jet-indexcreate-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6229d-105">The key size for an index can be specified in the [JET_INDEXCREATE](./jet-indexcreate-class.md) object.</span></span>

<span data-ttu-id="6229d-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6229d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6229d-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6229d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6229d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6229d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared ReadOnly Property SupportsLargeKeys As Boolean
    Get
'Usage
Dim value As Boolean

value = EsentVersion.SupportsLargeKeys
```

``` csharp
public static bool SupportsLargeKeys { get; }
```

#### <a name="property-value"></a><span data-ttu-id="6229d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6229d-109">Property value</span></span>

<span data-ttu-id="6229d-110">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6229d-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6229d-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6229d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6229d-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="6229d-112">Reference</span></span>

[<span data-ttu-id="6229d-113">Класс Есентверсион</span><span class="sxs-lookup"><span data-stu-id="6229d-113">EsentVersion class</span></span>](./esentversion-class.md)

[<span data-ttu-id="6229d-114">Элементы Есентверсион</span><span class="sxs-lookup"><span data-stu-id="6229d-114">EsentVersion members</span></span>](./esentversion-members.md)

[<span data-ttu-id="6229d-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6229d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
