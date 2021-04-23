---
description: 'Дополнительные сведения о: JET_SESID. Метод Equals (JET_SESID)'
title: JET_SESID. Метод Equals (JET_SESID)
TOCTitle: Equals method (JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.Equals(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.equals(v=EXCHG.10)
ms:contentKeyID: 39511762
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f840230047fbb1b0347e399bc60b4b905d868b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682534"
---
# <a name="jet_sesidequals-method-jet_sesid"></a><span data-ttu-id="01e61-103">JET_SESID. Метод Equals (JET_SESID)</span><span class="sxs-lookup"><span data-stu-id="01e61-103">JET_SESID.Equals method (JET_SESID)</span></span>

<span data-ttu-id="01e61-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="01e61-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="01e61-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01e61-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01e61-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="01e61-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01e61-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01e61-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_SESID _
) As Boolean
'Usage
Dim instance As JET_SESID
Dim other As JET_SESID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_SESID other
)
```

#### <a name="parameters"></a><span data-ttu-id="01e61-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="01e61-108">Parameters</span></span>

  - <span data-ttu-id="01e61-109">др.</span><span class="sxs-lookup"><span data-stu-id="01e61-109">other</span></span>  
    <span data-ttu-id="01e61-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="01e61-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="01e61-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="01e61-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="01e61-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01e61-112">Return value</span></span>

<span data-ttu-id="01e61-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="01e61-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="01e61-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="01e61-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="01e61-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="01e61-115">Implements</span></span>

[<span data-ttu-id="01e61-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="01e61-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="01e61-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01e61-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01e61-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="01e61-118">Reference</span></span>

[<span data-ttu-id="01e61-119">Структура JET_SESID</span><span class="sxs-lookup"><span data-stu-id="01e61-119">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="01e61-120">Элементы JET_SESID</span><span class="sxs-lookup"><span data-stu-id="01e61-120">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="01e61-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="01e61-121">Equals overload</span></span>](./jet-sesid.equals-method.md)

[<span data-ttu-id="01e61-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="01e61-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
