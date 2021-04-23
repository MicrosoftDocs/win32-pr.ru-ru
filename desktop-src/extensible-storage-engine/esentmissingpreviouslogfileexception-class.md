---
description: 'Дополнительные сведения о: Есентмиссингпревиауслогфиликсцептион Class'
title: Класс Есентмиссингпревиауслогфиликсцептион
TOCTitle: EsentMissingPreviousLogFileException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingpreviouslogfileexception(v=EXCHG.10)
ms:contentKeyID: 55102244
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5db6203093a85dabc317876d4c3d1544356b31b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701695"
---
# <a name="esentmissingpreviouslogfileexception-class"></a><span data-ttu-id="44ec0-103">Класс Есентмиссингпревиауслогфиликсцептион</span><span class="sxs-lookup"><span data-stu-id="44ec0-103">EsentMissingPreviousLogFileException class</span></span>

<span data-ttu-id="44ec0-104">Базовый класс для JET_err. Исключения Миссингпревиауслогфиле.</span><span class="sxs-lookup"><span data-stu-id="44ec0-104">Base class for JET_err.MissingPreviousLogFile exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="44ec0-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="44ec0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="44ec0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="44ec0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="44ec0-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="44ec0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="44ec0-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="44ec0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="44ec0-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="44ec0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="44ec0-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="44ec0-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="44ec0-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="44ec0-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="44ec0-112">Microsoft. ISAM. ESENT. Interop. Есентмиссингпревиауслогфиликсцептион</span><span class="sxs-lookup"><span data-stu-id="44ec0-112">Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException</span></span>  

<span data-ttu-id="44ec0-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44ec0-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44ec0-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="44ec0-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44ec0-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44ec0-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingPreviousLogFileException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentMissingPreviousLogFileException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingPreviousLogFileException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="44ec0-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="44ec0-116">Thread safety</span></span>

<span data-ttu-id="44ec0-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="44ec0-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="44ec0-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="44ec0-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="44ec0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44ec0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44ec0-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="44ec0-120">Reference</span></span>

[<span data-ttu-id="44ec0-121">Элементы Есентмиссингпревиауслогфиликсцептион</span><span class="sxs-lookup"><span data-stu-id="44ec0-121">EsentMissingPreviousLogFileException members</span></span>](./esentmissingpreviouslogfileexception-members.md)

[<span data-ttu-id="44ec0-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="44ec0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
