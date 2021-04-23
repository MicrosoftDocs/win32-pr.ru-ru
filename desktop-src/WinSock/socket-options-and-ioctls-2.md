---
description: Некоторые параметры сокетов для сокетов Windows Sockets 2 приведены в следующей таблице.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Параметры сокета и IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712536"
---
# <a name="socket-options-and-ioctls"></a><span data-ttu-id="5725e-103">Параметры сокета и IOCTL</span><span class="sxs-lookup"><span data-stu-id="5725e-103">Socket Options and IOCTLs</span></span>

<span data-ttu-id="5725e-104">Некоторые параметры сокетов для сокетов Windows Sockets 2 приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5725e-104">Some of the socket options for Windows Sockets 2 are summarized in the following table.</span></span> <span data-ttu-id="5725e-105">Более подробные сведения приведены в разделе 4 раздела [**вспжетсоккопт**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) and/or [**вспсетсоккопт**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5725e-105">More detailed information is provided in section 4 under [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) and/or [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span></span> <span data-ttu-id="5725e-106">Существуют другие новые параметры сокета, относящиеся к протоколу, которые можно найти в Protocol-Specific приложении.</span><span class="sxs-lookup"><span data-stu-id="5725e-106">There are other new protocol-specific socket options which can be found in the Protocol-Specific Annex.</span></span> <span data-ttu-id="5725e-107">Полный список [**параметров сокета**](socket-options.md) для сокетов Windows можно найти в справочнике по Winsock.</span><span class="sxs-lookup"><span data-stu-id="5725e-107">A complete list of [**Socket Options**](socket-options.md) for Windows Sockets are available in the Winsock reference.</span></span>

<span data-ttu-id="5725e-108">Общие сведения о некоторых параметрах WinSock ioctl см. в разделе [Общие сведения о коде операций сокета ioctl](summary-of-socket-ioctl-opcodes-2.md).</span><span class="sxs-lookup"><span data-stu-id="5725e-108">For a a summary of some of the Winsock Ioctls, see [Summary of Socket Ioctl Opcodes](summary-of-socket-ioctl-opcodes-2.md).</span></span> <span data-ttu-id="5725e-109">Полный список [**Winsock ioctl**](winsock-ioctls.md) можно найти в справочнике по Winsock.</span><span class="sxs-lookup"><span data-stu-id="5725e-109">A complete list of [**Winsock IOCTLs**](winsock-ioctls.md) are available in the Winsock reference.</span></span>

## <a name="summary-of-common-socket-options"></a><span data-ttu-id="5725e-110">Сводка общих параметров сокета</span><span class="sxs-lookup"><span data-stu-id="5725e-110">Summary of Common Socket Options</span></span>

<span data-ttu-id="5725e-111">Поставщик службы Winsock должен распознать все эти параметры, а (для [**вспжетсоккопт**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) возвращать значения правдоподобные для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="5725e-111">A Winsock service provider must recognize all of these options, and (for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) return plausible values for each.</span></span> <span data-ttu-id="5725e-112">Значение по умолчанию для каждого параметра показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5725e-112">The default value for each option is shown in the following table.</span></span>

<span data-ttu-id="5725e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5725e-113">Value</span></span>

<span data-ttu-id="5725e-114">Тип</span><span class="sxs-lookup"><span data-stu-id="5725e-114">Type</span></span>

<span data-ttu-id="5725e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5725e-115">Meaning</span></span>

<span data-ttu-id="5725e-116">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5725e-116">Default</span></span>

<span data-ttu-id="5725e-117">Примечание</span><span class="sxs-lookup"><span data-stu-id="5725e-117">Note</span></span>

<span data-ttu-id="5725e-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>Итак, \_ акцептконн</span><span class="sxs-lookup"><span data-stu-id="5725e-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>SO\_ACCEPTCONN</span></span>

<span data-ttu-id="5725e-119">BOOL</span><span class="sxs-lookup"><span data-stu-id="5725e-119">BOOL</span></span>

<span data-ttu-id="5725e-120">Сокет прослушивается.</span><span class="sxs-lookup"><span data-stu-id="5725e-120">Socket is listening.</span></span>

<span data-ttu-id="5725e-121">Значение FALSE, если не выполнено [**всплистен**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5725e-121">FALSE unless a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) has been performed.</span></span>

<span data-ttu-id="5725e-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_вещание</span><span class="sxs-lookup"><span data-stu-id="5725e-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>SO\_BROADCAST</span></span>

<span data-ttu-id="5725e-123">BOOL</span><span class="sxs-lookup"><span data-stu-id="5725e-123">BOOL</span></span>

<span data-ttu-id="5725e-124">Сокет настроен для передачи и получения широковещательных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5725e-124">Socket is configured for the transmission and receipt of broadcast messages.</span></span>

<span data-ttu-id="5725e-125">FALSE</span><span class="sxs-lookup"><span data-stu-id="5725e-125">FALSE</span></span>

<span data-ttu-id="5725e-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>Итак, \_ Отладка</span><span class="sxs-lookup"><span data-stu-id="5725e-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>SO\_DEBUG</span></span>

<span data-ttu-id="5725e-127">BOOL</span><span class="sxs-lookup"><span data-stu-id="5725e-127">BOOL</span></span>

<span data-ttu-id="5725e-128">Отладка включена.</span><span class="sxs-lookup"><span data-stu-id="5725e-128">Debugging is enabled.</span></span>

<span data-ttu-id="5725e-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="5725e-129">FALSE</span></span>

<span data-ttu-id="5725e-130">сохранении</span><span class="sxs-lookup"><span data-stu-id="5725e-130">(i)</span></span>

<span data-ttu-id="5725e-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>Итак, \_ донтлинжер</span><span class="sxs-lookup"><span data-stu-id="5725e-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>SO\_DONTLINGER</span></span>

<span data-ttu-id="5725e-132">BOOL</span><span class="sxs-lookup"><span data-stu-id="5725e-132">BOOL</span></span>

<span data-ttu-id="5725e-133">Если задано значение true, \_ параметр so-on отключен.</span><span class="sxs-lookup"><span data-stu-id="5725e-133">If true, the SO\_LINGER option is disabled.</span></span>

<span data-ttu-id="5725e-134">true</span><span class="sxs-lookup"><span data-stu-id="5725e-134">TRUE</span></span>

<span data-ttu-id="5725e-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>Итак, \_ донтрауте</span><span class="sxs-lookup"><span data-stu-id="5725e-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>SO\_DONTROUTE</span></span>

<span data-ttu-id="5725e-136">BOOL</span><span class="sxs-lookup"><span data-stu-id="5725e-136">BOOL</span></span>

<span data-ttu-id="5725e-137">Маршрутизация отключена.</span><span class="sxs-lookup"><span data-stu-id="5725e-137">Routing is disabled.</span></span> <span data-ttu-id="5725e-138">Выполняется успешно, но пропускается на \_ сокетах AF inet; сбой в \_ сокетах INET6 с [всаенопротупт](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="5725e-138">Succeeds but is ignored on AF\_INET sockets; fails on AF\_INET6 sockets with [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="5725e-139">Не поддерживается на сокетах ATM (приводит к ошибке).</span><span class="sxs-lookup"><span data-stu-id="5725e-139">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="5725e-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="5725e-140">FALSE</span></span>

<span data-ttu-id="5725e-141">сохранении</span><span class="sxs-lookup"><span data-stu-id="5725e-141">(i)</span></span>

<span data-ttu-id="5725e-142"><span id="SO_ERROR"></span><span id="so_error"></span>\_Ошибка</span><span class="sxs-lookup"><span data-stu-id="5725e-142"><span id="SO_ERROR"></span><span id="so_error"></span>SO\_ERROR</span></span>

<span data-ttu-id="5725e-143">INT</span><span class="sxs-lookup"><span data-stu-id="5725e-143">int</span></span>

<span data-ttu-id="5725e-144">Извлекает состояние ошибки и очищается.</span><span class="sxs-lookup"><span data-stu-id="5725e-144">Retrieves error status and clear.</span></span>

<span data-ttu-id="5725e-145">0</span><span class="sxs-lookup"><span data-stu-id="5725e-145">0</span></span>

<span data-ttu-id="5725e-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>так \_ что \_ идентификатор группы</span><span class="sxs-lookup"><span data-stu-id="5725e-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>SO\_GROUP\_ID</span></span>

<span data-ttu-id="5725e-147">GROUP</span><span class="sxs-lookup"><span data-stu-id="5725e-147">GROUP</span></span>

<span data-ttu-id="5725e-148">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="5725e-148">Reserved.</span></span>

<span data-ttu-id="5725e-149">NULL</span><span class="sxs-lookup"><span data-stu-id="5725e-149">NULL</span></span>

<span data-ttu-id="5725e-150">Только получение</span><span class="sxs-lookup"><span data-stu-id="5725e-150">Get only</span></span>

<span data-ttu-id="5725e-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>Итак \_ , \_ приоритет группы</span><span class="sxs-lookup"><span data-stu-id="5725e-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO\_GROUP\_PRIORITY</span></span>

<span data-ttu-id="5725e-152">INT</span><span class="sxs-lookup"><span data-stu-id="5725e-152">int</span></span>

<span data-ttu-id="5725e-153">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="5725e-153">Reserved.</span></span>

<span data-ttu-id="5725e-154">0</span><span class="sxs-lookup"><span data-stu-id="5725e-154">0</span></span>

[<span data-ttu-id="5725e-155">**Итак, \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="5725e-155">**SO\_KEEPALIVE**</span></span>](so-keepalive.md)

<span data-ttu-id="5725e-156">BOOL</span><span class="sxs-lookup"><span data-stu-id="5725e-156">BOOL</span></span>

<span data-ttu-id="5725e-157">Проверку активности отправляются.</span><span class="sxs-lookup"><span data-stu-id="5725e-157">Keepalives are being sent.</span></span> <span data-ttu-id="5725e-158">Не поддерживается на сокетах ATM (приводит к ошибке).</span><span class="sxs-lookup"><span data-stu-id="5725e-158">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="5725e-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="5725e-159">FALSE</span></span>

<span data-ttu-id="5725e-160">сохранении</span><span class="sxs-lookup"><span data-stu-id="5725e-160">(i)</span></span>

<span data-ttu-id="5725e-161"><span id="SO_LINGER"></span><span id="so_linger"></span>т. д. \_</span><span class="sxs-lookup"><span data-stu-id="5725e-161"><span id="SO_LINGER"></span><span id="so_linger"></span>SO\_LINGER</span></span>

<span data-ttu-id="5725e-162">Структура — ожидание</span><span class="sxs-lookup"><span data-stu-id="5725e-162">Structure linger</span></span>

<span data-ttu-id="5725e-163">Возвращает текущие параметры "ожидание".</span><span class="sxs-lookup"><span data-stu-id="5725e-163">Returns the current linger options.</span></span>

<span data-ttu-id="5725e-164">l \_ онофф равен 0</span><span class="sxs-lookup"><span data-stu-id="5725e-164">l\_onoff is 0</span></span>

<span data-ttu-id="5725e-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_максимальный \_ размер сообщения \_</span><span class="sxs-lookup"><span data-stu-id="5725e-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>SO\_MAX\_MSG\_SIZE</span></span>

<span data-ttu-id="5725e-166">INT</span><span class="sxs-lookup"><span data-stu-id="5725e-166">int</span></span>

<span data-ttu-id="5725e-167">Максимальный исходящий размер сообщения для типов сокетов сообщений.</span><span class="sxs-lookup"><span data-stu-id="5725e-167">Maximum outbound size of a message for message socket types.</span></span> <span data-ttu-id="5725e-168">Для определения максимального размера входящего сообщения нет необходимости.</span><span class="sxs-lookup"><span data-stu-id="5725e-168">There is no provision to determine the maximum inbound message size.</span></span> <span data-ttu-id="5725e-169">Не имеет смысла для ориентированных на поток сокетов.</span><span class="sxs-lookup"><span data-stu-id="5725e-169">Has no meaning for stream-oriented sockets.</span></span>

<span data-ttu-id="5725e-170">Зависит от реализации</span><span class="sxs-lookup"><span data-stu-id="5725e-170">Implementation dependent</span></span>

<span data-ttu-id="5725e-171">Только получение</span><span class="sxs-lookup"><span data-stu-id="5725e-171">Get only</span></span>

<span data-ttu-id="5725e-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>Итак, \_ убинлине</span><span class="sxs-lookup"><span data-stu-id="5725e-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>SO\_OOBINLINE</span></span>

<span data-ttu-id="5725e-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="5725e-173">BOOL</span></span>

<span data-ttu-id="5725e-174">Данные OOB получаются в потоке обычных данных.</span><span class="sxs-lookup"><span data-stu-id="5725e-174">OOB data is being received in the normal data stream.</span></span>

<span data-ttu-id="5725e-175">FALSE</span><span class="sxs-lookup"><span data-stu-id="5725e-175">FALSE</span></span>

<span data-ttu-id="5725e-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_инфов протокола \_</span><span class="sxs-lookup"><span data-stu-id="5725e-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO\_PROTOCOL\_INFOW</span></span>

<span data-ttu-id="5725e-177">[ **\_ сведения о структуре всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span><span class="sxs-lookup"><span data-stu-id="5725e-177">structure [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span></span>

<span data-ttu-id="5725e-178">Описание протокола для протокола, привязанного к этому сокету.</span><span class="sxs-lookup"><span data-stu-id="5725e-178">Description of protocol information for the protocol that is bound to this socket.</span></span>

<span data-ttu-id="5725e-179">Зависит от протокола</span><span class="sxs-lookup"><span data-stu-id="5725e-179">Protocol dependent</span></span>

<span data-ttu-id="5725e-180">Только получение</span><span class="sxs-lookup"><span data-stu-id="5725e-180">Get only</span></span>

<span data-ttu-id="5725e-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>Итак, \_ рквбуф</span><span class="sxs-lookup"><span data-stu-id="5725e-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>SO\_RCVBUF</span></span>

<span data-ttu-id="5725e-182">INT</span><span class="sxs-lookup"><span data-stu-id="5725e-182">int</span></span>

<span data-ttu-id="5725e-183">Общее количество буферных пространств сокета, зарезервированных для получения.</span><span class="sxs-lookup"><span data-stu-id="5725e-183">The total per-socket buffer space reserved for receives.</span></span> <span data-ttu-id="5725e-184">Это не связано с \_ максимальным \_ размером сообщения \_ и не обязательно соответствует размеру окна приема TCP.</span><span class="sxs-lookup"><span data-stu-id="5725e-184">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of the TCP receive window.</span></span>

<span data-ttu-id="5725e-185">Зависит от реализации</span><span class="sxs-lookup"><span data-stu-id="5725e-185">Implementation dependent</span></span>

<span data-ttu-id="5725e-186">сохранении</span><span class="sxs-lookup"><span data-stu-id="5725e-186">(i)</span></span>

<span data-ttu-id="5725e-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>Итак, \_ реусеаддр</span><span class="sxs-lookup"><span data-stu-id="5725e-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>SO\_REUSEADDR</span></span>

<span data-ttu-id="5725e-188">BOOL</span><span class="sxs-lookup"><span data-stu-id="5725e-188">BOOL</span></span>

<span data-ttu-id="5725e-189">Адрес, к которому привязан этот сокет, может использоваться другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="5725e-189">The address to which this socket is bound can be used by others.</span></span> <span data-ttu-id="5725e-190">Неприменимо к сокетам ATM.</span><span class="sxs-lookup"><span data-stu-id="5725e-190">Not applicable on ATM sockets.</span></span>

<span data-ttu-id="5725e-191">FALSE</span><span class="sxs-lookup"><span data-stu-id="5725e-191">FALSE</span></span>

<span data-ttu-id="5725e-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>Итак, \_ сндбуф</span><span class="sxs-lookup"><span data-stu-id="5725e-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO\_SNDBUF</span></span>

<span data-ttu-id="5725e-193">INT</span><span class="sxs-lookup"><span data-stu-id="5725e-193">int</span></span>

<span data-ttu-id="5725e-194">Общее количество буферных пространств сокета, зарезервированных для отправки.</span><span class="sxs-lookup"><span data-stu-id="5725e-194">The total per-socket buffer space reserved for sends.</span></span> <span data-ttu-id="5725e-195">Это не связано с \_ максимальным \_ размером сообщения \_ и не обязательно соответствует размеру окна TCP-отправки.</span><span class="sxs-lookup"><span data-stu-id="5725e-195">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of a TCP send window.</span></span>

<span data-ttu-id="5725e-196">Зависит от реализации</span><span class="sxs-lookup"><span data-stu-id="5725e-196">Implementation dependent</span></span>

<span data-ttu-id="5725e-197">сохранении</span><span class="sxs-lookup"><span data-stu-id="5725e-197">(i)</span></span>

<span data-ttu-id="5725e-198"><span id="SO_TYPE"></span><span id="so_type"></span>Поэтому \_ тип</span><span class="sxs-lookup"><span data-stu-id="5725e-198"><span id="SO_TYPE"></span><span id="so_type"></span>SO\_TYPE</span></span>

<span data-ttu-id="5725e-199">INT</span><span class="sxs-lookup"><span data-stu-id="5725e-199">int</span></span>

<span data-ttu-id="5725e-200">Тип сокета (например, \_ поток Сокк).</span><span class="sxs-lookup"><span data-stu-id="5725e-200">The type of the socket (for example, SOCK\_STREAM).</span></span>

<span data-ttu-id="5725e-201">Как создано через сокет.</span><span class="sxs-lookup"><span data-stu-id="5725e-201">As created through socket.</span></span>

<span data-ttu-id="5725e-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>\_Конфигурация ПВД</span><span class="sxs-lookup"><span data-stu-id="5725e-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD\_CONFIG</span></span>

<span data-ttu-id="5725e-203">знак FAR \*</span><span class="sxs-lookup"><span data-stu-id="5725e-203">char FAR \*</span></span>

<span data-ttu-id="5725e-204">Объект структуры непрозрачных данных, содержащий сведения о конфигурации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="5725e-204">An opaque data structure object containing configuration information of the service provider.</span></span>

<span data-ttu-id="5725e-205">Зависит от реализации</span><span class="sxs-lookup"><span data-stu-id="5725e-205">Implementation dependent</span></span>

<span data-ttu-id="5725e-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>\_Задержка TCP</span><span class="sxs-lookup"><span data-stu-id="5725e-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP\_NODELAY</span></span>

<span data-ttu-id="5725e-207">BOOL</span><span class="sxs-lookup"><span data-stu-id="5725e-207">BOOL</span></span>

<span data-ttu-id="5725e-208">Отключить алгоритм Nagle для отправки объединенных пакетов.</span><span class="sxs-lookup"><span data-stu-id="5725e-208">Disables the Nagle algorithm for send coalescing.</span></span>

<span data-ttu-id="5725e-209">Зависит от реализации</span><span class="sxs-lookup"><span data-stu-id="5725e-209">Implementation dependent</span></span>

<span data-ttu-id="5725e-210">(i) поставщик услуг может автоматически игнорировать этот параметр в [**вспсетсоккопт**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) и вернуть значение константы для [**вспжетсоккопт**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), либо может принимать значение для **вспсетсоккопт** и возвращать соответствующее значение в **вспжетсоккопт** без использования значения каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="5725e-210">(i) A service provider may silently ignore this option on [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) and return a constant value for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), or it may accept a value for **WSPSetSockOpt** and return the corresponding value in **WSPGetSockOpt** without using the value in any way.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="5725e-211">См. также</span><span class="sxs-lookup"><span data-stu-id="5725e-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5725e-212">**Параметры сокета**</span><span class="sxs-lookup"><span data-stu-id="5725e-212">**Socket Options**</span></span>](socket-options.md)
</dt> <dt>

[<span data-ttu-id="5725e-213">**\_Параметры сокета сокета Sol**</span><span class="sxs-lookup"><span data-stu-id="5725e-213">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="5725e-214">**\_Параметры TCP-сокета иппрото**</span><span class="sxs-lookup"><span data-stu-id="5725e-214">**IPPROTO\_TCP Socket Options**</span></span>](ipproto-tcp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="5725e-215">**\_Параметры сокета UDP иппрото**</span><span class="sxs-lookup"><span data-stu-id="5725e-215">**IPPROTO\_UDP Socket Options**</span></span>](ipproto-udp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="5725e-216">**Winsock IOCTL**</span><span class="sxs-lookup"><span data-stu-id="5725e-216">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
