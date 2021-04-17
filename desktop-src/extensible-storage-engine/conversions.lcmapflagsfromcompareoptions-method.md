---
description: 'Дополнительные сведения о методе: reлкмапфлагсфромкомпареоптионсs.'
title: Метод преобразования. Лкмапфлагсфромкомпареоптионс
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711321"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a><span data-ttu-id="289f3-103">Метод преобразования. Лкмапфлагсфромкомпареоптионс</span><span class="sxs-lookup"><span data-stu-id="289f3-103">Conversions.LCMapFlagsFromCompareOptions method</span></span>

<span data-ttu-id="289f3-104">Дайте CompareOptions, преобразуйте их в флаги из LCMapString завершилось ошибкой.</span><span class="sxs-lookup"><span data-stu-id="289f3-104">Give CompareOptions, turn them into flags from LCMapString.</span></span> <span data-ttu-id="289f3-105">Неизвестные параметры игнорируются.</span><span class="sxs-lookup"><span data-stu-id="289f3-105">Unknown options are ignored.</span></span>

<span data-ttu-id="289f3-106">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="289f3-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="289f3-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="289f3-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="289f3-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="289f3-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="289f3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="289f3-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a><span data-ttu-id="289f3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="289f3-110">Parameters</span></span>

  - <span data-ttu-id="289f3-111">compareOptions</span><span class="sxs-lookup"><span data-stu-id="289f3-111">compareOptions</span></span>  
    <span data-ttu-id="289f3-112">Тип: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="289f3-112">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
    
    <span data-ttu-id="289f3-113">Преобразуемые параметры.</span><span class="sxs-lookup"><span data-stu-id="289f3-113">The options to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="289f3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="289f3-114">Return value</span></span>

<span data-ttu-id="289f3-115">Тип: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="289f3-115">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
<span data-ttu-id="289f3-116">Флаги LCMapString завершилось ошибкой, соответствующие параметрам сравнения.</span><span class="sxs-lookup"><span data-stu-id="289f3-116">The LCMapString flags that match the compare options.</span></span> <span data-ttu-id="289f3-117">Неподдерживаемые параметры игнорируются.</span><span class="sxs-lookup"><span data-stu-id="289f3-117">Unsupported options are ignored.</span></span>  

## <a name="see-also"></a><span data-ttu-id="289f3-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="289f3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="289f3-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="289f3-119">Reference</span></span>

[<span data-ttu-id="289f3-120">Класс преобразований</span><span class="sxs-lookup"><span data-stu-id="289f3-120">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="289f3-121">Преобразования элементов</span><span class="sxs-lookup"><span data-stu-id="289f3-121">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="289f3-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="289f3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
