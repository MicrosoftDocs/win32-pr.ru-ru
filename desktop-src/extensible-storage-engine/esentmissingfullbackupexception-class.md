---
description: 'Дополнительные сведения о: Есентмиссингфуллбаккупексцептион Class'
title: Класс Есентмиссингфуллбаккупексцептион
TOCTitle: EsentMissingFullBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingfullbackupexception(v=EXCHG.10)
ms:contentKeyID: 55102230
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c345475e9e23f60460d7ee5eb901e5997ecb6062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155730"
---
# <a name="esentmissingfullbackupexception-class"></a><span data-ttu-id="a881c-103">Класс Есентмиссингфуллбаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="a881c-103">EsentMissingFullBackupException class</span></span>

<span data-ttu-id="a881c-104">Базовый класс для JET_err. Исключения Миссингфуллбаккуп.</span><span class="sxs-lookup"><span data-stu-id="a881c-104">Base class for JET_err.MissingFullBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a881c-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="a881c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a881c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a881c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a881c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a881c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a881c-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="a881c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a881c-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="a881c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a881c-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="a881c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a881c-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="a881c-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="a881c-112">Microsoft. ISAM. ESENT. Interop. Есентмиссингфуллбаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="a881c-112">Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException</span></span>  

<span data-ttu-id="a881c-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a881c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a881c-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a881c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a881c-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a881c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingFullBackupException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMissingFullBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingFullBackupException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="a881c-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="a881c-116">Thread safety</span></span>

<span data-ttu-id="a881c-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="a881c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a881c-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="a881c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a881c-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a881c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a881c-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="a881c-120">Reference</span></span>

[<span data-ttu-id="a881c-121">Элементы Есентмиссингфуллбаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="a881c-121">EsentMissingFullBackupException members</span></span>](./esentmissingfullbackupexception-members.md)

[<span data-ttu-id="a881c-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a881c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
