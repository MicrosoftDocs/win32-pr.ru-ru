---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Макскурсорс'
title: Инстанцепараметерс. Макскурсорс, свойство
TOCTitle: 'MaxCursors property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxcursors(v=EXCHG.10)
ms:contentKeyID: 55103565
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxCursors
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 029ff7c41916e668f532be60f018870f30e487ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713155"
---
# <a name="instanceparametersmaxcursors-property"></a><span data-ttu-id="e9521-103">Инстанцепараметерс. Макскурсорс, свойство</span><span class="sxs-lookup"><span data-stu-id="e9521-103">InstanceParameters.MaxCursors property</span></span>

<span data-ttu-id="e9521-104">Возвращает или задает количество ресурсов курсора, зарезервированных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e9521-104">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="e9521-105">Ресурс курсора непосредственно соответствует JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="e9521-105">A cursor resource directly corresponds to a JET_TABLEID.</span></span>

<span data-ttu-id="e9521-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e9521-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e9521-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e9521-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e9521-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9521-108">Syntax</span></span>

``` vb
'Declaration
Public Property MaxCursors As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxCursors

instance.MaxCursors = value
```

``` csharp
public int MaxCursors { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e9521-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e9521-109">Property value</span></span>

<span data-ttu-id="e9521-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e9521-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e9521-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9521-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e9521-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="e9521-112">Reference</span></span>

[<span data-ttu-id="e9521-113">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="e9521-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="e9521-114">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="e9521-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="e9521-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e9521-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
