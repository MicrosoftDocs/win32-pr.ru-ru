---
description: 'Дополнительные сведения: структура JET_SIGNATURE'
title: Структура JET_SIGNATURE
TOCTitle: JET_SIGNATURE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SIGNATURE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature(v=EXCHG.10)
ms:contentKeyID: 39511048
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5c8ce12b23194aea2a45c273e0207f88faad6f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701661"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="1d895-103">Структура JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="1d895-103">JET_SIGNATURE structure</span></span>

<span data-ttu-id="1d895-104">Структура JET_SIGNATURE содержит сведения, которые однозначно идентифицируют базу данных или последовательность файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="1d895-104">The JET_SIGNATURE structure contains information that uniquely identifies a database or logfile sequence.</span></span>

<span data-ttu-id="1d895-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1d895-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1d895-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1d895-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1d895-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d895-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_SIGNATURE _
    Implements IEquatable(Of JET_SIGNATURE)
'Usage
Dim instance As JET_SIGNATURE
```

``` csharp
[SerializableAttribute]
public struct JET_SIGNATURE : IEquatable<JET_SIGNATURE>
```

## <a name="thread-safety"></a><span data-ttu-id="1d895-108">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="1d895-108">Thread safety</span></span>

<span data-ttu-id="1d895-109">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="1d895-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1d895-110">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="1d895-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d895-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d895-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1d895-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="1d895-112">Reference</span></span>

[<span data-ttu-id="1d895-113">Элементы JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="1d895-113">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="1d895-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1d895-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
