---
description: 'Дополнительные сведения: структура JET_LS'
title: Структура JET_LS
TOCTitle: JET_LS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls(v=EXCHG.10)
ms:contentKeyID: 39510760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d32c1a6815cfa7552fed0d8f1a01376ae0eacaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265548"
---
# <a name="jet_ls-structure"></a><span data-ttu-id="a5c82-103">Структура JET_LS</span><span class="sxs-lookup"><span data-stu-id="a5c82-103">JET_LS structure</span></span>

<span data-ttu-id="a5c82-104">Локальное хранилище для маркера ESENT.</span><span class="sxs-lookup"><span data-stu-id="a5c82-104">Local storage for an ESENT handle.</span></span> <span data-ttu-id="a5c82-105">Используется [жетжетлс (JET_SESID, JET_TABLEID, JET_LS, лсгрбит)](./api.jetgetls-method.md) и [жетсетлс (JET_SESID, JET_TABLEID, JET_LS, лсгрбит)](./api.jetsetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="a5c82-105">Used by [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md) and [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span>

<span data-ttu-id="a5c82-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a5c82-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a5c82-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a5c82-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c82-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5c82-108">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_LS _
    Implements IEquatable(Of JET_LS), IFormattable
'Usage
Dim instance As JET_LS
```

``` csharp
public struct JET_LS : IEquatable<JET_LS>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="a5c82-109">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="a5c82-109">Thread safety</span></span>

<span data-ttu-id="a5c82-110">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="a5c82-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a5c82-111">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="a5c82-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5c82-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5c82-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a5c82-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="a5c82-113">Reference</span></span>

[<span data-ttu-id="a5c82-114">Элементы JET_LS</span><span class="sxs-lookup"><span data-stu-id="a5c82-114">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="a5c82-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a5c82-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
