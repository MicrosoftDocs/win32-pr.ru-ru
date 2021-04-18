---
description: 'Дополнительные сведения: неявное преобразование экземпляра (экземпляр в JET_INSTANCE)'
title: Неявное преобразование экземпляра (экземпляр JET_INSTANCE)
TOCTitle: Implicit conversion (Instance to JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.op_Implicit(Microsoft.Isam.Esent.Interop.Instance)~Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55103290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
- Microsoft.Isam.Esent.Interop.Instance.op_Implicit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7dbac9f0b5736970cf51aef9e99f2877cfd488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719430"
---
# <a name="instance-implicit-conversion-instance-to-jet_instance"></a><span data-ttu-id="fbcbb-103">Неявное преобразование экземпляра (экземпляр JET_INSTANCE)</span><span class="sxs-lookup"><span data-stu-id="fbcbb-103">Instance Implicit conversion (Instance to JET_INSTANCE)</span></span>

<span data-ttu-id="fbcbb-104">Предоставьте неявное преобразование объекта экземпляра в структуру JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="fbcbb-104">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="fbcbb-105">Это делается так, что экземпляр можно использовать в любом месте, где требуется JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="fbcbb-105">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span>

<span data-ttu-id="fbcbb-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fbcbb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fbcbb-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fbcbb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fbcbb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbcbb-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    instance As Instance _
) As JET_INSTANCE
'Usage
Dim input As Instance
Dim output As JET_INSTANCE

output = CType(input, JET_INSTANCE)
```

``` csharp
public static implicit operator JET_INSTANCE (
    Instance instance
)
```

#### <a name="parameters"></a><span data-ttu-id="fbcbb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbcbb-109">Parameters</span></span>

  - <span data-ttu-id="fbcbb-110">экземпляр</span><span class="sxs-lookup"><span data-stu-id="fbcbb-110">instance</span></span>  
    <span data-ttu-id="fbcbb-111">Тип: [Microsoft. ISAM. ESENT. Interop. instance](./instance-class.md)</span><span class="sxs-lookup"><span data-stu-id="fbcbb-111">Type: [Microsoft.Isam.Esent.Interop.Instance](./instance-class.md)</span></span>  
    
    <span data-ttu-id="fbcbb-112">Преобразуемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="fbcbb-112">The instance to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fbcbb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbcbb-113">Return value</span></span>

<span data-ttu-id="fbcbb-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fbcbb-114">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
<span data-ttu-id="fbcbb-115">JET_INSTANCE, инкапсулированный экземпляром.</span><span class="sxs-lookup"><span data-stu-id="fbcbb-115">The JET_INSTANCE wrapped by the instance.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fbcbb-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbcbb-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fbcbb-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="fbcbb-117">Reference</span></span>

[<span data-ttu-id="fbcbb-118">Класс экземпляра</span><span class="sxs-lookup"><span data-stu-id="fbcbb-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="fbcbb-119">Члены экземпляра</span><span class="sxs-lookup"><span data-stu-id="fbcbb-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="fbcbb-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fbcbb-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
