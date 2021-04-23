---
description: '\_Структура схемы PID содержит определение содержимого идентификатора пакета транспортного потока MPEG-2.'
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: Структура PID_MAP (Бдатипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689276"
---
# <a name="pid_map-structure"></a><span data-ttu-id="a9d06-103">\_Структура схемы PID</span><span class="sxs-lookup"><span data-stu-id="a9d06-103">PID\_MAP structure</span></span>

<span data-ttu-id="a9d06-104">`PID_MAP`Структура содержит определение содержимого идентификатора пакета транспортного потока MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="a9d06-104">The `PID_MAP` structure contains identifies the contents of an MPEG-2 transport stream packet ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d06-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9d06-105">Syntax</span></span>


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a><span data-ttu-id="a9d06-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a9d06-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9d06-107">**улпид**</span><span class="sxs-lookup"><span data-stu-id="a9d06-107">**ulPID**</span></span>
</dt> <dd>

<span data-ttu-id="a9d06-108">Указывает идентификатор пакета (PID)</span><span class="sxs-lookup"><span data-stu-id="a9d06-108">Specifies the packet ID (PID)</span></span>

</dd> <dt>

<span data-ttu-id="a9d06-109">**медиасамплеконтент**</span><span class="sxs-lookup"><span data-stu-id="a9d06-109">**MediaSampleContent**</span></span>
</dt> <dd>

<span data-ttu-id="a9d06-110">Задает содержимое полезных данных пакета в виде типа перечисления [**мультимедиа \_ образец \_ содержимого**](media-sample-content.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d06-110">Specifies the contents of the packet payload, as a [**MEDIA\_SAMPLE\_CONTENT**](media-sample-content.md) enumeration type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9d06-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a9d06-111">Requirements</span></span>



| <span data-ttu-id="a9d06-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a9d06-112">Requirement</span></span> | <span data-ttu-id="a9d06-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a9d06-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d06-114">Header</span><span class="sxs-lookup"><span data-stu-id="a9d06-114">Header</span></span><br/> | <dl> <span data-ttu-id="a9d06-115"><dt>Бдатипес. h (включение Бдаифаце. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9d06-115"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d06-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9d06-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d06-117">Структуры DirectShow</span><span class="sxs-lookup"><span data-stu-id="a9d06-117">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="a9d06-118">**Интерфейс Иенумпидмап**</span><span class="sxs-lookup"><span data-stu-id="a9d06-118">**IEnumPIDMap Interface**</span></span>](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




