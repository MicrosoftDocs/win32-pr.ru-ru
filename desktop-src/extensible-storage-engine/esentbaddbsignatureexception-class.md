---
description: 'Дополнительные сведения о: Есентбаддбсигнатуриксцептион Class'
title: Класс Есентбаддбсигнатуриксцептион
TOCTitle: EsentBadDbSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbaddbsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55107255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c0adf077cf0665c6bee2246c66af882a397c46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702509"
---
# <a name="esentbaddbsignatureexception-class"></a><span data-ttu-id="b3401-103">Класс Есентбаддбсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="b3401-103">EsentBadDbSignatureException class</span></span>

<span data-ttu-id="b3401-104">Базовый класс для JET_err. Исключения Баддбсигнатуре.</span><span class="sxs-lookup"><span data-stu-id="b3401-104">Base class for JET_err.BadDbSignature exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b3401-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="b3401-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b3401-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b3401-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b3401-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b3401-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b3401-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="b3401-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b3401-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b3401-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b3401-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="b3401-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b3401-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="b3401-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="b3401-112">Microsoft. ISAM. ESENT. Interop. Есентбаддбсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="b3401-112">Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException</span></span>  

<span data-ttu-id="b3401-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b3401-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b3401-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b3401-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b3401-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3401-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadDbSignatureException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentBadDbSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadDbSignatureException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="b3401-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="b3401-116">Thread safety</span></span>

<span data-ttu-id="b3401-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="b3401-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b3401-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b3401-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3401-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3401-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b3401-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="b3401-120">Reference</span></span>

[<span data-ttu-id="b3401-121">Элементы Есентбаддбсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="b3401-121">EsentBadDbSignatureException members</span></span>](./esentbaddbsignatureexception-members.md)

[<span data-ttu-id="b3401-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b3401-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
