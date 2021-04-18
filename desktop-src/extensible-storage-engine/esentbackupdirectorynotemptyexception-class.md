---
description: 'Дополнительные сведения о: Есентбаккупдиректоринотемптексцептион Class'
title: Класс Есентбаккупдиректоринотемптексцептион
TOCTitle: EsentBackupDirectoryNotEmptyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupdirectorynotemptyexception(v=EXCHG.10)
ms:contentKeyID: 55101028
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4553d8edc1218e09adcbe1ae4967ceb256d811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424033"
---
# <a name="esentbackupdirectorynotemptyexception-class"></a><span data-ttu-id="77e80-103">Класс Есентбаккупдиректоринотемптексцептион</span><span class="sxs-lookup"><span data-stu-id="77e80-103">EsentBackupDirectoryNotEmptyException class</span></span>

<span data-ttu-id="77e80-104">Базовый класс для JET_err. Исключения Баккупдиректоринотемпти.</span><span class="sxs-lookup"><span data-stu-id="77e80-104">Base class for JET_err.BackupDirectoryNotEmpty exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="77e80-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="77e80-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="77e80-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="77e80-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="77e80-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="77e80-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="77e80-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="77e80-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="77e80-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="77e80-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="77e80-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="77e80-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="77e80-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="77e80-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="77e80-112">Microsoft. ISAM. ESENT. Interop. Есентбаккупдиректоринотемптексцептион</span><span class="sxs-lookup"><span data-stu-id="77e80-112">Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException</span></span>  

<span data-ttu-id="77e80-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="77e80-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="77e80-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="77e80-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="77e80-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77e80-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupDirectoryNotEmptyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentBackupDirectoryNotEmptyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupDirectoryNotEmptyException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="77e80-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="77e80-116">Thread safety</span></span>

<span data-ttu-id="77e80-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="77e80-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="77e80-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="77e80-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="77e80-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77e80-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="77e80-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="77e80-120">Reference</span></span>

[<span data-ttu-id="77e80-121">Элементы Есентбаккупдиректоринотемптексцептион</span><span class="sxs-lookup"><span data-stu-id="77e80-121">EsentBackupDirectoryNotEmptyException members</span></span>](./esentbackupdirectorynotemptyexception-members.md)

[<span data-ttu-id="77e80-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="77e80-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
