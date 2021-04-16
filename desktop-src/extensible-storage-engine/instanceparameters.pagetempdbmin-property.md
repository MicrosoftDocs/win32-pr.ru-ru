---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Пажетемпдбмин'
title: Инстанцепараметерс. Пажетемпдбмин, свойство
TOCTitle: 'PageTempDBMin property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.pagetempdbmin(v=EXCHG.10)
ms:contentKeyID: 55103558
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06825762485ad52743d585ce0fed86bd1739cd21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712164"
---
# <a name="instanceparameterspagetempdbmin-property"></a><span data-ttu-id="1aa75-103">Инстанцепараметерс. Пажетемпдбмин, свойство</span><span class="sxs-lookup"><span data-stu-id="1aa75-103">InstanceParameters.PageTempDBMin property</span></span>

<span data-ttu-id="1aa75-104">Возвращает или задает начальный размер временной базы данных.</span><span class="sxs-lookup"><span data-stu-id="1aa75-104">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="1aa75-105">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="1aa75-105">The size is in database pages.</span></span> <span data-ttu-id="1aa75-106">Нулевой размер означает, что следует использовать стандартный размер обычной базы данных.</span><span class="sxs-lookup"><span data-stu-id="1aa75-106">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="1aa75-107">Часто нежелательно, чтобы небольшие приложения настроили временную базу данных как можно меньше.</span><span class="sxs-lookup"><span data-stu-id="1aa75-107">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="1aa75-108">Если задать для этого параметра значение [пажетемпдбсмаллест](./systemparameters.pagetempdbsmallest-field.md) , будет достигнута наименьшая временная база данных.</span><span class="sxs-lookup"><span data-stu-id="1aa75-108">Setting this parameter to [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) will achieve the smallest temporary database possible.</span></span>

<span data-ttu-id="1aa75-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1aa75-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1aa75-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1aa75-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa75-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1aa75-111">Syntax</span></span>

``` vb
'Declaration
Public Property PageTempDBMin As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PageTempDBMin

instance.PageTempDBMin = value
```

``` csharp
public int PageTempDBMin { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1aa75-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1aa75-112">Property value</span></span>

<span data-ttu-id="1aa75-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1aa75-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1aa75-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1aa75-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1aa75-115">Справочник</span><span class="sxs-lookup"><span data-stu-id="1aa75-115">Reference</span></span>

[<span data-ttu-id="1aa75-116">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="1aa75-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="1aa75-117">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="1aa75-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="1aa75-118">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1aa75-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
