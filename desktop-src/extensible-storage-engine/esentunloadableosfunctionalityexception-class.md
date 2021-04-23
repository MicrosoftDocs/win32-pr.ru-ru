---
description: 'Дополнительные сведения о: Есентунлоадаблеосфунктионалитексцептион Class'
title: Класс Есентунлоадаблеосфунктионалитексцептион
TOCTitle: EsentUnloadableOSFunctionalityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentunloadableosfunctionalityexception(v=EXCHG.10)
ms:contentKeyID: 55107333
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81b1151be5020a07f92582e762c6e6597138d9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683888"
---
# <a name="esentunloadableosfunctionalityexception-class"></a><span data-ttu-id="4cfd7-103">Класс Есентунлоадаблеосфунктионалитексцептион</span><span class="sxs-lookup"><span data-stu-id="4cfd7-103">EsentUnloadableOSFunctionalityException class</span></span>

<span data-ttu-id="4cfd7-104">Базовый класс для JET_err. Исключения Унлоадаблеосфунктионалити.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-104">Base class for JET_err.UnloadableOSFunctionality exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4cfd7-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="4cfd7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4cfd7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4cfd7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4cfd7-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4cfd7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4cfd7-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="4cfd7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4cfd7-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="4cfd7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4cfd7-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="4cfd7-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="4cfd7-111">Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="4cfd7-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="4cfd7-112">Microsoft. ISAM. ESENT. Interop. Есентунлоадаблеосфунктионалитексцептион</span><span class="sxs-lookup"><span data-stu-id="4cfd7-112">Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException</span></span>  

<span data-ttu-id="4cfd7-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4cfd7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4cfd7-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4cfd7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfd7-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cfd7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUnloadableOSFunctionalityException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentUnloadableOSFunctionalityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUnloadableOSFunctionalityException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="4cfd7-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="4cfd7-116">Thread safety</span></span>

<span data-ttu-id="4cfd7-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4cfd7-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cfd7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cfd7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4cfd7-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="4cfd7-120">Reference</span></span>

[<span data-ttu-id="4cfd7-121">Элементы Есентунлоадаблеосфунктионалитексцептион</span><span class="sxs-lookup"><span data-stu-id="4cfd7-121">EsentUnloadableOSFunctionalityException members</span></span>](./esentunloadableosfunctionalityexception-members.md)

[<span data-ttu-id="4cfd7-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4cfd7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
