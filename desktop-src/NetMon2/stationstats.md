---
description: Структура СТАТИОНСТАТС предоставляет статистику о конкретной станции, описываемой текущей записью.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: Структура СТАТИОНСТАТС (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080598"
---
# <a name="stationstats-structure"></a><span data-ttu-id="51dd2-103">Структура СТАТИОНСТАТС</span><span class="sxs-lookup"><span data-stu-id="51dd2-103">STATIONSTATS structure</span></span>

<span data-ttu-id="51dd2-104">Структура **статионстатс** предоставляет статистику о конкретной [*станции*](s.md) , описываемой текущей записью.</span><span class="sxs-lookup"><span data-stu-id="51dd2-104">The **STATIONSTATS** structure provides statistics about a specific [*station*](s.md) described by the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="51dd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51dd2-105">Syntax</span></span>


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a><span data-ttu-id="51dd2-106">Члены</span><span class="sxs-lookup"><span data-stu-id="51dd2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="51dd2-107">**некстстатионстатс**</span><span class="sxs-lookup"><span data-stu-id="51dd2-107">**NextStationStats**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-108">Индекс следующей станции, записанной в массиве структуры **статионстатс** .</span><span class="sxs-lookup"><span data-stu-id="51dd2-108">Index of the next station recorded in the **STATIONSTATS** structure array.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-109">**сессионпартнерлист**</span><span class="sxs-lookup"><span data-stu-id="51dd2-109">**SessionPartnerList**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-110">Индекс списка партнеров станции.</span><span class="sxs-lookup"><span data-stu-id="51dd2-110">Index of the station partner list.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-111">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="51dd2-111">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-112">Этот элемент устарел.</span><span class="sxs-lookup"><span data-stu-id="51dd2-112">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-113">**статионаддресс**</span><span class="sxs-lookup"><span data-stu-id="51dd2-113">**StationAddress**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-114">MAC-адрес станции.</span><span class="sxs-lookup"><span data-stu-id="51dd2-114">The MAC address of the station.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-115">**Коммутаци**</span><span class="sxs-lookup"><span data-stu-id="51dd2-115">**Pad**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-116">Выравнивание **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="51dd2-116">**DWORD** alignment.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-117">**тоталпаккетсрецеивед**</span><span class="sxs-lookup"><span data-stu-id="51dd2-117">**TotalPacketsReceived**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-118">Общее число пакетов, отправленных на станцию.</span><span class="sxs-lookup"><span data-stu-id="51dd2-118">Total number of packets sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-119">**тоталдиректедпаккетссент**</span><span class="sxs-lookup"><span data-stu-id="51dd2-119">**TotalDirectedPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-120">Общее число направленных станцией отправленных пакетов.</span><span class="sxs-lookup"><span data-stu-id="51dd2-120">Total number of directed packets sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-121">**тоталброадкастпаккетссент**</span><span class="sxs-lookup"><span data-stu-id="51dd2-121">**TotalBroadcastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-122">Общее число пакетов, направленных с помощью широковещательной рассылки (MAC-адрес FF FF FF FF FF), отправленных станцией.</span><span class="sxs-lookup"><span data-stu-id="51dd2-122">Total number of broadcast-directed packets (MAC address FF FF FF FF FF FF) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-123">**тоталмултикастпаккетссент**</span><span class="sxs-lookup"><span data-stu-id="51dd2-123">**TotalMulticastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-124">Общее число пакетов многоадресной рассылки (набор битов группы в адресе назначения), отправленных станцией.</span><span class="sxs-lookup"><span data-stu-id="51dd2-124">Total number of multicast packets (Group bit set in destination address) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-125">**TotalBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="51dd2-125">**TotalBytesReceived**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-126">Общее число байтов, отправленных на станцию.</span><span class="sxs-lookup"><span data-stu-id="51dd2-126">Total number of bytes sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="51dd2-127">**TotalBytesSent**</span><span class="sxs-lookup"><span data-stu-id="51dd2-127">**TotalBytesSent**</span></span>
</dt> <dd>

<span data-ttu-id="51dd2-128">Общее число байтов, отправленных станцией.</span><span class="sxs-lookup"><span data-stu-id="51dd2-128">Total number of bytes sent by the station.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51dd2-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51dd2-129">Remarks</span></span>

<span data-ttu-id="51dd2-130">Сетевой монитор хранит сведения о сеансах и станциях в двух связанных массивах.</span><span class="sxs-lookup"><span data-stu-id="51dd2-130">Network Monitor stores session and station information in two associated arrays.</span></span> <span data-ttu-id="51dd2-131">, элементы которого являются структурами [сессионстатс](sessionstats.md) и **статионстатс** соответственно.</span><span class="sxs-lookup"><span data-stu-id="51dd2-131">whose elements are [SESSIONSTATS](sessionstats.md) and **STATIONSTATS** structures respectively.</span></span> <span data-ttu-id="51dd2-132">Члены этих структур можно использовать для перехода между ними.</span><span class="sxs-lookup"><span data-stu-id="51dd2-132">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="51dd2-133">Например, чтобы перейти на следующую станцию, используйте **некстстатионстатс**.</span><span class="sxs-lookup"><span data-stu-id="51dd2-133">For example, to move to the next station use **NextStationStats**.</span></span> <span data-ttu-id="51dd2-134">Чтобы перейти к списку участников сеанса в массиве СЕССИОНСТАТС, используйте индекс, указанный в **сессионпартнерлист**.</span><span class="sxs-lookup"><span data-stu-id="51dd2-134">To jump to the session partner list in the SESSIONSTATS array, use the index provided in **SessionPartnerList**.</span></span>

> [!Note]  
> <span data-ttu-id="51dd2-135">Массив **статионстатс** содержит элемент для каждой станции, используемой во время текущей записи.</span><span class="sxs-lookup"><span data-stu-id="51dd2-135">The **STATIONSTATS** array contains an element for each station used during the current capture.</span></span> <span data-ttu-id="51dd2-136">Алгоритм, сетевой монитор используемый для добавления элементов в этот массив, основан на наиболее эффективном способе записи информации во время выполнения записи.</span><span class="sxs-lookup"><span data-stu-id="51dd2-136">The algorithm Network Monitor uses to add elements to this array is based on the most efficient way to record information while the capture is in progress.</span></span> <span data-ttu-id="51dd2-137">Следовательно, следующая станция не всегда является следующим элементом массива.</span><span class="sxs-lookup"><span data-stu-id="51dd2-137">Consequently, the next station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51dd2-138">Требования</span><span class="sxs-lookup"><span data-stu-id="51dd2-138">Requirements</span></span>



| <span data-ttu-id="51dd2-139">Требование</span><span class="sxs-lookup"><span data-stu-id="51dd2-139">Requirement</span></span> | <span data-ttu-id="51dd2-140">Значение</span><span class="sxs-lookup"><span data-stu-id="51dd2-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="51dd2-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51dd2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="51dd2-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51dd2-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="51dd2-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51dd2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="51dd2-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51dd2-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="51dd2-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="51dd2-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="51dd2-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="51dd2-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51dd2-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51dd2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51dd2-148">Иделайдк:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="51dd2-148">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="51dd2-149">ИРТК:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="51dd2-149">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="51dd2-150">Истатс:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="51dd2-150">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




