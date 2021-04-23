---
description: 'Дополнительные сведения: структура JET_DBID'
title: Структура JET_DBID
TOCTitle: JET_DBID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DBID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid(v=EXCHG.10)
ms:contentKeyID: 39515255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e92373015b64593936ee8d447b619932d168157c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910491"
---
# <a name="jet_dbid-structure"></a><span data-ttu-id="de3ce-103">Структура JET_DBID</span><span class="sxs-lookup"><span data-stu-id="de3ce-103">JET_DBID structure</span></span>

<span data-ttu-id="de3ce-104">JET_DBID содержит обработчик для базы данных.</span><span class="sxs-lookup"><span data-stu-id="de3ce-104">A JET_DBID contains the handle to the database.</span></span> <span data-ttu-id="de3ce-105">Для управления схемой базы данных используется маркер базы данных.</span><span class="sxs-lookup"><span data-stu-id="de3ce-105">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="de3ce-106">Его также можно использовать для управления таблицами в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="de3ce-106">It can also be used to manage the tables inside of that database.</span></span>

<span data-ttu-id="de3ce-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="de3ce-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="de3ce-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="de3ce-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="de3ce-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de3ce-109">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_DBID _
    Implements IEquatable(Of JET_DBID), IFormattable
'Usage
Dim instance As JET_DBID
```

``` csharp
public struct JET_DBID : IEquatable<JET_DBID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="de3ce-110">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="de3ce-110">Thread safety</span></span>

<span data-ttu-id="de3ce-111">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="de3ce-111">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="de3ce-112">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="de3ce-112">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="de3ce-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de3ce-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="de3ce-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="de3ce-114">Reference</span></span>

[<span data-ttu-id="de3ce-115">Элементы JET_DBID</span><span class="sxs-lookup"><span data-stu-id="de3ce-115">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="de3ce-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="de3ce-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
