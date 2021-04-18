---
description: 'Дополнительные сведения о: JET_CONDITIONALCOLUMN. Метод Контентекуалс'
title: JET_CONDITIONALCOLUMN. Метод Контентекуалс
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN.ContentEquals(Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103531
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd62bb5c6be4960232865de48080969c04438f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683998"
---
# <a name="jet_conditionalcolumncontentequals-method"></a><span data-ttu-id="7e335-103">JET_CONDITIONALCOLUMN. Метод Контентекуалс</span><span class="sxs-lookup"><span data-stu-id="7e335-103">JET_CONDITIONALCOLUMN.ContentEquals method</span></span>

<span data-ttu-id="7e335-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="7e335-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="7e335-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e335-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e335-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e335-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e335-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e335-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_CONDITIONALCOLUMN _
) As Boolean
'Usage
Dim instance As JET_CONDITIONALCOLUMN
Dim other As JET_CONDITIONALCOLUMN
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_CONDITIONALCOLUMN other
)
```

#### <a name="parameters"></a><span data-ttu-id="7e335-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e335-108">Parameters</span></span>

  - <span data-ttu-id="7e335-109">др.</span><span class="sxs-lookup"><span data-stu-id="7e335-109">other</span></span>  
    <span data-ttu-id="7e335-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-class.md)</span><span class="sxs-lookup"><span data-stu-id="7e335-110">Type: [Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-class.md)</span></span>  
    
    <span data-ttu-id="7e335-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="7e335-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7e335-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e335-112">Return value</span></span>

<span data-ttu-id="7e335-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7e335-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7e335-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="7e335-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="7e335-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="7e335-115">Implements</span></span>

[<span data-ttu-id="7e335-116">Иконтентекуатабле \<T\> . Контентекуалс (T)</span><span class="sxs-lookup"><span data-stu-id="7e335-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="7e335-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e335-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e335-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="7e335-118">Reference</span></span>

[<span data-ttu-id="7e335-119">Класс JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="7e335-119">JET_CONDITIONALCOLUMN class</span></span>](./jet-conditionalcolumn-class.md)

[<span data-ttu-id="7e335-120">Элементы JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="7e335-120">JET_CONDITIONALCOLUMN members</span></span>](./jet-conditionalcolumn-members.md)

[<span data-ttu-id="7e335-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7e335-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
