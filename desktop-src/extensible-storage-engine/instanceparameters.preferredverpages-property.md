---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Преферредверпажес'
title: Инстанцепараметерс. Преферредверпажес, свойство
TOCTitle: 'PreferredVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.preferredverpages(v=EXCHG.10)
ms:contentKeyID: 55103322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PreferredVerPages
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 067d41cd3fb945b2f18d3cd6154b1eef6793b1e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712162"
---
# <a name="instanceparameterspreferredverpages-property"></a><span data-ttu-id="eb2fb-103">Инстанцепараметерс. Преферредверпажес, свойство</span><span class="sxs-lookup"><span data-stu-id="eb2fb-103">InstanceParameters.PreferredVerPages property</span></span>

<span data-ttu-id="eb2fb-104">Возвращает или задает предпочтительное количество страниц хранилища версий, зарезервированных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="eb2fb-104">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="eb2fb-105">Если размер хранилища версий превышает это пороговое значение, то любая информация, которая используется только для необязательных фоновых задач, таких как освобождение места на удаленном диске в базе данных, задается для сохранения сведений о транзакциях.</span><span class="sxs-lookup"><span data-stu-id="eb2fb-105">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="eb2fb-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb2fb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb2fb-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb2fb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2fb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb2fb-108">Syntax</span></span>

``` vb
'Declaration
Public Property PreferredVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PreferredVerPages

instance.PreferredVerPages = value
```

``` csharp
public int PreferredVerPages { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="eb2fb-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="eb2fb-109">Property value</span></span>

<span data-ttu-id="eb2fb-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="eb2fb-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="eb2fb-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb2fb-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb2fb-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="eb2fb-112">Reference</span></span>

[<span data-ttu-id="eb2fb-113">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="eb2fb-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="eb2fb-114">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="eb2fb-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="eb2fb-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="eb2fb-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
