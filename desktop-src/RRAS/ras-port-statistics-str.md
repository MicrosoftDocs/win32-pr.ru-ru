---
title: Структура RAS_PORT_STATISTICS (Рассапи. h)
description: '\_ \_ Структура статистики порта RAS сообщает о статистике, которую сервер RAS собирает для подключенного порта.'
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS структуры RAS_PORT_STATISTICS
- RAS — указатель структуры PRAS_PORT_STATISTICS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672679"
---
# <a name="ras_port_statistics-structure"></a><span data-ttu-id="3836c-105">\_ \_ Структура статистики порта RAS</span><span class="sxs-lookup"><span data-stu-id="3836c-105">RAS\_PORT\_STATISTICS structure</span></span>

<span data-ttu-id="3836c-106">\[Структура **\_ \_ статистики порта RAS** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="3836c-106">\[The **RAS\_PORT\_STATISTICS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="3836c-107">Структура **\_ \_ статистики порта RAS** сообщает о статистике, которую сервер RAS собирает для подключенного порта.</span><span class="sxs-lookup"><span data-stu-id="3836c-107">The **RAS\_PORT\_STATISTICS** structure reports the statistics that a RAS server collects for a connected port.</span></span> <span data-ttu-id="3836c-108">Сервер RAS сбрасывает различные статистические счетчики каждый раз при подключении порта.</span><span class="sxs-lookup"><span data-stu-id="3836c-108">The RAS server resets the various statistic counters each time the port is connected.</span></span> <span data-ttu-id="3836c-109">Вызовите функцию [**расадминпортклеарстатистикс**](rasadminportclearstatistics.md) , чтобы принудительно сбросить счетчики статистики на сервере удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="3836c-109">Call the [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) function to force the RAS server to reset the statistic counters.</span></span>

<span data-ttu-id="3836c-110">Для порта, который является частью многоканального соединения, эта структура предоставляет два набора статистических данных.</span><span class="sxs-lookup"><span data-stu-id="3836c-110">For a port that is part of a multilink connection, this structure provides two sets of statistics.</span></span> <span data-ttu-id="3836c-111">Первый набор содержит совокупную статистику по всем портам в соединении.</span><span class="sxs-lookup"><span data-stu-id="3836c-111">The first set contains the cumulative statistics for all ports in the connection.</span></span> <span data-ttu-id="3836c-112">Эти статистические данные одинаковы для всех портов в соединении.</span><span class="sxs-lookup"><span data-stu-id="3836c-112">These statistics are the same for all ports in the connection.</span></span> <span data-ttu-id="3836c-113">Второй набор содержит статистику только для этого порта.</span><span class="sxs-lookup"><span data-stu-id="3836c-113">The second set contains the statistics for just this port.</span></span> <span data-ttu-id="3836c-114">Если порт не является частью многоканального подключения, то оба набора статистических данных имеют одинаковую информацию.</span><span class="sxs-lookup"><span data-stu-id="3836c-114">If the port is not part of a multilink connection, both sets of statistics have the same information.</span></span> <span data-ttu-id="3836c-115">Чтобы определить, является ли порт частью многоканального подключения, проверьте \_ бит МНОГОканальный порт в элементе **flags** порта [**RAS порта \_ \_ 0**](ras-port-0-str.md) .</span><span class="sxs-lookup"><span data-stu-id="3836c-115">To determine whether a port is part of a multilink connection, check the PORT\_MULTILINKED bit in the **Flags** member of the port's [**RAS\_PORT\_0**](ras-port-0-str.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3836c-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3836c-116">Syntax</span></span>


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a><span data-ttu-id="3836c-117">Члены</span><span class="sxs-lookup"><span data-stu-id="3836c-117">Members</span></span>

<dl> <dt>

<span data-ttu-id="3836c-118">**двбитесксмитед**</span><span class="sxs-lookup"><span data-stu-id="3836c-118">**dwBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-119">Указывает общее число байтов, переданных соединением.</span><span class="sxs-lookup"><span data-stu-id="3836c-119">Specifies the total number of bytes transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-120">**двбитесрквед**</span><span class="sxs-lookup"><span data-stu-id="3836c-120">**dwBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-121">Указывает общее число байтов, полученных соединением.</span><span class="sxs-lookup"><span data-stu-id="3836c-121">Specifies the total number of bytes received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-122">**двфрамесксмитед**</span><span class="sxs-lookup"><span data-stu-id="3836c-122">**dwFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-123">Указывает общее число кадров, переданных соединением.</span><span class="sxs-lookup"><span data-stu-id="3836c-123">Specifies the total number of frames transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-124">**двфрамесрквед**</span><span class="sxs-lookup"><span data-stu-id="3836c-124">**dwFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-125">Указывает общее число кадров, полученных соединением.</span><span class="sxs-lookup"><span data-stu-id="3836c-125">Specifies the total number of frames received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-126">**двкрцерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-126">**dwCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-127">Указывает общее число ошибок CRC в соединении.</span><span class="sxs-lookup"><span data-stu-id="3836c-127">Specifies the total number of CRC errors on the connection.</span></span> <span data-ttu-id="3836c-128">Ошибки CRC вызваны сбоем циклической проверки избыточности.</span><span class="sxs-lookup"><span data-stu-id="3836c-128">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="3836c-129">Ошибка CRC означает, что один или несколько символов в полученном пакете данных были обнаружены неискаженными по прибытии.</span><span class="sxs-lookup"><span data-stu-id="3836c-129">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-130">**двтимеаутерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-130">**dwTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-131">Указывает общее число ошибок истечения времени ожидания в соединении.</span><span class="sxs-lookup"><span data-stu-id="3836c-131">Specifies the total number of time-out errors on the connection.</span></span> <span data-ttu-id="3836c-132">Ошибки времени ожидания возникают, когда ожидаемый символ не получен вовремя.</span><span class="sxs-lookup"><span data-stu-id="3836c-132">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="3836c-133">В этом случае программное обеспечение предполагает, что данные были потеряны и запрашивают повторную отправку.</span><span class="sxs-lookup"><span data-stu-id="3836c-133">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-134">**двалигнментерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-134">**dwAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-135">Указывает общее число ошибок выравнивания в соединении.</span><span class="sxs-lookup"><span data-stu-id="3836c-135">Specifies the total number of alignment errors on the connection.</span></span> <span data-ttu-id="3836c-136">Ошибки выравнивания возникают, если полученный символ не является ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="3836c-136">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="3836c-137">Обычно это происходит при потере символа или при возникновении ошибки истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="3836c-137">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-138">**двхардвареоверрунерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-138">**dwHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-139">Указывает общее число ошибок аппаратного переполнения в соединении.</span><span class="sxs-lookup"><span data-stu-id="3836c-139">Specifies the total number of hardware overrun errors on the connection.</span></span> <span data-ttu-id="3836c-140">Эти ошибки указывают, сколько раз отправляющий компьютер передавал символы быстрее, чем принимающее компьютерное оборудование может их обработать.</span><span class="sxs-lookup"><span data-stu-id="3836c-140">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="3836c-141">Если проблема сохраняется, уменьшите скорость соединения бит/с на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3836c-141">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-142">**двфраминжерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-142">**dwFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-143">Указывает общее число ошибок кадрирования в соединении.</span><span class="sxs-lookup"><span data-stu-id="3836c-143">Specifies the total number of framing errors on the connection.</span></span> <span data-ttu-id="3836c-144">Ошибка кадрирования возникает при получении асинхронного символа с недопустимым битом начала или окончания.</span><span class="sxs-lookup"><span data-stu-id="3836c-144">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-145">**двбуффероверрунерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-145">**dwBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-146">Указывает общее число ошибок переполнения буфера для соединения.</span><span class="sxs-lookup"><span data-stu-id="3836c-146">Specifies the total number of buffer overrun errors on the connection.</span></span> <span data-ttu-id="3836c-147">Ошибка переполнения буфера возникает, когда отправляющий компьютер передает символы быстрее, чем принимающий компьютер может их разместить.</span><span class="sxs-lookup"><span data-stu-id="3836c-147">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="3836c-148">Если проблема сохраняется, уменьшите скорость соединения бит/с на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3836c-148">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-149">**двбитесксмитедункомпрессед**</span><span class="sxs-lookup"><span data-stu-id="3836c-149">**dwBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-150">Указывает общее число байтов, переданных несжатым соединением.</span><span class="sxs-lookup"><span data-stu-id="3836c-150">Specifies the total number of bytes transmitted uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-151">**двбитесркведункомпрессед**</span><span class="sxs-lookup"><span data-stu-id="3836c-151">**dwBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-152">Указывает общее число байтов, полученных соединением без сжатия.</span><span class="sxs-lookup"><span data-stu-id="3836c-152">Specifies the total number of bytes received uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-153">**двбитесксмитедкомпрессед**</span><span class="sxs-lookup"><span data-stu-id="3836c-153">**dwBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-154">Указывает общее число байтов, переданных в сжатом соединении.</span><span class="sxs-lookup"><span data-stu-id="3836c-154">Specifies the total number of bytes transmitted compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-155">**двбитесркведкомпрессед**</span><span class="sxs-lookup"><span data-stu-id="3836c-155">**dwBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-156">Указывает общее число байтов, принятых в сжатом соединении.</span><span class="sxs-lookup"><span data-stu-id="3836c-156">Specifies the total number of bytes received compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-157">**двпортбитесксмитед**</span><span class="sxs-lookup"><span data-stu-id="3836c-157">**dwPortBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-158">Указывает общее число байтов, переданных портом.</span><span class="sxs-lookup"><span data-stu-id="3836c-158">Specifies the total number of bytes transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-159">**двпортбитесрквед**</span><span class="sxs-lookup"><span data-stu-id="3836c-159">**dwPortBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-160">Указывает общее число байтов, полученных портом.</span><span class="sxs-lookup"><span data-stu-id="3836c-160">Specifies the total number of bytes received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-161">**двпортфрамесксмитед**</span><span class="sxs-lookup"><span data-stu-id="3836c-161">**dwPortFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-162">Указывает общее число кадров, переданных портом.</span><span class="sxs-lookup"><span data-stu-id="3836c-162">Specifies the total number of frames transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-163">**двпортфрамесрквед**</span><span class="sxs-lookup"><span data-stu-id="3836c-163">**dwPortFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-164">Указывает общее число кадров, полученных портом.</span><span class="sxs-lookup"><span data-stu-id="3836c-164">Specifies the total number of frames received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-165">**двпорткрцерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-165">**dwPortCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-166">Указывает общее число ошибок CRC в порте.</span><span class="sxs-lookup"><span data-stu-id="3836c-166">Specifies the total number of CRC errors on the port.</span></span> <span data-ttu-id="3836c-167">Ошибки CRC вызваны сбоем циклической проверки избыточности.</span><span class="sxs-lookup"><span data-stu-id="3836c-167">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="3836c-168">Ошибка CRC означает, что один или несколько символов в полученном пакете данных были обнаружены неискаженными по прибытии.</span><span class="sxs-lookup"><span data-stu-id="3836c-168">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-169">**двпорттимеаутерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-169">**dwPortTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-170">Указывает общее число ошибок истечения времени ожидания в порте.</span><span class="sxs-lookup"><span data-stu-id="3836c-170">Specifies the total number of time-out errors on the port.</span></span> <span data-ttu-id="3836c-171">Ошибки времени ожидания возникают, когда ожидаемый символ не получен вовремя.</span><span class="sxs-lookup"><span data-stu-id="3836c-171">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="3836c-172">В этом случае программное обеспечение предполагает, что данные были потеряны и запрашивают повторную отправку.</span><span class="sxs-lookup"><span data-stu-id="3836c-172">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-173">**двпорталигнментерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-173">**dwPortAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-174">Указывает общее количество ошибок выравнивания на порту.</span><span class="sxs-lookup"><span data-stu-id="3836c-174">Specifies the total number of alignment errors on the port.</span></span> <span data-ttu-id="3836c-175">Ошибки выравнивания возникают, если полученный символ не является ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="3836c-175">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="3836c-176">Обычно это происходит при потере символа или при возникновении ошибки истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="3836c-176">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-177">**двпорсардвареоверрунерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-177">**dwPortHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-178">Указывает общее число ошибок аппаратного переполнения для порта.</span><span class="sxs-lookup"><span data-stu-id="3836c-178">Specifies the total number of hardware overrun errors on the port.</span></span> <span data-ttu-id="3836c-179">Эти ошибки указывают, сколько раз отправляющий компьютер передавал символы быстрее, чем принимающее компьютерное оборудование может их обработать.</span><span class="sxs-lookup"><span data-stu-id="3836c-179">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="3836c-180">Если проблема сохраняется, уменьшите скорость соединения бит/с на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3836c-180">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-181">**двпортфраминжерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-181">**dwPortFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-182">Указывает общее число ошибок кадрирования в порте.</span><span class="sxs-lookup"><span data-stu-id="3836c-182">Specifies the total number of framing errors on the port.</span></span> <span data-ttu-id="3836c-183">Ошибка кадрирования возникает при получении асинхронного символа с недопустимым битом начала или окончания.</span><span class="sxs-lookup"><span data-stu-id="3836c-183">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-184">**двпортбуффероверрунерр**</span><span class="sxs-lookup"><span data-stu-id="3836c-184">**dwPortBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-185">Указывает общее число ошибок переполнения буфера для порта.</span><span class="sxs-lookup"><span data-stu-id="3836c-185">Specifies the total number of buffer overrun errors on the port.</span></span> <span data-ttu-id="3836c-186">Ошибка переполнения буфера возникает, когда отправляющий компьютер передает символы быстрее, чем принимающий компьютер может их разместить.</span><span class="sxs-lookup"><span data-stu-id="3836c-186">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="3836c-187">Если проблема сохраняется, уменьшите скорость соединения бит/с на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3836c-187">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-188">**двпортбитесксмитедункомпрессед**</span><span class="sxs-lookup"><span data-stu-id="3836c-188">**dwPortBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-189">Указывает общее число байтов, переданных несжатым портом.</span><span class="sxs-lookup"><span data-stu-id="3836c-189">Specifies the total number of bytes transmitted uncompressed by the port.</span></span> <span data-ttu-id="3836c-190">Если порт является частью многоканального соединения, этот член является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="3836c-190">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="3836c-191">Вместо этого используйте статистику сжатия для соединения.</span><span class="sxs-lookup"><span data-stu-id="3836c-191">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-192">**двпортбитесркведункомпрессед**</span><span class="sxs-lookup"><span data-stu-id="3836c-192">**dwPortBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-193">Указывает общее число байтов, полученных портом без сжатия.</span><span class="sxs-lookup"><span data-stu-id="3836c-193">Specifies the total number of bytes received uncompressed by the port.</span></span> <span data-ttu-id="3836c-194">Если порт является частью многоканального соединения, этот член является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="3836c-194">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="3836c-195">Вместо этого используйте статистику сжатия для соединения.</span><span class="sxs-lookup"><span data-stu-id="3836c-195">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-196">**двпортбитесксмитедкомпрессед**</span><span class="sxs-lookup"><span data-stu-id="3836c-196">**dwPortBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-197">Указывает общее число байтов, переданных в сжатом порте.</span><span class="sxs-lookup"><span data-stu-id="3836c-197">Specifies the total number of bytes transmitted compressed by the port.</span></span> <span data-ttu-id="3836c-198">Если порт является частью многоканального соединения, этот член является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="3836c-198">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="3836c-199">Вместо этого используйте статистику сжатия для соединения.</span><span class="sxs-lookup"><span data-stu-id="3836c-199">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="3836c-200">**двпортбитесркведкомпрессед**</span><span class="sxs-lookup"><span data-stu-id="3836c-200">**dwPortBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="3836c-201">Указывает общее число байтов, полученных портом в сжатом виде.</span><span class="sxs-lookup"><span data-stu-id="3836c-201">Specifies the total number of bytes received compressed by the port.</span></span> <span data-ttu-id="3836c-202">Если порт является частью многоканального соединения, этот член является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="3836c-202">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="3836c-203">Вместо этого используйте статистику сжатия для соединения.</span><span class="sxs-lookup"><span data-stu-id="3836c-203">Use the compression statistics for the connection instead.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3836c-204">Требования</span><span class="sxs-lookup"><span data-stu-id="3836c-204">Requirements</span></span>



| <span data-ttu-id="3836c-205">Требование</span><span class="sxs-lookup"><span data-stu-id="3836c-205">Requirement</span></span> | <span data-ttu-id="3836c-206">Значение</span><span class="sxs-lookup"><span data-stu-id="3836c-206">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3836c-207">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3836c-207">Minimum supported client</span></span><br/> | <span data-ttu-id="3836c-208">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3836c-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3836c-209">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3836c-209">Minimum supported server</span></span><br/> | <span data-ttu-id="3836c-210">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3836c-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3836c-211">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3836c-211">End of client support</span></span><br/>    | <span data-ttu-id="3836c-212">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3836c-212">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="3836c-213">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="3836c-213">End of server support</span></span><br/>    | <span data-ttu-id="3836c-214">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3836c-214">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="3836c-215">Header</span><span class="sxs-lookup"><span data-stu-id="3836c-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="3836c-216"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3836c-216"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3836c-217">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3836c-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3836c-218">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="3836c-218">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="3836c-219">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="3836c-219">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="3836c-220">**\_Порт RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="3836c-220">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="3836c-221">**расадминакцептневконнектион**</span><span class="sxs-lookup"><span data-stu-id="3836c-221">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="3836c-222">**расадминконнектионхангупнотификатион**</span><span class="sxs-lookup"><span data-stu-id="3836c-222">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="3836c-223">**расадминпортклеарстатистикс**</span><span class="sxs-lookup"><span data-stu-id="3836c-223">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)
</dt> <dt>

[<span data-ttu-id="3836c-224">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="3836c-224">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





