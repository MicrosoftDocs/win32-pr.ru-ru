---
description: 'Дополнительные сведения о: Есентмиссингфилетобаккупексцептион Class'
title: Класс Есентмиссингфилетобаккупексцептион
TOCTitle: EsentMissingFileToBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingfiletobackupexception(v=EXCHG.10)
ms:contentKeyID: 55102216
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5941140df070abb3a273378f3ec275eaf1c6fdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263725"
---
# <a name="esentmissingfiletobackupexception-class"></a><span data-ttu-id="8fec5-103">Класс Есентмиссингфилетобаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="8fec5-103">EsentMissingFileToBackupException class</span></span>

<span data-ttu-id="8fec5-104">Базовый класс для JET_err. Исключения Миссингфилетобаккуп.</span><span class="sxs-lookup"><span data-stu-id="8fec5-104">Base class for JET_err.MissingFileToBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8fec5-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="8fec5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8fec5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8fec5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8fec5-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="8fec5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8fec5-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="8fec5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8fec5-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="8fec5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8fec5-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="8fec5-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="8fec5-111">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="8fec5-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="8fec5-112">Microsoft. ISAM. ESENT. Interop. Есентмиссингфилетобаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="8fec5-112">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>  

<span data-ttu-id="8fec5-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8fec5-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8fec5-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8fec5-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8fec5-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fec5-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingFileToBackupException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingFileToBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingFileToBackupException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="8fec5-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="8fec5-116">Thread safety</span></span>

<span data-ttu-id="8fec5-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="8fec5-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8fec5-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="8fec5-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fec5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fec5-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8fec5-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="8fec5-120">Reference</span></span>

[<span data-ttu-id="8fec5-121">Элементы Есентмиссингфилетобаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="8fec5-121">EsentMissingFileToBackupException members</span></span>](./esentmissingfiletobackupexception-members.md)

[<span data-ttu-id="8fec5-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8fec5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
