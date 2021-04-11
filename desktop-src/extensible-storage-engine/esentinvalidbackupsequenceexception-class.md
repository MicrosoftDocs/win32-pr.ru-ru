---
description: 'Дополнительные сведения о: Есентинвалидбаккупсекуенцеексцептион Class'
title: Класс Есентинвалидбаккупсекуенцеексцептион
TOCTitle: EsentInvalidBackupSequenceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidBackupSequenceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidbackupsequenceexception(v=EXCHG.10)
ms:contentKeyID: 55101852
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidBackupSequenceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidBackupSequenceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd3707729f0fcbccfab5e8f7f2dc2c33d5ed4e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264980"
---
# <a name="esentinvalidbackupsequenceexception-class"></a><span data-ttu-id="b400b-103">Класс Есентинвалидбаккупсекуенцеексцептион</span><span class="sxs-lookup"><span data-stu-id="b400b-103">EsentInvalidBackupSequenceException class</span></span>

<span data-ttu-id="b400b-104">Базовый класс для JET_err. Исключения Инвалидбаккупсекуенце.</span><span class="sxs-lookup"><span data-stu-id="b400b-104">Base class for JET_err.InvalidBackupSequence exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b400b-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="b400b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b400b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b400b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b400b-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b400b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b400b-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="b400b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b400b-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b400b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b400b-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="b400b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b400b-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="b400b-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b400b-112">Microsoft. ISAM. ESENT. Interop. Есентинвалидбаккупсекуенцеексцептион</span><span class="sxs-lookup"><span data-stu-id="b400b-112">Microsoft.Isam.Esent.Interop.EsentInvalidBackupSequenceException</span></span>  

<span data-ttu-id="b400b-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b400b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b400b-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b400b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b400b-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b400b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidBackupSequenceException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidBackupSequenceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidBackupSequenceException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b400b-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="b400b-116">Thread safety</span></span>

<span data-ttu-id="b400b-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="b400b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b400b-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b400b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b400b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b400b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b400b-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="b400b-120">Reference</span></span>

[<span data-ttu-id="b400b-121">Элементы Есентинвалидбаккупсекуенцеексцептион</span><span class="sxs-lookup"><span data-stu-id="b400b-121">EsentInvalidBackupSequenceException members</span></span>](./esentinvalidbackupsequenceexception-members.md)

[<span data-ttu-id="b400b-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b400b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
