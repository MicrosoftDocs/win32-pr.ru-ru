---
description: 'Дополнительные сведения о: JET_DBID. Метод Equals (JET_DBID)'
title: JET_DBID. Метод Equals (JET_DBID)
TOCTitle: Equals method (JET_DBID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.Equals(Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.equals(v=EXCHG.10)
ms:contentKeyID: 39514199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9023108f1a1b3ffe565519607ab1498af363d40d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647567"
---
# <a name="jet_dbidequals-method-jet_dbid"></a><span data-ttu-id="7add7-103">JET_DBID. Метод Equals (JET_DBID)</span><span class="sxs-lookup"><span data-stu-id="7add7-103">JET_DBID.Equals method (JET_DBID)</span></span>

<span data-ttu-id="7add7-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="7add7-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="7add7-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7add7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7add7-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7add7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7add7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7add7-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_DBID _
) As Boolean
'Usage
Dim instance As JET_DBID
Dim other As JET_DBID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_DBID other
)
```

#### <a name="parameters"></a><span data-ttu-id="7add7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7add7-108">Parameters</span></span>

  - <span data-ttu-id="7add7-109">др.</span><span class="sxs-lookup"><span data-stu-id="7add7-109">other</span></span>  
    <span data-ttu-id="7add7-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7add7-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="7add7-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="7add7-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7add7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7add7-112">Return value</span></span>

<span data-ttu-id="7add7-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7add7-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7add7-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="7add7-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="7add7-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="7add7-115">Implements</span></span>

[<span data-ttu-id="7add7-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="7add7-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="7add7-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7add7-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7add7-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="7add7-118">Reference</span></span>

[<span data-ttu-id="7add7-119">Структура JET_DBID</span><span class="sxs-lookup"><span data-stu-id="7add7-119">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="7add7-120">Элементы JET_DBID</span><span class="sxs-lookup"><span data-stu-id="7add7-120">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="7add7-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="7add7-121">Equals overload</span></span>](./jet-dbid.equals-method.md)

[<span data-ttu-id="7add7-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7add7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
