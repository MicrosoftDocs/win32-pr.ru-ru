---
description: 'Дополнительные сведения: структура JET_BKINFO'
title: Структура JET_BKINFO
TOCTitle: JET_BKINFO structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo(v=EXCHG.10)
ms:contentKeyID: 39511166
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c3b0d3178abaa90fe507c06a2a997472492643c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272133"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="197c3-103">Структура JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="197c3-103">JET_BKINFO structure</span></span>

<span data-ttu-id="197c3-104">Содержит коллекцию данных о конкретном событии резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="197c3-104">Holds a collection of data about a specific backup event.</span></span>

<span data-ttu-id="197c3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="197c3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="197c3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="197c3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="197c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="197c3-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKINFO _
    Implements IEquatable(Of JET_BKINFO), INullableJetStruct
'Usage
Dim instance As JET_BKINFO
```

``` csharp
[SerializableAttribute]
public struct JET_BKINFO : IEquatable<JET_BKINFO>, 
    INullableJetStruct
```

## <a name="thread-safety"></a><span data-ttu-id="197c3-108">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="197c3-108">Thread safety</span></span>

<span data-ttu-id="197c3-109">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="197c3-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="197c3-110">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="197c3-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="197c3-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="197c3-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="197c3-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="197c3-112">Reference</span></span>

[<span data-ttu-id="197c3-113">Элементы JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="197c3-113">JET_BKINFO members</span></span>](./jet-bkinfo-members.md)

[<span data-ttu-id="197c3-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="197c3-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
