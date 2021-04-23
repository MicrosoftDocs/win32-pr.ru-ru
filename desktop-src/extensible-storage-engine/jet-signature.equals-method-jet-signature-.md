---
description: 'Дополнительные сведения о: JET_SIGNATURE. Метод Equals (JET_SIGNATURE)'
title: JET_SIGNATURE. Метод Equals (JET_SIGNATURE)
TOCTitle: Equals method (JET_SIGNATURE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals(Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.equals(v=EXCHG.10)
ms:contentKeyID: 39511830
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f099b74af84e1a75289313c5bb9d4de646b51a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542583"
---
# <a name="jet_signatureequals-method-jet_signature"></a><span data-ttu-id="6bf3e-103">JET_SIGNATURE. Метод Equals (JET_SIGNATURE)</span><span class="sxs-lookup"><span data-stu-id="6bf3e-103">JET_SIGNATURE.Equals method (JET_SIGNATURE)</span></span>

<span data-ttu-id="6bf3e-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="6bf3e-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="6bf3e-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6bf3e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6bf3e-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6bf3e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6bf3e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bf3e-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_SIGNATURE _
) As Boolean
'Usage
Dim instance As JET_SIGNATURE
Dim other As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_SIGNATURE other
)
```

#### <a name="parameters"></a><span data-ttu-id="6bf3e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bf3e-108">Parameters</span></span>

  - <span data-ttu-id="6bf3e-109">др.</span><span class="sxs-lookup"><span data-stu-id="6bf3e-109">other</span></span>  
    <span data-ttu-id="6bf3e-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="6bf3e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="6bf3e-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="6bf3e-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6bf3e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bf3e-112">Return value</span></span>

<span data-ttu-id="6bf3e-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6bf3e-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="6bf3e-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="6bf3e-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="6bf3e-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="6bf3e-115">Implements</span></span>

[<span data-ttu-id="6bf3e-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="6bf3e-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="6bf3e-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bf3e-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6bf3e-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="6bf3e-118">Reference</span></span>

[<span data-ttu-id="6bf3e-119">Структура JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="6bf3e-119">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="6bf3e-120">Элементы JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="6bf3e-120">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="6bf3e-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="6bf3e-121">Equals overload</span></span>](./jet-signature.equals-method.md)

[<span data-ttu-id="6bf3e-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6bf3e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
