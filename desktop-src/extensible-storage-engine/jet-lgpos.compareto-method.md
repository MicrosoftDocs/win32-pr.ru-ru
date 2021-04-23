---
description: Дополнительные сведения о методе JET_LGPOS. CompareTo
title: JET_LGPOS. CompareTo, метод
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo(Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.compareto(v=EXCHG.10)
ms:contentKeyID: 39514516
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83012ed755ab876618147c013e99868927e16f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683882"
---
# <a name="jet_lgposcompareto-method"></a><span data-ttu-id="80568-103">JET_LGPOS. CompareTo, метод</span><span class="sxs-lookup"><span data-stu-id="80568-103">JET_LGPOS.CompareTo method</span></span>

<span data-ttu-id="80568-104">Сравнивает эту точку журнала с другим положением журнала и определяет, является ли этот экземпляр предшествующим, таким же, как и после другого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="80568-104">Compares this log position to another log position and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="80568-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="80568-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="80568-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="80568-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="80568-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80568-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_LGPOS _
) As Integer
'Usage
Dim instance As JET_LGPOS
Dim other As JET_LGPOS
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_LGPOS other
)
```

#### <a name="parameters"></a><span data-ttu-id="80568-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="80568-108">Parameters</span></span>

  - <span data-ttu-id="80568-109">др.</span><span class="sxs-lookup"><span data-stu-id="80568-109">other</span></span>  
    <span data-ttu-id="80568-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="80568-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="80568-111">Расположение журнала, сравниваемое с текущим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="80568-111">The log position to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="80568-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80568-112">Return value</span></span>

<span data-ttu-id="80568-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="80568-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="80568-114">Число со знаком, указывающее относительное положение данного экземпляра и параметра value.</span><span class="sxs-lookup"><span data-stu-id="80568-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="80568-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="80568-115">Implements</span></span>

[<span data-ttu-id="80568-116">Интерфейс IComparable \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="80568-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="80568-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80568-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="80568-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="80568-118">Reference</span></span>

[<span data-ttu-id="80568-119">Структура JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="80568-119">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="80568-120">Элементы JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="80568-120">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="80568-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="80568-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
