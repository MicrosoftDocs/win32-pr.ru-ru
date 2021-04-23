---
description: 'Дополнительные сведения: структура JET_INSTANCE'
title: Структура JET_INSTANCE
TOCTitle: JET_INSTANCE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance(v=EXCHG.10)
ms:contentKeyID: 39510997
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a676c0815ba20b725da0216a7c9a145c1c1cfd68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265557"
---
# <a name="jet_instance-structure"></a><span data-ttu-id="c808b-103">Структура JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c808b-103">JET_INSTANCE structure</span></span>

<span data-ttu-id="c808b-104">JET_INSTANCE содержит обработчик для экземпляра базы данных, используемый для вызовов API JET.</span><span class="sxs-lookup"><span data-stu-id="c808b-104">A JET_INSTANCE contains a handle to the instance of the database to use for calls to the JET API.</span></span>

<span data-ttu-id="c808b-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c808b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c808b-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c808b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c808b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c808b-107">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INSTANCE _
    Implements IEquatable(Of JET_INSTANCE), IFormattable
'Usage
Dim instance As JET_INSTANCE
```

``` csharp
public struct JET_INSTANCE : IEquatable<JET_INSTANCE>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="c808b-108">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="c808b-108">Thread safety</span></span>

<span data-ttu-id="c808b-109">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="c808b-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c808b-110">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="c808b-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c808b-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c808b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c808b-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="c808b-112">Reference</span></span>

[<span data-ttu-id="c808b-113">Элементы JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c808b-113">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="c808b-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c808b-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
