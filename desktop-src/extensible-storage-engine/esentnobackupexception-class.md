---
description: 'Дополнительные сведения о: Есентнобаккупексцептион Class'
title: Класс Есентнобаккупексцептион
TOCTitle: EsentNoBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnobackupexception(v=EXCHG.10)
ms:contentKeyID: 55102284
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoBackupException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 057e9e657c14e0ae0629618e7e7b138e053c5995
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809203"
---
# <a name="esentnobackupexception-class"></a><span data-ttu-id="ad705-103">Класс Есентнобаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="ad705-103">EsentNoBackupException class</span></span>

<span data-ttu-id="ad705-104">Базовый класс для JET_err. Исключения при создании резервной копии.</span><span class="sxs-lookup"><span data-stu-id="ad705-104">Base class for JET_err.NoBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ad705-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="ad705-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ad705-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ad705-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ad705-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ad705-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ad705-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ad705-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ad705-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ad705-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ad705-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="ad705-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ad705-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ad705-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="ad705-112">Microsoft. ISAM. ESENT. Interop. Есентнобаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="ad705-112">Microsoft.Isam.Esent.Interop.EsentNoBackupException</span></span>  

<span data-ttu-id="ad705-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ad705-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ad705-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ad705-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ad705-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad705-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoBackupException _
    Inherits EsentStateException
'Usage
Dim instance As EsentNoBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoBackupException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="ad705-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ad705-116">Thread safety</span></span>

<span data-ttu-id="ad705-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ad705-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ad705-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="ad705-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad705-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad705-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ad705-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="ad705-120">Reference</span></span>

[<span data-ttu-id="ad705-121">Элементы Есентнобаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="ad705-121">EsentNoBackupException members</span></span>](./esentnobackupexception-members.md)

[<span data-ttu-id="ad705-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ad705-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
