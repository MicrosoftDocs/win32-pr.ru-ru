---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Циркуларлог'
title: Инстанцепараметерс. Циркуларлог, свойство
TOCTitle: 'CircularLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.circularlog(v=EXCHG.10)
ms:contentKeyID: 55103320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CircularLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f9a77aa0d0f60b49269dc939787b165a3f2f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713156"
---
# <a name="instanceparameterscircularlog-property"></a><span data-ttu-id="5fd7e-103">Инстанцепараметерс. Циркуларлог, свойство</span><span class="sxs-lookup"><span data-stu-id="5fd7e-103">InstanceParameters.CircularLog property</span></span>

<span data-ttu-id="5fd7e-104">Возвращает или задает значение, указывающее, включено ли циклическое ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="5fd7e-104">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="5fd7e-105">Если циклическое ведение журнала отключено, все созданные файлы журнала транзакций сохраняются на диске до тех пор, пока они больше не нужны, так как была выполнена полная резервная копия базы данных.</span><span class="sxs-lookup"><span data-stu-id="5fd7e-105">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="5fd7e-106">Если циклическое ведение журнала включено, на диске сохраняются только файлы журнала транзакций, которые являются моложе текущей контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="5fd7e-106">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="5fd7e-107">Преимущество этого режима заключается в том, что для снятия старых файлов журнала транзакций резервные копии не требуются.</span><span class="sxs-lookup"><span data-stu-id="5fd7e-107">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span>

<span data-ttu-id="5fd7e-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5fd7e-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5fd7e-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5fd7e-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd7e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fd7e-110">Syntax</span></span>

``` vb
'Declaration
Public Property CircularLog As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CircularLog

instance.CircularLog = value
```

``` csharp
public bool CircularLog { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5fd7e-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5fd7e-111">Property value</span></span>

<span data-ttu-id="5fd7e-112">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="5fd7e-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5fd7e-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fd7e-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5fd7e-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="5fd7e-114">Reference</span></span>

[<span data-ttu-id="5fd7e-115">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="5fd7e-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="5fd7e-116">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="5fd7e-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="5fd7e-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5fd7e-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
