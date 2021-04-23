---
title: Синтаксис String (обобщенное время)
description: Формат строки времени, определенный стандартом ASN. 1. | Синтаксис String (обобщенное время)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Схема AD синтаксиса String (обобщенное время)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273465"
---
# <a name="stringgeneralized-time-syntax"></a><span data-ttu-id="dd05a-105">Синтаксис String (обобщенное время)</span><span class="sxs-lookup"><span data-stu-id="dd05a-105">String(Generalized-Time) syntax</span></span>

<span data-ttu-id="dd05a-106">Формат строки времени, определенный стандартом ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="dd05a-106">A time string format defined by ASN.1 standards.</span></span> <span data-ttu-id="dd05a-107">Используйте этот синтаксис для хранения значений времени в Generalized-Time формате.</span><span class="sxs-lookup"><span data-stu-id="dd05a-107">Use this syntax for storing time values in Generalized-Time format.</span></span>

<span data-ttu-id="dd05a-108">Формат синтаксиса Generalized-Time — "YYYYMMDDHHMMSS. 0Z".</span><span class="sxs-lookup"><span data-stu-id="dd05a-108">The format for the Generalized-Time syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="dd05a-109">Примером допустимого значения является "20010928060000.0 Z".</span><span class="sxs-lookup"><span data-stu-id="dd05a-109">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="dd05a-110">"Z" обозначает отсутствие разностного времени.</span><span class="sxs-lookup"><span data-stu-id="dd05a-110">The "Z" indicates no time differential.</span></span> <span data-ttu-id="dd05a-111">Active Directory сохраняет дату и время как среднее время по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="dd05a-111">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="dd05a-112">Если значение времени не указано, по умолчанию используется значение GMT.</span><span class="sxs-lookup"><span data-stu-id="dd05a-112">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="dd05a-113">Если время указано в часовом поясе, отличном от GMT, то разностное соединение между часовым поясом и GMT добавляется к строке вместо «Z» в формате «YYYYMMDDHHMMSS. 0 \[ +/- \] ЧЧММ».</span><span class="sxs-lookup"><span data-stu-id="dd05a-113">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="dd05a-114">Пример допустимого значения: "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="dd05a-114">An example of an acceptable value is "20010928060000.0+0200".</span></span> <span data-ttu-id="dd05a-115">Разностное резервное копирование основано на формуле: GMT = Local + DIFFERENTIAL.</span><span class="sxs-lookup"><span data-stu-id="dd05a-115">The differential is based on the formula: GMT=Local+differential.</span></span>

<span data-ttu-id="dd05a-116">Дополнительные сведения см. в разделе ISO 8601 и X680.</span><span class="sxs-lookup"><span data-stu-id="dd05a-116">For more information, see ISO 8601 and X680.</span></span>



| <span data-ttu-id="dd05a-117">Ввод</span><span class="sxs-lookup"><span data-stu-id="dd05a-117">Entry</span></span> | <span data-ttu-id="dd05a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dd05a-118">Value</span></span> |
|--------------|----------------------------------------------------------------------------|
| <span data-ttu-id="dd05a-119">Имя</span><span class="sxs-lookup"><span data-stu-id="dd05a-119">Name</span></span>         | <span data-ttu-id="dd05a-120">String(обобщенное_время)</span><span class="sxs-lookup"><span data-stu-id="dd05a-120">String(Generalized-Time)</span></span>                                                   |
| <span data-ttu-id="dd05a-121">Идентификатор синтаксиса</span><span class="sxs-lookup"><span data-stu-id="dd05a-121">Syntax ID</span></span>    | <span data-ttu-id="dd05a-122">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="dd05a-122">2.5.5.11</span></span>                                                                   |
| <span data-ttu-id="dd05a-123">ИДЕНТИФИКАТОР OM</span><span class="sxs-lookup"><span data-stu-id="dd05a-123">OM ID</span></span>        | <span data-ttu-id="dd05a-124">24</span><span class="sxs-lookup"><span data-stu-id="dd05a-124">24</span></span>                                                                         |
| <span data-ttu-id="dd05a-125">Тип MAPI</span><span class="sxs-lookup"><span data-stu-id="dd05a-125">MAPI Type</span></span>    | <span data-ttu-id="dd05a-126">систиме</span><span class="sxs-lookup"><span data-stu-id="dd05a-126">SYSTIME</span></span>                                                                    |
| <span data-ttu-id="dd05a-127">Тип ADS</span><span class="sxs-lookup"><span data-stu-id="dd05a-127">ADS Type</span></span>     | <span data-ttu-id="dd05a-128">АДСТИПЕ \_ время в формате UTC \_</span><span class="sxs-lookup"><span data-stu-id="dd05a-128">ADSTYPE\_UTC\_TIME</span></span>                                                         |
| <span data-ttu-id="dd05a-129">Тип варианта</span><span class="sxs-lookup"><span data-stu-id="dd05a-129">Variant Type</span></span> | <span data-ttu-id="dd05a-130">\_Дата VT</span><span class="sxs-lookup"><span data-stu-id="dd05a-130">VT\_DATE</span></span>                                                                   |
| <span data-ttu-id="dd05a-131">Тип SDS</span><span class="sxs-lookup"><span data-stu-id="dd05a-131">SDS Type</span></span>     | [<span data-ttu-id="dd05a-132">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="dd05a-132">System.DateTime</span></span>](/dotnet/api/system.datetime) |



## <a name="see-also"></a><span data-ttu-id="dd05a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd05a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd05a-134">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="dd05a-134">System.DateTime</span></span>](/dotnet/api/system.datetime)
</dt> </dl>

 

 
