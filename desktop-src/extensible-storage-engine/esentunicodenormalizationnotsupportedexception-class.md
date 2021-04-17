---
description: 'Дополнительные сведения о: Есентуникоденормализатионнотсуппортедексцептион Class'
title: Класс Есентуникоденормализатионнотсуппортедексцептион
TOCTitle: EsentUnicodeNormalizationNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentunicodenormalizationnotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f11b74602997f356bea15e6b0d422ab30e3775be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702816"
---
# <a name="esentunicodenormalizationnotsupportedexception-class"></a><span data-ttu-id="28f45-103">Класс Есентуникоденормализатионнотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="28f45-103">EsentUnicodeNormalizationNotSupportedException class</span></span>

<span data-ttu-id="28f45-104">Базовый класс для JET_err. Исключения Уникоденормализатионнотсуппортед.</span><span class="sxs-lookup"><span data-stu-id="28f45-104">Base class for JET_err.UnicodeNormalizationNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="28f45-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="28f45-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="28f45-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="28f45-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="28f45-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="28f45-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="28f45-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="28f45-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="28f45-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="28f45-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="28f45-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="28f45-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="28f45-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="28f45-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="28f45-112">Microsoft. ISAM. ESENT. Interop. Есентуникоденормализатионнотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="28f45-112">Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException</span></span>  

<span data-ttu-id="28f45-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="28f45-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="28f45-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="28f45-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="28f45-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28f45-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUnicodeNormalizationNotSupportedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentUnicodeNormalizationNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUnicodeNormalizationNotSupportedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="28f45-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="28f45-116">Thread safety</span></span>

<span data-ttu-id="28f45-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="28f45-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="28f45-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="28f45-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="28f45-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28f45-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="28f45-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="28f45-120">Reference</span></span>

[<span data-ttu-id="28f45-121">Элементы Есентуникоденормализатионнотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="28f45-121">EsentUnicodeNormalizationNotSupportedException members</span></span>](./esentunicodenormalizationnotsupportedexception-members.md)

[<span data-ttu-id="28f45-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="28f45-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
