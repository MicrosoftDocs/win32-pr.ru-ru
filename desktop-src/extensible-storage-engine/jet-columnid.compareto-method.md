---
description: Дополнительные сведения о методе JET_COLUMNID. CompareTo
title: JET_COLUMNID. CompareTo, метод
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.compareto(v=EXCHG.10)
ms:contentKeyID: 39509744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7eea24875b0639f7f5b7968084a3fff2aa7cccec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155022"
---
# <a name="jet_columnidcompareto-method"></a><span data-ttu-id="e05d8-103">JET_COLUMNID. CompareTo, метод</span><span class="sxs-lookup"><span data-stu-id="e05d8-103">JET_COLUMNID.CompareTo method</span></span>

<span data-ttu-id="e05d8-104">Сравнивает это значение columnid с другим columnid и определяет, является ли данный экземпляр предшествующим, таким же, как и после другого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e05d8-104">Compares this columnid to another columnid and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="e05d8-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e05d8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e05d8-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e05d8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e05d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e05d8-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COLUMNID _
) As Integer
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a><span data-ttu-id="e05d8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e05d8-108">Parameters</span></span>

  - <span data-ttu-id="e05d8-109">др.</span><span class="sxs-lookup"><span data-stu-id="e05d8-109">other</span></span>  
    <span data-ttu-id="e05d8-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e05d8-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e05d8-111">Значение columnid, сравниваемое с текущим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="e05d8-111">The columnid to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e05d8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e05d8-112">Return value</span></span>

<span data-ttu-id="e05d8-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e05d8-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="e05d8-114">Число со знаком, указывающее относительное положение данного экземпляра и параметра value.</span><span class="sxs-lookup"><span data-stu-id="e05d8-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="e05d8-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="e05d8-115">Implements</span></span>

[<span data-ttu-id="e05d8-116">Интерфейс IComparable \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="e05d8-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="e05d8-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e05d8-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e05d8-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="e05d8-118">Reference</span></span>

[<span data-ttu-id="e05d8-119">Структура JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e05d8-119">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="e05d8-120">Элементы JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e05d8-120">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="e05d8-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e05d8-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
