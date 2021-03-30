---
description: 'Дополнительные сведения о методе: reкомпареоптионсфромлкмапфлагсs.'
title: Метод преобразования. Компареоптионсфромлкмапфлагс
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263399"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a><span data-ttu-id="cd053-103">Метод преобразования. Компареоптионсфромлкмапфлагс</span><span class="sxs-lookup"><span data-stu-id="cd053-103">Conversions.CompareOptionsFromLCMapFlags method</span></span>

<span data-ttu-id="cd053-104">Заданными флагами для Лкмапфлагс, преобразуйте их в параметры сравнения.</span><span class="sxs-lookup"><span data-stu-id="cd053-104">Given flags for LCMapFlags, turn them into compare options.</span></span> <span data-ttu-id="cd053-105">Неизвестные параметры игнорируются.</span><span class="sxs-lookup"><span data-stu-id="cd053-105">Unknown options are ignored.</span></span>

<span data-ttu-id="cd053-106">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="cd053-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="cd053-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cd053-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cd053-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cd053-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cd053-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd053-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a><span data-ttu-id="cd053-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd053-110">Parameters</span></span>

  - <span data-ttu-id="cd053-111">лкмапфлагс</span><span class="sxs-lookup"><span data-stu-id="cd053-111">lcmapFlags</span></span>  
    <span data-ttu-id="cd053-112">Тип: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="cd053-112">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="cd053-113">Флаги LCMapString завершилось ошибкой.</span><span class="sxs-lookup"><span data-stu-id="cd053-113">LCMapString flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cd053-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd053-114">Return value</span></span>

<span data-ttu-id="cd053-115">Тип: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="cd053-115">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
<span data-ttu-id="cd053-116">CompareOptions, описывающий флаги (известные).</span><span class="sxs-lookup"><span data-stu-id="cd053-116">CompareOptions describing the (known) flags.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cd053-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd053-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cd053-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="cd053-118">Reference</span></span>

[<span data-ttu-id="cd053-119">Класс преобразований</span><span class="sxs-lookup"><span data-stu-id="cd053-119">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="cd053-120">Преобразования элементов</span><span class="sxs-lookup"><span data-stu-id="cd053-120">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="cd053-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cd053-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
