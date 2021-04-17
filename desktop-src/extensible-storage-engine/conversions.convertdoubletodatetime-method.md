---
description: 'Дополнительные сведения о методе: reконвертдаублетодатетимеs.'
title: Метод преобразования. Конвертдаублетодатетиме
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693374"
---
# <a name="conversionsconvertdoubletodatetime-method"></a><span data-ttu-id="e4a4a-103">Метод преобразования. Конвертдаублетодатетиме</span><span class="sxs-lookup"><span data-stu-id="e4a4a-103">Conversions.ConvertDoubleToDateTime method</span></span>

<span data-ttu-id="e4a4a-104">Преобразуйте значение типа Double (формат даты и времени OA) в тип DateTime.</span><span class="sxs-lookup"><span data-stu-id="e4a4a-104">Convert a double (OA date time format) to a DateTime.</span></span> <span data-ttu-id="e4a4a-105">В отличие от DateTime. FromOADate, это не создает исключения.</span><span class="sxs-lookup"><span data-stu-id="e4a4a-105">Unlike DateTime.FromOADate this doesn't throw exceptions.</span></span>

<span data-ttu-id="e4a4a-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4a4a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e4a4a-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e4a4a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a4a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4a4a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a><span data-ttu-id="e4a4a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4a4a-109">Parameters</span></span>

  - <span data-ttu-id="e4a4a-110">d</span><span class="sxs-lookup"><span data-stu-id="e4a4a-110">d</span></span>  
    <span data-ttu-id="e4a4a-111">Тип: [System. Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="e4a4a-111">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="e4a4a-112">Значение типа Double.</span><span class="sxs-lookup"><span data-stu-id="e4a4a-112">The double value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e4a4a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4a4a-113">Return value</span></span>

<span data-ttu-id="e4a4a-114">Тип: [System. DateTime](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="e4a4a-114">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
<span data-ttu-id="e4a4a-115">Значение типа DateTime.</span><span class="sxs-lookup"><span data-stu-id="e4a4a-115">A DateTime.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4a4a-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4a4a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4a4a-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="e4a4a-117">Reference</span></span>

[<span data-ttu-id="e4a4a-118">Класс преобразований</span><span class="sxs-lookup"><span data-stu-id="e4a4a-118">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="e4a4a-119">Преобразования элементов</span><span class="sxs-lookup"><span data-stu-id="e4a4a-119">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="e4a4a-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e4a4a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
