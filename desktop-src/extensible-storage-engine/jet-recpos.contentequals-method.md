---
description: 'Дополнительные сведения о: JET_RECPOS. Метод Контентекуалс'
title: JET_RECPOS. Метод Контентекуалс
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_RECPOS.ContentEquals(Microsoft.Isam.Esent.Interop.JET_RECPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recpos.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103845
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECPOS.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECPOS.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cff822551bd2687308dde12df1f4e0e381f58046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911448"
---
# <a name="jet_recposcontentequals-method"></a><span data-ttu-id="21406-103">JET_RECPOS. Метод Контентекуалс</span><span class="sxs-lookup"><span data-stu-id="21406-103">JET_RECPOS.ContentEquals method</span></span>

<span data-ttu-id="21406-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="21406-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="21406-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21406-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="21406-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="21406-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21406-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21406-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_RECPOS _
) As Boolean
'Usage
Dim instance As JET_RECPOS
Dim other As JET_RECPOS
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_RECPOS other
)
```

#### <a name="parameters"></a><span data-ttu-id="21406-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="21406-108">Parameters</span></span>

  - <span data-ttu-id="21406-109">др.</span><span class="sxs-lookup"><span data-stu-id="21406-109">other</span></span>  
    <span data-ttu-id="21406-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="21406-110">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="21406-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="21406-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="21406-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21406-112">Return value</span></span>

<span data-ttu-id="21406-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="21406-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="21406-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="21406-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="21406-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="21406-115">Implements</span></span>

[<span data-ttu-id="21406-116">Иконтентекуатабле \<T\> . Контентекуалс (T)</span><span class="sxs-lookup"><span data-stu-id="21406-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="21406-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21406-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21406-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="21406-118">Reference</span></span>

[<span data-ttu-id="21406-119">Класс JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="21406-119">JET_RECPOS class</span></span>](./jet-recpos-class.md)

[<span data-ttu-id="21406-120">Элементы JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="21406-120">JET_RECPOS members</span></span>](./jet-recpos-members.md)

[<span data-ttu-id="21406-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="21406-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
