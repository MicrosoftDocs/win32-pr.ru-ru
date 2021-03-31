---
description: Описание кодов ошибок 1700-3999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Коды системных ошибок (1700-3999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895441"
---
# <a name="system-error-codes-1700-3999"></a><span data-ttu-id="5eb82-103">Коды системных ошибок (1700-3999)</span><span class="sxs-lookup"><span data-stu-id="5eb82-103">System Error Codes (1700-3999)</span></span>

> [!NOTE]
> <span data-ttu-id="5eb82-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="5eb82-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="5eb82-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="5eb82-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 1700 – 3999.</span><span class="sxs-lookup"><span data-stu-id="5eb82-106">The following list describes [system error codes](system-error-codes.md) for errors 1700 to 3999.</span></span> <span data-ttu-id="5eb82-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="5eb82-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="5eb82-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="5eb82-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="5eb82-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**\_ \_ Недопустимая \_ Привязка строк RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC\_S\_INVALID\_STRING\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-110">1700 (0x6A4)</span><span class="sxs-lookup"><span data-stu-id="5eb82-110">1700 (0x6A4)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-111">Недопустимая строка привязки.</span><span class="sxs-lookup"><span data-stu-id="5eb82-111">The string binding is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**\_ \_ неправильный \_ тип \_ \_ привязки RPC**</span><span class="sxs-lookup"><span data-stu-id="5eb82-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC\_S\_WRONG\_KIND\_OF\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-113">1701 (0x6A5)</span><span class="sxs-lookup"><span data-stu-id="5eb82-113">1701 (0x6A5)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-114">Недопустимый тип маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="5eb82-114">The binding handle is not the correct type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**\_ \_ Недопустимая привязка RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-116">1702 (0x6A6)</span><span class="sxs-lookup"><span data-stu-id="5eb82-116">1702 (0x6A6)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-117">Недопустимый маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="5eb82-117">The binding handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**\_ПРОТСЕК RPC \_ S \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="5eb82-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC\_S\_PROTSEQ\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-119">1703 (0x6A7)</span><span class="sxs-lookup"><span data-stu-id="5eb82-119">1703 (0x6A7)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-120">Последовательность протокола RPC не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-120">The RPC protocol sequence is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ недопустимое \_ \_ протсек RPC**</span><span class="sxs-lookup"><span data-stu-id="5eb82-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC\_S\_INVALID\_RPC\_PROTSEQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-122">1704 (0x6A8)</span><span class="sxs-lookup"><span data-stu-id="5eb82-122">1704 (0x6A8)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-123">Последовательность протокола RPC недопустима.</span><span class="sxs-lookup"><span data-stu-id="5eb82-123">The RPC protocol sequence is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC \_ S \_ Недопустимая \_ строка \_ UUID**</span><span class="sxs-lookup"><span data-stu-id="5eb82-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC\_S\_INVALID\_STRING\_UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-125">1705 (0x6A9)</span><span class="sxs-lookup"><span data-stu-id="5eb82-125">1705 (0x6A9)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-126">Недопустимый универсальный уникальный идентификатор (UUID).</span><span class="sxs-lookup"><span data-stu-id="5eb82-126">The string universal unique identifier (UUID) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**\_ \_ Недопустимый \_ Формат конечной точки RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC\_S\_INVALID\_ENDPOINT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-128">1706 (0x6AA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-128">1706 (0x6AA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-129">Недопустимый формат конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5eb82-129">The endpoint format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**\_ \_ Недопустимый \_ сетевой \_ адрес RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC\_S\_INVALID\_NET\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-131">1707 (0x6AB)</span><span class="sxs-lookup"><span data-stu-id="5eb82-131">1707 (0x6AB)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-132">Недопустимый сетевой адрес.</span><span class="sxs-lookup"><span data-stu-id="5eb82-132">The network address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S \_ не \_ найдена конечная точка \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC\_S\_NO\_ENDPOINT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-134">1708 (0x6AC)</span><span class="sxs-lookup"><span data-stu-id="5eb82-134">1708 (0x6AC)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-135">Конечная точка не найдена.</span><span class="sxs-lookup"><span data-stu-id="5eb82-135">No endpoint was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**\_ \_ недопустимое \_ время ожидания RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC\_S\_INVALID\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-137">1709 (0x6AD)</span><span class="sxs-lookup"><span data-stu-id="5eb82-137">1709 (0x6AD)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-138">Недопустимое значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="5eb82-138">The timeout value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**\_объект RPC \_ S \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="5eb82-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**RPC\_S\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-140">1710 (0x6AE)</span><span class="sxs-lookup"><span data-stu-id="5eb82-140">1710 (0x6AE)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-141">Не найден универсальный уникальный идентификатор (UUID) объекта.</span><span class="sxs-lookup"><span data-stu-id="5eb82-141">The object universal unique identifier (UUID) was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ S \_ уже \_ зарегистрирован**</span><span class="sxs-lookup"><span data-stu-id="5eb82-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC\_S\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-143">1711 (0x6AF)</span><span class="sxs-lookup"><span data-stu-id="5eb82-143">1711 (0x6AF)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-144">Универсальный уникальный идентификатор (UUID) объекта уже зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="5eb82-144">The object universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**\_тип RPC \_ S \_ уже \_ зарегистрирован**</span><span class="sxs-lookup"><span data-stu-id="5eb82-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**RPC\_S\_TYPE\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-146">1712 (0x6B0)</span><span class="sxs-lookup"><span data-stu-id="5eb82-146">1712 (0x6B0)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-147">Универсальный уникальный идентификатор (UUID) типа уже зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="5eb82-147">The type universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ S \_ уже \_ прослушивает**</span><span class="sxs-lookup"><span data-stu-id="5eb82-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC\_S\_ALREADY\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-149">1713 (0x6B1)</span><span class="sxs-lookup"><span data-stu-id="5eb82-149">1713 (0x6B1)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-150">Сервер RPC уже прослушивается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-150">The RPC server is already listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ \_ протсекс не \_ зарегистрирован**</span><span class="sxs-lookup"><span data-stu-id="5eb82-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC\_S\_NO\_PROTSEQS\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-152">1714 (0x6B2)</span><span class="sxs-lookup"><span data-stu-id="5eb82-152">1714 (0x6B2)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-153">Последовательности протоколов не зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="5eb82-153">No protocol sequences have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ не \_ ожидает передачи данных**</span><span class="sxs-lookup"><span data-stu-id="5eb82-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC\_S\_NOT\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-155">1715 (0x6B3)</span><span class="sxs-lookup"><span data-stu-id="5eb82-155">1715 (0x6B3)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-156">Сервер RPC не прослушивается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-156">The RPC server is not listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**\_неизвестный \_ \_ тип диспетчера \_ RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC\_S\_UNKNOWN\_MGR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-158">1716 (0x6B4)</span><span class="sxs-lookup"><span data-stu-id="5eb82-158">1716 (0x6B4)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-159">Неизвестный тип диспетчера.</span><span class="sxs-lookup"><span data-stu-id="5eb82-159">The manager type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ Unknown, \_ Если**</span><span class="sxs-lookup"><span data-stu-id="5eb82-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC\_S\_UNKNOWN\_IF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-161">1717 (0x6B5)</span><span class="sxs-lookup"><span data-stu-id="5eb82-161">1717 (0x6B5)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-162">Неизвестный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="5eb82-162">The interface is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ нет \_ привязок**</span><span class="sxs-lookup"><span data-stu-id="5eb82-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC\_S\_NO\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-164">1718 (0x6B6)</span><span class="sxs-lookup"><span data-stu-id="5eb82-164">1718 (0x6B6)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-165">Привязки отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="5eb82-165">There are no bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ нет \_ протсекс**</span><span class="sxs-lookup"><span data-stu-id="5eb82-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC\_S\_NO\_PROTSEQS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-167">1719 (0x6B7)</span><span class="sxs-lookup"><span data-stu-id="5eb82-167">1719 (0x6B7)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-168">Нет последовательностей протоколов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-168">There are no protocol sequences.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S не \_ удается \_ создать \_ конечную точку**</span><span class="sxs-lookup"><span data-stu-id="5eb82-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC\_S\_CANT\_CREATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-170">1720 (0x6B8)</span><span class="sxs-lookup"><span data-stu-id="5eb82-170">1720 (0x6B8)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-171">Не удается создать конечную точку.</span><span class="sxs-lookup"><span data-stu-id="5eb82-171">The endpoint cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC \_ S \_ не \_ хватает \_ ресурсов**</span><span class="sxs-lookup"><span data-stu-id="5eb82-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC\_S\_OUT\_OF\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-173">1721 (0x6B9)</span><span class="sxs-lookup"><span data-stu-id="5eb82-173">1721 (0x6B9)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-174">Недостаточно ресурсов для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="5eb82-174">Not enough resources are available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**\_сервер RPC \_ S \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC\_S\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-176">1722 (0x6BA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-176">1722 (0x6BA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-177">Сервер RPC недоступен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-177">The RPC server is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**\_сервер RPC \_ S \_ \_ занят**</span><span class="sxs-lookup"><span data-stu-id="5eb82-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC\_S\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-179">1723 (0x6BB)</span><span class="sxs-lookup"><span data-stu-id="5eb82-179">1723 (0x6BB)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-180">Сервер RPC слишком занят для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="5eb82-180">The RPC server is too busy to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**\_ \_ недопустимые \_ Параметры сети RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC\_S\_INVALID\_NETWORK\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-182">1724 (0x6BC)</span><span class="sxs-lookup"><span data-stu-id="5eb82-182">1724 (0x6BC)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-183">Недопустимые параметры сети.</span><span class="sxs-lookup"><span data-stu-id="5eb82-183">The network options are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S \_ нет \_ \_ активных вызовов**</span><span class="sxs-lookup"><span data-stu-id="5eb82-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC\_S\_NO\_CALL\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-185">1725 (0x6BD)</span><span class="sxs-lookup"><span data-stu-id="5eb82-185">1725 (0x6BD)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-186">В этом потоке отсутствуют активные вызовы удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="5eb82-186">There are no remote procedure calls active on this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**\_ \_ сбой вызова RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**RPC\_S\_CALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-188">1726 (0x6BE)</span><span class="sxs-lookup"><span data-stu-id="5eb82-188">1726 (0x6BE)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-189">Сбой вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="5eb82-189">The remote procedure call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**\_ \_ сбой вызова RPC \_ S \_ дне**</span><span class="sxs-lookup"><span data-stu-id="5eb82-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**RPC\_S\_CALL\_FAILED\_DNE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-191">1727 (0x6BF)</span><span class="sxs-lookup"><span data-stu-id="5eb82-191">1727 (0x6BF)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-192">Не удалось выполнить удаленный вызов процедуры, так как он не выполнен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-192">The remote procedure call failed and did not execute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**\_ \_ Ошибка протокола RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC\_S\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-194">1728 (0x6C0)</span><span class="sxs-lookup"><span data-stu-id="5eb82-194">1728 (0x6C0)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-195">Произошла ошибка протокола удаленного вызова процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="5eb82-195">A remote procedure call (RPC) protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**\_ \_ доступ прокси-сервера RPC S \_ \_ запрещен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC\_S\_PROXY\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-197">1729 (0x6C1)</span><span class="sxs-lookup"><span data-stu-id="5eb82-197">1729 (0x6C1)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-198">Отказано в доступе к прокси-серверу HTTP.</span><span class="sxs-lookup"><span data-stu-id="5eb82-198">Access to the HTTP proxy is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**\_ \_ неподдерживаемый входящий \_ \_ флаг RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC\_S\_UNSUPPORTED\_TRANS\_SYN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-200">1730 (0x6C2)</span><span class="sxs-lookup"><span data-stu-id="5eb82-200">1730 (0x6C2)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-201">Синтаксис перемещения не поддерживается сервером RPC.</span><span class="sxs-lookup"><span data-stu-id="5eb82-201">The transfer syntax is not supported by the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**\_ \_ неподдерживаемый тип RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC\_S\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-203">1732 (0x6C4)</span><span class="sxs-lookup"><span data-stu-id="5eb82-203">1732 (0x6C4)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-204">Тип универсального уникального идентификатора (UUID) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-204">The universal unique identifier (UUID) type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**\_ \_ Недопустимый \_ тег RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC\_S\_INVALID\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-206">1733 (0x6C5)</span><span class="sxs-lookup"><span data-stu-id="5eb82-206">1733 (0x6C5)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-207">Недопустимый тег.</span><span class="sxs-lookup"><span data-stu-id="5eb82-207">The tag is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**\_ \_ Недопустимая привязка RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC\_S\_INVALID\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-209">1734 (0x6C6)</span><span class="sxs-lookup"><span data-stu-id="5eb82-209">1734 (0x6C6)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-210">Недопустимые границы массива.</span><span class="sxs-lookup"><span data-stu-id="5eb82-210">The array bounds are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ S \_ \_ имя записи \_ отсутствует**</span><span class="sxs-lookup"><span data-stu-id="5eb82-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC\_S\_NO\_ENTRY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-212">1735 (0x6C7)</span><span class="sxs-lookup"><span data-stu-id="5eb82-212">1735 (0x6C7)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-213">Привязка не содержит имени записи.</span><span class="sxs-lookup"><span data-stu-id="5eb82-213">The binding does not contain an entry name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**\_ \_ Недопустимый \_ синтаксис имени RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC\_S\_INVALID\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-215">1736 (0x6C8)</span><span class="sxs-lookup"><span data-stu-id="5eb82-215">1736 (0x6C8)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-216">Недопустимый синтаксис имени.</span><span class="sxs-lookup"><span data-stu-id="5eb82-216">The name syntax is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**\_ \_ неподдерживаемый \_ синтаксис имени RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC\_S\_UNSUPPORTED\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-218">1737 (0x6C9)</span><span class="sxs-lookup"><span data-stu-id="5eb82-218">1737 (0x6C9)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-219">Синтаксис имени не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-219">The name syntax is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**\_ \_ идентификатор UUID RPC S не является \_ \_ адресом**</span><span class="sxs-lookup"><span data-stu-id="5eb82-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC\_S\_UUID\_NO\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-221">1739 (0x6CB)</span><span class="sxs-lookup"><span data-stu-id="5eb82-221">1739 (0x6CB)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-222">Нет доступного сетевого адреса для создания универсального уникального идентификатора (UUID).</span><span class="sxs-lookup"><span data-stu-id="5eb82-222">No network address is available to use to construct a universal unique identifier (UUID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_ \_ повторяющаяся \_ Конечная точка RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**RPC\_S\_DUPLICATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-224">1740 (0x6CC)</span><span class="sxs-lookup"><span data-stu-id="5eb82-224">1740 (0x6CC)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-225">Повторяющаяся конечная точка.</span><span class="sxs-lookup"><span data-stu-id="5eb82-225">The endpoint is a duplicate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_неизвестный \_ \_ тип AUTHN \_ RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**RPC\_S\_UNKNOWN\_AUTHN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-227">1741 (0x6CD)</span><span class="sxs-lookup"><span data-stu-id="5eb82-227">1741 (0x6CD)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-228">Неизвестный тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5eb82-228">The authentication type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**\_ \_ Максимальное число вызовов RPC S \_ \_ слишком \_ мало**</span><span class="sxs-lookup"><span data-stu-id="5eb82-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC\_S\_MAX\_CALLS\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-230">1742 (0x6CE)</span><span class="sxs-lookup"><span data-stu-id="5eb82-230">1742 (0x6CE)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-231">Максимальное число вызовов слишком мало.</span><span class="sxs-lookup"><span data-stu-id="5eb82-231">The maximum number of calls is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**\_ \_ \_ слишком \_ длинная строка RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC\_S\_STRING\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-233">1743 (0x6CF)</span><span class="sxs-lookup"><span data-stu-id="5eb82-233">1743 (0x6CF)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-234">Строка слишком длинная.</span><span class="sxs-lookup"><span data-stu-id="5eb82-234">The string is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**\_ПРОТСЕК RPC \_ S \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="5eb82-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC\_S\_PROTSEQ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-236">1744 (0x6D0)</span><span class="sxs-lookup"><span data-stu-id="5eb82-236">1744 (0x6D0)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-237">Последовательность протокола RPC не найдена.</span><span class="sxs-lookup"><span data-stu-id="5eb82-237">The RPC protocol sequence was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**\_ПРОКНУМ RPC \_ S \_ за пределами \_ \_ диапазона**</span><span class="sxs-lookup"><span data-stu-id="5eb82-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC\_S\_PROCNUM\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-239">1745 (0x6D1)</span><span class="sxs-lookup"><span data-stu-id="5eb82-239">1745 (0x6D1)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-240">Номер процедуры выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="5eb82-240">The procedure number is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**\_Привязка RPC \_ S \_ \_ не имеет \_ проверки подлинности**</span><span class="sxs-lookup"><span data-stu-id="5eb82-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC\_S\_BINDING\_HAS\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-242">1746 (0x6D2)</span><span class="sxs-lookup"><span data-stu-id="5eb82-242">1746 (0x6D2)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-243">Привязка не содержит сведений о проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="5eb82-243">The binding does not contain any authentication information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**\_ \_ неизвестная \_ Служба AUTHN RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC\_S\_UNKNOWN\_AUTHN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-245">1747 (0x6D3)</span><span class="sxs-lookup"><span data-stu-id="5eb82-245">1747 (0x6D3)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-246">Неизвестная служба проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5eb82-246">The authentication service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**\_неизвестный \_ \_ уровень AUTHN \_ RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC\_S\_UNKNOWN\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-248">1748 (0x6D4)</span><span class="sxs-lookup"><span data-stu-id="5eb82-248">1748 (0x6D4)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-249">Неизвестный уровень проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5eb82-249">The authentication level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**\_ \_ недопустимое \_ удостоверение проверки подлинности RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC\_S\_INVALID\_AUTH\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-251">1749 (0x6D5)</span><span class="sxs-lookup"><span data-stu-id="5eb82-251">1749 (0x6D5)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-252">Недопустимый контекст безопасности.</span><span class="sxs-lookup"><span data-stu-id="5eb82-252">The security context is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**\_ \_ неизвестная \_ Служба AUTHZ RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC\_S\_UNKNOWN\_AUTHZ\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-254">1750 (0x6D6)</span><span class="sxs-lookup"><span data-stu-id="5eb82-254">1750 (0x6D6)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-255">Неизвестная служба авторизации.</span><span class="sxs-lookup"><span data-stu-id="5eb82-255">The authorization service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT \_ S \_ Недопустимая \_ запись**</span><span class="sxs-lookup"><span data-stu-id="5eb82-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT\_S\_INVALID\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-257">1751 (0x6D7)</span><span class="sxs-lookup"><span data-stu-id="5eb82-257">1751 (0x6D7)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-258">Недопустимая запись.</span><span class="sxs-lookup"><span data-stu-id="5eb82-258">The entry is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S не \_ удается \_ выполнить \_ Op**</span><span class="sxs-lookup"><span data-stu-id="5eb82-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT\_S\_CANT\_PERFORM\_OP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-260">1752 (0x6D8)</span><span class="sxs-lookup"><span data-stu-id="5eb82-260">1752 (0x6D8)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-261">Конечной точке сервера не удается выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="5eb82-261">The server endpoint cannot perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ не \_ зарегистрирован**</span><span class="sxs-lookup"><span data-stu-id="5eb82-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT\_S\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-263">1753 (0x6D9)</span><span class="sxs-lookup"><span data-stu-id="5eb82-263">1753 (0x6D9)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-264">В модуле сопоставления конечных точек больше нет доступных конечных узлов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-264">There are no more endpoints available from the endpoint mapper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**\_ \_ нет ничего \_ для \_ экспорта в RPC**</span><span class="sxs-lookup"><span data-stu-id="5eb82-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC\_S\_NOTHING\_TO\_EXPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-266">1754 (0x6DA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-266">1754 (0x6DA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-267">Нет экспортированных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-267">No interfaces have been exported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_неполное \_ \_ имя RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**RPC\_S\_INCOMPLETE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-269">1755 (0x6DB)</span><span class="sxs-lookup"><span data-stu-id="5eb82-269">1755 (0x6DB)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-270">Имя записи является неполным.</span><span class="sxs-lookup"><span data-stu-id="5eb82-270">The entry name is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC \_ S \_ недопустимое \_ \_ значение параметра сторно**</span><span class="sxs-lookup"><span data-stu-id="5eb82-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC\_S\_INVALID\_VERS\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-272">1756 (0x6DC)</span><span class="sxs-lookup"><span data-stu-id="5eb82-272">1756 (0x6DC)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-273">Недопустимый параметр версии.</span><span class="sxs-lookup"><span data-stu-id="5eb82-273">The version option is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ \_ больше нет \_ \_ членов**</span><span class="sxs-lookup"><span data-stu-id="5eb82-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC\_S\_NO\_MORE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-275">1757 (0x6DD)</span><span class="sxs-lookup"><span data-stu-id="5eb82-275">1757 (0x6DD)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-276">Больше нет членов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-276">There are no more members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ не \_ все \_ OBJ-файлы \_ Экспорт**</span><span class="sxs-lookup"><span data-stu-id="5eb82-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_UNEXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-278">1758 (0x6DE)</span><span class="sxs-lookup"><span data-stu-id="5eb82-278">1758 (0x6DE)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-279">Нет ничего для экспорта.</span><span class="sxs-lookup"><span data-stu-id="5eb82-279">There is nothing to unexport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_интерфейс RPC \_ S \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="5eb82-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**RPC\_S\_INTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-281">1759 (0x6DF)</span><span class="sxs-lookup"><span data-stu-id="5eb82-281">1759 (0x6DF)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-282">Интерфейс не найден.</span><span class="sxs-lookup"><span data-stu-id="5eb82-282">The interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**\_запись RPC \_ S \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="5eb82-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC\_S\_ENTRY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-284">1760 (0x6E0)</span><span class="sxs-lookup"><span data-stu-id="5eb82-284">1760 (0x6E0)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-285">Запись уже существует.</span><span class="sxs-lookup"><span data-stu-id="5eb82-285">The entry already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**\_запись RPC \_ S \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="5eb82-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC\_S\_ENTRY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-287">1761 (0x6E1)</span><span class="sxs-lookup"><span data-stu-id="5eb82-287">1761 (0x6E1)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-288">Запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="5eb82-288">The entry is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**\_ \_ служба имен RPC \_ \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="5eb82-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC\_S\_NAME\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-290">1762 (0x6E2)</span><span class="sxs-lookup"><span data-stu-id="5eb82-290">1762 (0x6E2)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-291">Служба имен недоступна.</span><span class="sxs-lookup"><span data-stu-id="5eb82-291">The name service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ неправильный \_ \_ идентификатор "RPC S"**</span><span class="sxs-lookup"><span data-stu-id="5eb82-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC\_S\_INVALID\_NAF\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-293">1763 (0x6E3)</span><span class="sxs-lookup"><span data-stu-id="5eb82-293">1763 (0x6E3)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-294">Недопустимое семейство сетевых адресов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-294">The network address family is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ S \_ не \_ поддерживает**</span><span class="sxs-lookup"><span data-stu-id="5eb82-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC\_S\_CANNOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-296">1764 (0x6E4)</span><span class="sxs-lookup"><span data-stu-id="5eb82-296">1764 (0x6E4)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-297">Запрошенная операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-297">The requested operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**\_ \_ нет \_ доступных контекстов RPC. \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC\_S\_NO\_CONTEXT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-299">1765 (0x6E5)</span><span class="sxs-lookup"><span data-stu-id="5eb82-299">1765 (0x6E5)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-300">Нет доступных контекстов безопасности для разрешения олицетворения.</span><span class="sxs-lookup"><span data-stu-id="5eb82-300">No security context is available to allow impersonation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_ \_ Внутренняя ошибка RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**RPC\_S\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-302">1766 (0x6E6)</span><span class="sxs-lookup"><span data-stu-id="5eb82-302">1766 (0x6E6)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-303">Произошла внутренняя ошибка в удаленном вызове процедуры (RPC).</span><span class="sxs-lookup"><span data-stu-id="5eb82-303">An internal error occurred in a remote procedure call (RPC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC \_ с \_ нулевым \_ делением**</span><span class="sxs-lookup"><span data-stu-id="5eb82-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC\_S\_ZERO\_DIVIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-305">1767 (0x6E7)</span><span class="sxs-lookup"><span data-stu-id="5eb82-305">1767 (0x6E7)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-306">Сервер RPC попытался выполнить целочисленное деление на ноль.</span><span class="sxs-lookup"><span data-stu-id="5eb82-306">The RPC server attempted an integer division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**\_ \_ Ошибка адреса RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC\_S\_ADDRESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-308">1768 (0x6E8)</span><span class="sxs-lookup"><span data-stu-id="5eb82-308">1768 (0x6E8)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-309">Произошла ошибка адресации на сервере RPC.</span><span class="sxs-lookup"><span data-stu-id="5eb82-309">An addressing error occurred in the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**\_0 подключений \_ FP \_ div, \_ ноль**</span><span class="sxs-lookup"><span data-stu-id="5eb82-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC\_S\_FP\_DIV\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-311">1769 (0x6E9)</span><span class="sxs-lookup"><span data-stu-id="5eb82-311">1769 (0x6E9)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-312">Операция с плавающей точкой на сервере RPC привела к делению на нуль.</span><span class="sxs-lookup"><span data-stu-id="5eb82-312">A floating-point operation at the RPC server caused a division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**\_потеря точности в RPC с \_ плавающей запятой \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC\_S\_FP\_UNDERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-314">1770 (0x6EA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-314">1770 (0x6EA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-315">На сервере RPC произошла потеря точности с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="5eb82-315">A floating-point underflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**\_ \_ переполнение FP в RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC\_S\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-317">1771 (0x6EB)</span><span class="sxs-lookup"><span data-stu-id="5eb82-317">1771 (0x6EB)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-318">Переполнение с плавающей запятой произошло на сервере RPC.</span><span class="sxs-lookup"><span data-stu-id="5eb82-318">A floating-point overflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ больше \_ нет \_ записей**</span><span class="sxs-lookup"><span data-stu-id="5eb82-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC\_X\_NO\_MORE\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-320">1772 (0x6EC)</span><span class="sxs-lookup"><span data-stu-id="5eb82-320">1772 (0x6EC)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-321">Список серверов RPC, доступных для привязки автодескрипторов, исчерпан.</span><span class="sxs-lookup"><span data-stu-id="5eb82-321">The list of RPC servers available for the binding of auto handles has been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC \_ X \_ SS \_ , \_ \_ сбой передачи \_ char**</span><span class="sxs-lookup"><span data-stu-id="5eb82-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC\_X\_SS\_CHAR\_TRANS\_OPEN\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-323">1773 (0x6ED)</span><span class="sxs-lookup"><span data-stu-id="5eb82-323">1773 (0x6ED)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-324">Не удалось открыть файл таблицы преобразования символов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-324">Unable to open the character translation table file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**истечение \_ \_ \_ \_ \_ короткого файла для \_ транзакции RPC X SS**</span><span class="sxs-lookup"><span data-stu-id="5eb82-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC\_X\_SS\_CHAR\_TRANS\_SHORT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-326">1774 (0x6EE)</span><span class="sxs-lookup"><span data-stu-id="5eb82-326">1774 (0x6EE)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-327">Файл, содержащий таблицу преобразования символов, имеет менее 512 байт.</span><span class="sxs-lookup"><span data-stu-id="5eb82-327">The file containing the character translation table has fewer than 512 bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ в \_ \_ контексте null**</span><span class="sxs-lookup"><span data-stu-id="5eb82-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC\_X\_SS\_IN\_NULL\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-329">1775 (0x6EF)</span><span class="sxs-lookup"><span data-stu-id="5eb82-329">1775 (0x6EF)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-330">При вызове удаленной процедуры от клиента к узлу был передан нулевой маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="5eb82-330">A null context handle was passed from the client to the host during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**\_ \_ \_ повреждение контекста RPC X \_ SS**</span><span class="sxs-lookup"><span data-stu-id="5eb82-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC\_X\_SS\_CONTEXT\_DAMAGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-332">1777 (0x6F1)</span><span class="sxs-lookup"><span data-stu-id="5eb82-332">1777 (0x6F1)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-333">Обработчик контекста изменился во время удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="5eb82-333">The context handle changed during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**\_ \_ \_ несовпадение дескрипторов RPC X SS \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC\_X\_SS\_HANDLES\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-335">1778 (0x6F2)</span><span class="sxs-lookup"><span data-stu-id="5eb82-335">1778 (0x6F2)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-336">Дескрипторы привязки, переданные удаленному вызову процедуры, не совпадают.</span><span class="sxs-lookup"><span data-stu-id="5eb82-336">The binding handles passed to a remote procedure call do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ не \_ может \_ получить \_ маркер вызова**</span><span class="sxs-lookup"><span data-stu-id="5eb82-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC\_X\_SS\_CANNOT\_GET\_CALL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-338">1779 (0x6F3)</span><span class="sxs-lookup"><span data-stu-id="5eb82-338">1779 (0x6F3)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-339">Заглушке не удается получить маркер удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="5eb82-339">The stub is unable to get the remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**\_ \_ пустой \_ указатель ссылки RPC \_ X**</span><span class="sxs-lookup"><span data-stu-id="5eb82-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC\_X\_NULL\_REF\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-341">1780 (0x6F4)</span><span class="sxs-lookup"><span data-stu-id="5eb82-341">1780 (0x6F4)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-342">Заглушке передан пустой указатель ссылки.</span><span class="sxs-lookup"><span data-stu-id="5eb82-342">A null reference pointer was passed to the stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**\_ \_ значение перечисления RPC \_ X \_ вне \_ \_ допустимого диапазона**</span><span class="sxs-lookup"><span data-stu-id="5eb82-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-344">1781 (0x6F5)</span><span class="sxs-lookup"><span data-stu-id="5eb82-344">1781 (0x6F5)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-345">Значение перечисления вне диапазона.</span><span class="sxs-lookup"><span data-stu-id="5eb82-345">The enumeration value is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**\_ \_ число байт RPC \_ X \_ слишком \_ мало**</span><span class="sxs-lookup"><span data-stu-id="5eb82-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC\_X\_BYTE\_COUNT\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-347">1782 (0x6F6)</span><span class="sxs-lookup"><span data-stu-id="5eb82-347">1782 (0x6F6)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-348">Число байтов слишком мало.</span><span class="sxs-lookup"><span data-stu-id="5eb82-348">The byte count is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**\_ \_ неверные \_ данные заглушки RPC X \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC\_X\_BAD\_STUB\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-350">1783 (0x6F7)</span><span class="sxs-lookup"><span data-stu-id="5eb82-350">1783 (0x6F7)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-351">Заглушка получила неправильные данные.</span><span class="sxs-lookup"><span data-stu-id="5eb82-351">The stub received bad data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**Ошибка \_ недопустимого \_ \_ буфера пользователя**</span><span class="sxs-lookup"><span data-stu-id="5eb82-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERROR\_INVALID\_USER\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-353">1784 (0x6F8)</span><span class="sxs-lookup"><span data-stu-id="5eb82-353">1784 (0x6F8)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-354">Указанный буфер пользователя недопустим для запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="5eb82-354">The supplied user buffer is not valid for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**Ошибка \_ НЕопознанного \_ носителя**</span><span class="sxs-lookup"><span data-stu-id="5eb82-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERROR\_UNRECOGNIZED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-356">1785 (0x6F9)</span><span class="sxs-lookup"><span data-stu-id="5eb82-356">1785 (0x6F9)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-357">Дисковый носитель не распознан.</span><span class="sxs-lookup"><span data-stu-id="5eb82-357">The disk media is not recognized.</span></span> <span data-ttu-id="5eb82-358">Возможно, он не отформатирован.</span><span class="sxs-lookup"><span data-stu-id="5eb82-358">It may not be formatted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**Ошибка \_ без \_ доверия \_ \_ секрет LSA**</span><span class="sxs-lookup"><span data-stu-id="5eb82-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERROR\_NO\_TRUST\_LSA\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-360">1786 (0x6FA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-360">1786 (0x6FA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-361">Рабочая станция не имеет секрета доверия.</span><span class="sxs-lookup"><span data-stu-id="5eb82-361">The workstation does not have a trust secret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**Ошибка \_ \_ : нет \_ \_ учетной записи SAM доверия**</span><span class="sxs-lookup"><span data-stu-id="5eb82-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERROR\_NO\_TRUST\_SAM\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-363">1787 (0x6FB)</span><span class="sxs-lookup"><span data-stu-id="5eb82-363">1787 (0x6FB)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-364">База данных безопасности на сервере не имеет учетной записи компьютера для этого отношения доверия рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="5eb82-364">The security database on the server does not have a computer account for this workstation trust relationship.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**Ошибка \_ доверенного \_ домена при ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERROR\_TRUSTED\_DOMAIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-366">1788 (0x6FC)</span><span class="sxs-lookup"><span data-stu-id="5eb82-366">1788 (0x6FC)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-367">Не удалось установить доверительные отношения между основным доменом и доверенным доменом.</span><span class="sxs-lookup"><span data-stu-id="5eb82-367">The trust relationship between the primary domain and the trusted domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**Ошибка \_ \_ \_ при сбое доверительной связи**</span><span class="sxs-lookup"><span data-stu-id="5eb82-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERROR\_TRUSTED\_RELATIONSHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-369">1789 (0x6FD)</span><span class="sxs-lookup"><span data-stu-id="5eb82-369">1789 (0x6FD)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-370">Сбой отношения доверия между данной рабочей станцией и основным доменом.</span><span class="sxs-lookup"><span data-stu-id="5eb82-370">The trust relationship between this workstation and the primary domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**Ошибка \_ доверия \_ при сбое**</span><span class="sxs-lookup"><span data-stu-id="5eb82-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-372">1790 (0x6FE)</span><span class="sxs-lookup"><span data-stu-id="5eb82-372">1790 (0x6FE)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-373">Ошибка входа в сеть.</span><span class="sxs-lookup"><span data-stu-id="5eb82-373">The network logon failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**\_ \_ выполняется вызов RPC \_ S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC\_S\_CALL\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-375">1791 (0x6FF)</span><span class="sxs-lookup"><span data-stu-id="5eb82-375">1791 (0x6FF)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-376">Удаленный вызов процедур уже выполняется для этого потока.</span><span class="sxs-lookup"><span data-stu-id="5eb82-376">A remote procedure call is already in progress for this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**Ошибка \_ Netlogon \_ не \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="5eb82-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERROR\_NETLOGON\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-378">1792 (0X700)</span><span class="sxs-lookup"><span data-stu-id="5eb82-378">1792 (0x700)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-379">Предпринята попытка входа в систему, но служба сетевого входа не запущена.</span><span class="sxs-lookup"><span data-stu-id="5eb82-379">An attempt was made to logon, but the network logon service was not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**\_срок действия учетной записи ошибки \_ истек**</span><span class="sxs-lookup"><span data-stu-id="5eb82-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**ERROR\_ACCOUNT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-381">1793 (0x701)</span><span class="sxs-lookup"><span data-stu-id="5eb82-381">1793 (0x701)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-382">Срок действия учетной записи пользователя истек.</span><span class="sxs-lookup"><span data-stu-id="5eb82-382">The user's account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**Перенаправитель ошибок \_ \_ имеет \_ открытые \_ дескрипторы**</span><span class="sxs-lookup"><span data-stu-id="5eb82-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**ERROR\_REDIRECTOR\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-384">1794 (0x702)</span><span class="sxs-lookup"><span data-stu-id="5eb82-384">1794 (0x702)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-385">Перенаправитель используется и не может быть выгружен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-385">The redirector is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**\_драйвер принтера \_ ошибок \_ уже \_ установлен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERROR\_PRINTER\_DRIVER\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-387">1795 (0x703)</span><span class="sxs-lookup"><span data-stu-id="5eb82-387">1795 (0x703)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-388">Указанный драйвер принтера уже установлен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-388">The specified printer driver is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**Ошибка \_ неизвестного \_ порта**</span><span class="sxs-lookup"><span data-stu-id="5eb82-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERROR\_UNKNOWN\_PORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-390">1796 (0x704)</span><span class="sxs-lookup"><span data-stu-id="5eb82-390">1796 (0x704)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-391">Указанный порт неизвестен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-391">The specified port is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**Ошибка \_ неизвестного \_ \_ драйвера принтера**</span><span class="sxs-lookup"><span data-stu-id="5eb82-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERROR\_UNKNOWN\_PRINTER\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-393">1797 (0x705)</span><span class="sxs-lookup"><span data-stu-id="5eb82-393">1797 (0x705)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-394">Неизвестный драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="5eb82-394">The printer driver is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**Ошибка \_ неизвестного \_ принтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="5eb82-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERROR\_UNKNOWN\_PRINTPROCESSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-396">1798 (0x706)</span><span class="sxs-lookup"><span data-stu-id="5eb82-396">1798 (0x706)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-397">Неизвестный обработчик заданий печати.</span><span class="sxs-lookup"><span data-stu-id="5eb82-397">The print processor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**Ошибка \_ недопустимого \_ \_ файла разделителя**</span><span class="sxs-lookup"><span data-stu-id="5eb82-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERROR\_INVALID\_SEPARATOR\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-399">1799 (0x707)</span><span class="sxs-lookup"><span data-stu-id="5eb82-399">1799 (0x707)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-400">Указан недопустимый файл разделителя.</span><span class="sxs-lookup"><span data-stu-id="5eb82-400">The specified separator file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**Ошибка \_ недопустимого \_ приоритета**</span><span class="sxs-lookup"><span data-stu-id="5eb82-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERROR\_INVALID\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-402">1800 (0x708)</span><span class="sxs-lookup"><span data-stu-id="5eb82-402">1800 (0x708)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-403">Указан недопустимый приоритет.</span><span class="sxs-lookup"><span data-stu-id="5eb82-403">The specified priority is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**Ошибка \_ недопустимое \_ \_ имя принтера**</span><span class="sxs-lookup"><span data-stu-id="5eb82-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERROR\_INVALID\_PRINTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-405">1801 (0x709)</span><span class="sxs-lookup"><span data-stu-id="5eb82-405">1801 (0x709)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-406">Недопустимое имя принтера.</span><span class="sxs-lookup"><span data-stu-id="5eb82-406">The printer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**\_принтер ошибок \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="5eb82-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**ERROR\_PRINTER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-408">1802 (0x70A)</span><span class="sxs-lookup"><span data-stu-id="5eb82-408">1802 (0x70A)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-409">Принтер уже существует.</span><span class="sxs-lookup"><span data-stu-id="5eb82-409">The printer already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**Ошибка \_ недопустимой \_ \_ команды принтера**</span><span class="sxs-lookup"><span data-stu-id="5eb82-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERROR\_INVALID\_PRINTER\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-411">1803 (0x70B)</span><span class="sxs-lookup"><span data-stu-id="5eb82-411">1803 (0x70B)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-412">Недопустимая команда принтера.</span><span class="sxs-lookup"><span data-stu-id="5eb82-412">The printer command is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**Ошибка \_ недопустимого \_ типа данных**</span><span class="sxs-lookup"><span data-stu-id="5eb82-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR\_INVALID\_DATATYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-414">1804 (0x70C)</span><span class="sxs-lookup"><span data-stu-id="5eb82-414">1804 (0x70C)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-415">Указан недопустимый тип данных.</span><span class="sxs-lookup"><span data-stu-id="5eb82-415">The specified datatype is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**Ошибка \_ недопустимого \_ окружения**</span><span class="sxs-lookup"><span data-stu-id="5eb82-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERROR\_INVALID\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-417">1805 (0x70D)</span><span class="sxs-lookup"><span data-stu-id="5eb82-417">1805 (0x70D)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-418">Указана недопустимая среда.</span><span class="sxs-lookup"><span data-stu-id="5eb82-418">The environment specified is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ S \_ больше \_ нет \_ привязок**</span><span class="sxs-lookup"><span data-stu-id="5eb82-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC\_S\_NO\_MORE\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-420">1806 (0x70E)</span><span class="sxs-lookup"><span data-stu-id="5eb82-420">1806 (0x70E)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-421">Больше нет привязок.</span><span class="sxs-lookup"><span data-stu-id="5eb82-421">There are no more bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**Ошибка \_ без входа в \_ \_ \_ УЧЕТную запись междоменного доверия**</span><span class="sxs-lookup"><span data-stu-id="5eb82-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERROR\_NOLOGON\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-423">1807 (0x70F)</span><span class="sxs-lookup"><span data-stu-id="5eb82-423">1807 (0x70F)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-424">Используемая учетная запись является учетной записью междоменного доверия.</span><span class="sxs-lookup"><span data-stu-id="5eb82-424">The account used is an interdomain trust account.</span></span> <span data-ttu-id="5eb82-425">Для доступа к серверу используйте глобальную учетную запись пользователя или локальную учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="5eb82-425">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**Ошибка при \_ \_ \_ \_ учетной записи доверия рабочей станции без входа**</span><span class="sxs-lookup"><span data-stu-id="5eb82-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERROR\_NOLOGON\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-427">1808 (0x710)</span><span class="sxs-lookup"><span data-stu-id="5eb82-427">1808 (0x710)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-428">Используемая учетная запись — это учетная запись компьютера.</span><span class="sxs-lookup"><span data-stu-id="5eb82-428">The account used is a computer account.</span></span> <span data-ttu-id="5eb82-429">Для доступа к серверу используйте глобальную учетную запись пользователя или локальную учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="5eb82-429">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**Ошибка при \_ подключении \_ \_ \_ учетной записи доверия сервера без имени**</span><span class="sxs-lookup"><span data-stu-id="5eb82-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERROR\_NOLOGON\_SERVER\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-431">1809 (0x711)</span><span class="sxs-lookup"><span data-stu-id="5eb82-431">1809 (0x711)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-432">Используемая учетная запись является учетной записью доверия сервера.</span><span class="sxs-lookup"><span data-stu-id="5eb82-432">The account used is a server trust account.</span></span> <span data-ttu-id="5eb82-433">Для доступа к серверу используйте глобальную учетную запись пользователя или локальную учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="5eb82-433">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**Ошибка \_ при \_ \_ несоответствии доверия домена**</span><span class="sxs-lookup"><span data-stu-id="5eb82-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERROR\_DOMAIN\_TRUST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-435">1810 (0x712)</span><span class="sxs-lookup"><span data-stu-id="5eb82-435">1810 (0x712)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-436">Имя или идентификатор безопасности (SID) указанного домена не согласуется со сведениями о доверии для этого домена.</span><span class="sxs-lookup"><span data-stu-id="5eb82-436">The name or security ID (SID) of the domain specified is inconsistent with the trust information for that domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**\_сервер ошибок \_ имеет \_ открытые \_ дескрипторы**</span><span class="sxs-lookup"><span data-stu-id="5eb82-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**ERROR\_SERVER\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-438">1811 (0x713)</span><span class="sxs-lookup"><span data-stu-id="5eb82-438">1811 (0x713)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-439">Сервер используется и не может быть выгружен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-439">The server is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**\_ \_ \_ не \_ найдены данные ресурса об ошибке**</span><span class="sxs-lookup"><span data-stu-id="5eb82-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**ERROR\_RESOURCE\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-441">1812 (0x714)</span><span class="sxs-lookup"><span data-stu-id="5eb82-441">1812 (0x714)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-442">Указанный файл изображения не содержит раздел ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-442">The specified image file did not contain a resource section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**\_тип ресурса \_ ошибки \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="5eb82-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**ERROR\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-444">1813 (0x715)</span><span class="sxs-lookup"><span data-stu-id="5eb82-444">1813 (0x715)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-445">Указанный тип ресурса не найден в файле образа.</span><span class="sxs-lookup"><span data-stu-id="5eb82-445">The specified resource type cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**\_ \_ \_ не \_ найдено имя ресурса ошибки**</span><span class="sxs-lookup"><span data-stu-id="5eb82-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERROR\_RESOURCE\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-447">1814 (0x716)</span><span class="sxs-lookup"><span data-stu-id="5eb82-447">1814 (0x716)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-448">Указанное имя ресурса не найдено в файле образа.</span><span class="sxs-lookup"><span data-stu-id="5eb82-448">The specified resource name cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**\_ \_ \_ не \_ удалось найти язык ресурса ошибок**</span><span class="sxs-lookup"><span data-stu-id="5eb82-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERROR\_RESOURCE\_LANG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-450">1815 (0x717)</span><span class="sxs-lookup"><span data-stu-id="5eb82-450">1815 (0x717)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-451">Указанный идентификатор языка ресурсов не найден в файле образа.</span><span class="sxs-lookup"><span data-stu-id="5eb82-451">The specified resource language ID cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**Ошибка \_ \_ недостаточно \_ квоты**</span><span class="sxs-lookup"><span data-stu-id="5eb82-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERROR\_NOT\_ENOUGH\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-453">1816 (0x718)</span><span class="sxs-lookup"><span data-stu-id="5eb82-453">1816 (0x718)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-454">Недостаточно квот для обработки команды.</span><span class="sxs-lookup"><span data-stu-id="5eb82-454">Not enough quota is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ нет \_ интерфейсов**</span><span class="sxs-lookup"><span data-stu-id="5eb82-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC\_S\_NO\_INTERFACES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-456">1817 (0x719)</span><span class="sxs-lookup"><span data-stu-id="5eb82-456">1817 (0x719)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-457">Нет зарегистрированных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-457">No interfaces have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**\_вызов RPC \_ S \_ отменен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC\_S\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-459">1818 (0x71A)</span><span class="sxs-lookup"><span data-stu-id="5eb82-459">1818 (0x71A)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-460">Удаленный вызов процедур был отменен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-460">The remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**\_Привязка RPC S не \_ \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="5eb82-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC\_S\_BINDING\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-462">1819 (0x71B)</span><span class="sxs-lookup"><span data-stu-id="5eb82-462">1819 (0x71B)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-463">Этот маркер привязки не содержит все необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="5eb82-463">The binding handle does not contain all required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**сбой связи RPC \_ S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC\_S\_COMM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-465">1820 (0x71C)</span><span class="sxs-lookup"><span data-stu-id="5eb82-465">1820 (0x71C)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-466">Ошибка связи при удаленном вызове процедуры.</span><span class="sxs-lookup"><span data-stu-id="5eb82-466">A communications failure occurred during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**\_ \_ неподдерживаемый \_ уровень AUTHN RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC\_S\_UNSUPPORTED\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-468">1821 (0x71D)</span><span class="sxs-lookup"><span data-stu-id="5eb82-468">1821 (0x71D)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-469">Запрошенный уровень проверки подлинности не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-469">The requested authentication level is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ S \_ без \_ \_ имени принк**</span><span class="sxs-lookup"><span data-stu-id="5eb82-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC\_S\_NO\_PRINC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-471">1822 (0x71E)</span><span class="sxs-lookup"><span data-stu-id="5eb82-471">1822 (0x71E)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-472">Имя участника не зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="5eb82-472">No principal name registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ S \_ не \_ \_ Ошибка RPC**</span><span class="sxs-lookup"><span data-stu-id="5eb82-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC\_S\_NOT\_RPC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-474">1823 (0x71F)</span><span class="sxs-lookup"><span data-stu-id="5eb82-474">1823 (0x71F)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-475">Указанная ошибка не является допустимым кодом ошибки RPC Windows.</span><span class="sxs-lookup"><span data-stu-id="5eb82-475">The error specified is not a valid Windows RPC error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_ \_ \_ только локальная UUID RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC\_S\_UUID\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-477">1824 (0x720)</span><span class="sxs-lookup"><span data-stu-id="5eb82-477">1824 (0x720)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-478">Выделен UUID, допустимый только на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="5eb82-478">A UUID that is valid only on this computer has been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**\_ \_ \_ \_ Ошибка pkg при вызове RPC S sec**</span><span class="sxs-lookup"><span data-stu-id="5eb82-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC\_S\_SEC\_PKG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-480">1825 (0x721)</span><span class="sxs-lookup"><span data-stu-id="5eb82-480">1825 (0x721)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-481">Произошла ошибка, относящаяся к пакету безопасности.</span><span class="sxs-lookup"><span data-stu-id="5eb82-481">A security package specific error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ не \_ отменен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC\_S\_NOT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-483">1826 (0x722)</span><span class="sxs-lookup"><span data-stu-id="5eb82-483">1826 (0x722)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-484">Поток не отменен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-484">Thread is not canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**\_ \_ недопустимое \_ действие ES RPC X \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC\_X\_INVALID\_ES\_ACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-486">1827 (0x723)</span><span class="sxs-lookup"><span data-stu-id="5eb82-486">1827 (0x723)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-487">Недопустимая операция с маркером кодирования или декодирования.</span><span class="sxs-lookup"><span data-stu-id="5eb82-487">Invalid operation on the encoding/decoding handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**\_ \_ неправильная \_ версия ES RPC X \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC\_X\_WRONG\_ES\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-489">1828 (0x724)</span><span class="sxs-lookup"><span data-stu-id="5eb82-489">1828 (0x724)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-490">Несовместимая версия пакета сериализации.</span><span class="sxs-lookup"><span data-stu-id="5eb82-490">Incompatible version of the serializing package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**\_ \_ неправильная \_ версия заглушки RPC X \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC\_X\_WRONG\_STUB\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-492">1829 (0x725)</span><span class="sxs-lookup"><span data-stu-id="5eb82-492">1829 (0x725)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-493">Несовместимая версия заглушки RPC.</span><span class="sxs-lookup"><span data-stu-id="5eb82-493">Incompatible version of the RPC stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC \_ X \_ Недопустимый \_ \_ объект канала**</span><span class="sxs-lookup"><span data-stu-id="5eb82-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC\_X\_INVALID\_PIPE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-495">1830 (0x726)</span><span class="sxs-lookup"><span data-stu-id="5eb82-495">1830 (0x726)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-496">Объект канала RPC недопустим или поврежден.</span><span class="sxs-lookup"><span data-stu-id="5eb82-496">The RPC pipe object is invalid or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**\_ \_ неправильный \_ порядок каналов RPC \_ X**</span><span class="sxs-lookup"><span data-stu-id="5eb82-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC\_X\_WRONG\_PIPE\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-498">1831 (0x727)</span><span class="sxs-lookup"><span data-stu-id="5eb82-498">1831 (0x727)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-499">Попытка выполнить недопустимую операцию для объекта канала RPC.</span><span class="sxs-lookup"><span data-stu-id="5eb82-499">An invalid operation was attempted on an RPC pipe object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**\_ \_ неправильная \_ версия канала RPC X \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC\_X\_WRONG\_PIPE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-501">1832 (0x728)</span><span class="sxs-lookup"><span data-stu-id="5eb82-501">1832 (0x728)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-502">Неподдерживаемая версия канала RPC.</span><span class="sxs-lookup"><span data-stu-id="5eb82-502">Unsupported RPC pipe version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**\_ \_ \_ Ошибка проверки подлинности cookie RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**RPC\_S\_COOKIE\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-504">1833 (0x729)</span><span class="sxs-lookup"><span data-stu-id="5eb82-504">1833 (0x729)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-505">Прокси-сервер HTTP отклонил подключение, так как произошел сбой при проверке подлинности файла cookie.</span><span class="sxs-lookup"><span data-stu-id="5eb82-505">HTTP proxy server rejected the connection because the cookie authentication failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**\_ \_ член группы RPC \_ S \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="5eb82-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**RPC\_S\_GROUP\_MEMBER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-507">1898 (0x76A)</span><span class="sxs-lookup"><span data-stu-id="5eb82-507">1898 (0x76A)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-508">Член группы не найден.</span><span class="sxs-lookup"><span data-stu-id="5eb82-508">The group member was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S не \_ удается \_ создать**</span><span class="sxs-lookup"><span data-stu-id="5eb82-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT\_S\_CANT\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-510">1899 (0x76B)</span><span class="sxs-lookup"><span data-stu-id="5eb82-510">1899 (0x76B)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-511">Не удалось создать запись базы данных сопоставителя конечных точек.</span><span class="sxs-lookup"><span data-stu-id="5eb82-511">The endpoint mapper database entry could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**\_ \_ Недопустимый \_ объект RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC\_S\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-513">1900 (0x76C)</span><span class="sxs-lookup"><span data-stu-id="5eb82-513">1900 (0x76C)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-514">Универсальный уникальный идентификатор (UUID) объекта является пустым UUID.</span><span class="sxs-lookup"><span data-stu-id="5eb82-514">The object universal unique identifier (UUID) is the nil UUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**Ошибка \_ недопустимое \_ время**</span><span class="sxs-lookup"><span data-stu-id="5eb82-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERROR\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-516">1901 (0x76D)</span><span class="sxs-lookup"><span data-stu-id="5eb82-516">1901 (0x76D)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-517">Указано недопустимое время.</span><span class="sxs-lookup"><span data-stu-id="5eb82-517">The specified time is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**Ошибка \_ недопустимого \_ \_ имени формы**</span><span class="sxs-lookup"><span data-stu-id="5eb82-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERROR\_INVALID\_FORM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-519">1902 (0x76E)</span><span class="sxs-lookup"><span data-stu-id="5eb82-519">1902 (0x76E)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-520">Указано недопустимое имя формы.</span><span class="sxs-lookup"><span data-stu-id="5eb82-520">The specified form name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**Ошибка \_ недопустимого \_ \_ размера формы**</span><span class="sxs-lookup"><span data-stu-id="5eb82-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERROR\_INVALID\_FORM\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-522">1903 (0x76F)</span><span class="sxs-lookup"><span data-stu-id="5eb82-522">1903 (0x76F)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-523">Указан недопустимый размер формы.</span><span class="sxs-lookup"><span data-stu-id="5eb82-523">The specified form size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**Ошибка \_ уже \_ ожидает выполнения**</span><span class="sxs-lookup"><span data-stu-id="5eb82-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERROR\_ALREADY\_WAITING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-525">1904 (0x770)</span><span class="sxs-lookup"><span data-stu-id="5eb82-525">1904 (0x770)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-526">Указанный обработчик принтера уже находится в ожидании.</span><span class="sxs-lookup"><span data-stu-id="5eb82-526">The specified printer handle is already being waited on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**\_принтер ошибок \_ удален**</span><span class="sxs-lookup"><span data-stu-id="5eb82-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERROR\_PRINTER\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-528">1905 (0x771)</span><span class="sxs-lookup"><span data-stu-id="5eb82-528">1905 (0x771)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-529">Указанный принтер удален.</span><span class="sxs-lookup"><span data-stu-id="5eb82-529">The specified printer has been deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**Ошибка \_ недопустимого \_ \_ состояния принтера**</span><span class="sxs-lookup"><span data-stu-id="5eb82-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERROR\_INVALID\_PRINTER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-531">1906 (0x772)</span><span class="sxs-lookup"><span data-stu-id="5eb82-531">1906 (0x772)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-532">Недопустимое состояние принтера.</span><span class="sxs-lookup"><span data-stu-id="5eb82-532">The state of the printer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**\_пароль ошибки \_ должен \_ измениться**</span><span class="sxs-lookup"><span data-stu-id="5eb82-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**ERROR\_PASSWORD\_MUST\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-534">1907 (0x773)</span><span class="sxs-lookup"><span data-stu-id="5eb82-534">1907 (0x773)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-535">Пароль пользователя необходимо изменить перед входом в систему.</span><span class="sxs-lookup"><span data-stu-id="5eb82-535">The user's password must be changed before signing in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**Ошибка \_ при \_ \_ \_ обнаружении контроллера домена**</span><span class="sxs-lookup"><span data-stu-id="5eb82-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**ERROR\_DOMAIN\_CONTROLLER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-537">1908 (0x774)</span><span class="sxs-lookup"><span data-stu-id="5eb82-537">1908 (0x774)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-538">Не удалось найти контроллер домена для этого домена.</span><span class="sxs-lookup"><span data-stu-id="5eb82-538">Could not find the domain controller for this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**\_учетная запись ошибки \_ заблокирована \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**ERROR\_ACCOUNT\_LOCKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-540">1909 (0x775)</span><span class="sxs-lookup"><span data-stu-id="5eb82-540">1909 (0x775)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-541">Учетная запись, на которую дана ссылка, заблокирована и не может быть зарегистрирована в.</span><span class="sxs-lookup"><span data-stu-id="5eb82-541">The referenced account is currently locked out and may not be logged on to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**ИЛИ \_ недопустимое \_ оксид**</span><span class="sxs-lookup"><span data-stu-id="5eb82-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OR\_INVALID\_OXID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-543">1910 (0x776)</span><span class="sxs-lookup"><span data-stu-id="5eb82-543">1910 (0x776)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-544">Указанный объект экспорта объектов не найден.</span><span class="sxs-lookup"><span data-stu-id="5eb82-544">The object exporter specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**ИЛИ \_ Недопустимый \_ OID**</span><span class="sxs-lookup"><span data-stu-id="5eb82-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OR\_INVALID\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-546">1911 (0x777)</span><span class="sxs-lookup"><span data-stu-id="5eb82-546">1911 (0x777)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-547">Указанный объект не найден.</span><span class="sxs-lookup"><span data-stu-id="5eb82-547">The object specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**ИЛИ \_ Недопустимый \_ набор**</span><span class="sxs-lookup"><span data-stu-id="5eb82-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OR\_INVALID\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-549">1912 (0x778)</span><span class="sxs-lookup"><span data-stu-id="5eb82-549">1912 (0x778)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-550">Указанный набор сопоставителя объектов не найден.</span><span class="sxs-lookup"><span data-stu-id="5eb82-550">The object resolver set specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**\_ \_ незавершенная отправка RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC\_S\_SEND\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-552">1913 (0x779)</span><span class="sxs-lookup"><span data-stu-id="5eb82-552">1913 (0x779)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-553">Некоторые данные будут отправлены в буфер запроса.</span><span class="sxs-lookup"><span data-stu-id="5eb82-553">Some data remains to be sent in the request buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**\_ \_ Недопустимый \_ асинхронный обработчик RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC\_S\_INVALID\_ASYNC\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-555">1914 (0x77A)</span><span class="sxs-lookup"><span data-stu-id="5eb82-555">1914 (0x77A)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-556">Недопустимый асинхронный обработчик вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="5eb82-556">Invalid asynchronous remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**\_ \_ Недопустимый \_ асинхронный вызов RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC\_S\_INVALID\_ASYNC\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-558">1915 (0x77B)</span><span class="sxs-lookup"><span data-stu-id="5eb82-558">1915 (0x77B)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-559">Недопустимый обработчик асинхронных вызовов RPC для этой операции.</span><span class="sxs-lookup"><span data-stu-id="5eb82-559">Invalid asynchronous RPC call handle for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**\_канал RPC \_ X \_ закрыт**</span><span class="sxs-lookup"><span data-stu-id="5eb82-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC\_X\_PIPE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-561">1916 (0x77C)</span><span class="sxs-lookup"><span data-stu-id="5eb82-561">1916 (0x77C)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-562">Объект канала RPC уже закрыт.</span><span class="sxs-lookup"><span data-stu-id="5eb82-562">The RPC pipe object has already been closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**\_ \_ \_ Ошибка дисциплины канала RPC X \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC\_X\_PIPE\_DISCIPLINE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-564">1917 (0x77D)</span><span class="sxs-lookup"><span data-stu-id="5eb82-564">1917 (0x77D)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-565">Вызов RPC завершен до обработки всех каналов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-565">The RPC call completed before all pipes were processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**\_канал RPC \_ X \_ пуст**</span><span class="sxs-lookup"><span data-stu-id="5eb82-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC\_X\_PIPE\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-567">1918 (0x77E)</span><span class="sxs-lookup"><span data-stu-id="5eb82-567">1918 (0x77E)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-568">Больше нет доступных данных из канала RPC.</span><span class="sxs-lookup"><span data-stu-id="5eb82-568">No more data is available from the RPC pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**Ошибка \_ No \_ SITENAME**</span><span class="sxs-lookup"><span data-stu-id="5eb82-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERROR\_NO\_SITENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-570">1919 (0x77F)</span><span class="sxs-lookup"><span data-stu-id="5eb82-570">1919 (0x77F)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-571">Для этого компьютера нет доступных имен сайтов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-571">No site name is available for this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ОШИБКА не \_ удается \_ получить доступ к \_ файлу**</span><span class="sxs-lookup"><span data-stu-id="5eb82-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERROR\_CANT\_ACCESS\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-573">1920 (0x780)</span><span class="sxs-lookup"><span data-stu-id="5eb82-573">1920 (0x780)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-574">Системе не удается получить доступ к файлу.</span><span class="sxs-lookup"><span data-stu-id="5eb82-574">The file cannot be accessed by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ОШИБКА не \_ удается \_ Разрешить \_ имя файла**</span><span class="sxs-lookup"><span data-stu-id="5eb82-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERROR\_CANT\_RESOLVE\_FILENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-576">1921 (0x781)</span><span class="sxs-lookup"><span data-stu-id="5eb82-576">1921 (0x781)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-577">Имя файла не может быть разрешено системой.</span><span class="sxs-lookup"><span data-stu-id="5eb82-577">The name of the file cannot be resolved by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**\_несоответствие \_ типа записи RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**RPC\_S\_ENTRY\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-579">1922 (0x782)</span><span class="sxs-lookup"><span data-stu-id="5eb82-579">1922 (0x782)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-580">Тип записи отличается от ожидаемого.</span><span class="sxs-lookup"><span data-stu-id="5eb82-580">The entry is not of the expected type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**\_ \_ не \_ все \_ OBJ-файлы \_ экспортированы в RPC S**</span><span class="sxs-lookup"><span data-stu-id="5eb82-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-582">1923 (0x783)</span><span class="sxs-lookup"><span data-stu-id="5eb82-582">1923 (0x783)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-583">Не все UUID объекта можно экспортировать в указанную запись.</span><span class="sxs-lookup"><span data-stu-id="5eb82-583">Not all object UUIDs could be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_интерфейс RPC \_ S \_ не \_ экспортирован**</span><span class="sxs-lookup"><span data-stu-id="5eb82-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**RPC\_S\_INTERFACE\_NOT\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-585">1924 (0x784)</span><span class="sxs-lookup"><span data-stu-id="5eb82-585">1924 (0x784)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-586">Не удалось экспортировать интерфейс в указанную запись.</span><span class="sxs-lookup"><span data-stu-id="5eb82-586">Interface could not be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_профиль RPC \_ S \_ не \_ добавлен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**RPC\_S\_PROFILE\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-588">1925 (0x785)</span><span class="sxs-lookup"><span data-stu-id="5eb82-588">1925 (0x785)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-589">Не удалось добавить указанную запись профиля.</span><span class="sxs-lookup"><span data-stu-id="5eb82-589">The specified profile entry could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**удаленное \_ ELT RPC S \_ \_ \_ не \_ Добавлено**</span><span class="sxs-lookup"><span data-stu-id="5eb82-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC\_S\_PRF\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-591">1926 (0x786)</span><span class="sxs-lookup"><span data-stu-id="5eb82-591">1926 (0x786)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-592">Не удалось добавить указанный элемент профиля.</span><span class="sxs-lookup"><span data-stu-id="5eb82-592">The specified profile element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**\_ \_ \_ \_ не \_ удалено ELT RPC с PRF**</span><span class="sxs-lookup"><span data-stu-id="5eb82-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC\_S\_PRF\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-594">1927 (0x787)</span><span class="sxs-lookup"><span data-stu-id="5eb82-594">1927 (0x787)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-595">Не удалось удалить указанный элемент профиля.</span><span class="sxs-lookup"><span data-stu-id="5eb82-595">The specified profile element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC \_ S \_ GRP \_ ELT \_ не \_ добавлен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC\_S\_GRP\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-597">1928 (0x788)</span><span class="sxs-lookup"><span data-stu-id="5eb82-597">1928 (0x788)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-598">Не удалось добавить элемент Group.</span><span class="sxs-lookup"><span data-stu-id="5eb82-598">The group element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**\_ \_ \_ \_ не \_ удалено ELT для RPC S GRP**</span><span class="sxs-lookup"><span data-stu-id="5eb82-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC\_S\_GRP\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-600">1929 (0x789)</span><span class="sxs-lookup"><span data-stu-id="5eb82-600">1929 (0x789)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-601">Не удалось удалить элемент группы.</span><span class="sxs-lookup"><span data-stu-id="5eb82-601">The group element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**Ошибка \_ \_ заблокирована драйвером на км \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERROR\_KM\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-603">1930 (0x78A)</span><span class="sxs-lookup"><span data-stu-id="5eb82-603">1930 (0x78A)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-604">Драйвер принтера несовместим с политикой, включенной на компьютере, которая блокирует драйверы NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="5eb82-604">The printer driver is not compatible with a policy enabled on your computer that blocks NT 4.0 drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**\_ \_ срок действия контекста ошибки истек**</span><span class="sxs-lookup"><span data-stu-id="5eb82-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**ERROR\_CONTEXT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-606">1931 (0x78B)</span><span class="sxs-lookup"><span data-stu-id="5eb82-606">1931 (0x78B)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-607">Срок действия контекста истек, и его больше нельзя использовать.</span><span class="sxs-lookup"><span data-stu-id="5eb82-607">The context has expired and can no longer be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**\_ \_ \_ \_ превышена квота доверия на пользователя (Error) \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERROR\_PER\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-609">1932 (0x78C)</span><span class="sxs-lookup"><span data-stu-id="5eb82-609">1932 (0x78C)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-610">Превышена квота на создание делегированного доверия текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="5eb82-610">The current user's delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**Ошибка \_ \_ \_ \_ превышения квоты доверия для всех пользователей \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERROR\_ALL\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-612">1933 (0x78D)</span><span class="sxs-lookup"><span data-stu-id="5eb82-612">1933 (0x78D)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-613">Общая квота на создание делегированного доверия была превышена.</span><span class="sxs-lookup"><span data-stu-id="5eb82-613">The total delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**Ошибка \_ при \_ удалении \_ пользователем \_ превышения квоты доверия \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERROR\_USER\_DELETE\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-615">1934 (0x78E)</span><span class="sxs-lookup"><span data-stu-id="5eb82-615">1934 (0x78E)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-616">Превышена квота на удаление делегированного доверия текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="5eb82-616">The current user's delegated trust deletion quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**Ошибка \_ при проверке подлинности \_ брандмауэра \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERROR\_AUTHENTICATION\_FIREWALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-618">1935 (0x78F)</span><span class="sxs-lookup"><span data-stu-id="5eb82-618">1935 (0x78F)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-619">Компьютер, на который вы входите в систему, защищен брандмауэром проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5eb82-619">The computer you are signing into is protected by an authentication firewall.</span></span> <span data-ttu-id="5eb82-620">Указанная учетная запись не может пройти проверку подлинности на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5eb82-620">The specified account is not allowed to authenticate to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**Ошибка \_ \_ \_ заблокированных подключений удаленной печати \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERROR\_REMOTE\_PRINT\_CONNECTIONS\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-622">1936 (0x790)</span><span class="sxs-lookup"><span data-stu-id="5eb82-622">1936 (0x790)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-623">Удаленные подключения к диспетчеру очереди печати блокируются политикой, заданной на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5eb82-623">Remote connections to the Print Spooler are blocked by a policy set on your machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**Ошибка \_ NTLM \_ заблокирована**</span><span class="sxs-lookup"><span data-stu-id="5eb82-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERROR\_NTLM\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-625">1937 (0x791)</span><span class="sxs-lookup"><span data-stu-id="5eb82-625">1937 (0x791)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-626">Проверка подлинности не удалась, так как проверка подлинности NTLM отключена.</span><span class="sxs-lookup"><span data-stu-id="5eb82-626">Authentication failed because NTLM authentication has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**\_ \_ требуется изменение пароля при ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ERROR\_PASSWORD\_CHANGE\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-628">1938 (0x792)</span><span class="sxs-lookup"><span data-stu-id="5eb82-628">1938 (0x792)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-629">Ошибка входа. Политика EAS требует, чтобы пользователь изменил свой пароль перед выполнением этой операции.</span><span class="sxs-lookup"><span data-stu-id="5eb82-629">Logon Failure: EAS policy requires that the user change their password before this operation can be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**Ошибка \_ недопустимого \_ \_ формата пикселей**</span><span class="sxs-lookup"><span data-stu-id="5eb82-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERROR\_INVALID\_PIXEL\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-631">2000 (0x7D0)</span><span class="sxs-lookup"><span data-stu-id="5eb82-631">2000 (0x7D0)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-632">Недопустимый формат пикселей.</span><span class="sxs-lookup"><span data-stu-id="5eb82-632">The pixel format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**Ошибка \_ неправильный \_ драйвер**</span><span class="sxs-lookup"><span data-stu-id="5eb82-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERROR\_BAD\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-634">2001 (0x7D1)</span><span class="sxs-lookup"><span data-stu-id="5eb82-634">2001 (0x7D1)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-635">Указан недопустимый драйвер.</span><span class="sxs-lookup"><span data-stu-id="5eb82-635">The specified driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**Ошибка \_ недопустимого \_ \_ стиля окна**</span><span class="sxs-lookup"><span data-stu-id="5eb82-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERROR\_INVALID\_WINDOW\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-637">2002 (0x7D2)</span><span class="sxs-lookup"><span data-stu-id="5eb82-637">2002 (0x7D2)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-638">Недопустимый атрибут стиля окна или класса для этой операции.</span><span class="sxs-lookup"><span data-stu-id="5eb82-638">The window style or class attribute is invalid for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**\_МЕТАФАЙЛ ошибок \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="5eb82-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERROR\_METAFILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-640">2003 (0x7D3)</span><span class="sxs-lookup"><span data-stu-id="5eb82-640">2003 (0x7D3)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-641">Запрошенная операция с метафайлами не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-641">The requested metafile operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**\_Преобразование ошибок \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="5eb82-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**ERROR\_TRANSFORM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-643">2004 (0x7D4)</span><span class="sxs-lookup"><span data-stu-id="5eb82-643">2004 (0x7D4)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-644">Запрошенная операция преобразования не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-644">The requested transformation operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**\_Обрезка ошибки \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="5eb82-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**ERROR\_CLIPPING\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-646">2005 (0x7D5)</span><span class="sxs-lookup"><span data-stu-id="5eb82-646">2005 (0x7D5)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-647">Запрошенная операция обрезки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5eb82-647">The requested clipping operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**Ошибка \_ недопустимого модуля \_ CMM**</span><span class="sxs-lookup"><span data-stu-id="5eb82-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERROR\_INVALID\_CMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-649">2010 (0x7DA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-649">2010 (0x7DA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-650">Указан недопустимый модуль управления цветом.</span><span class="sxs-lookup"><span data-stu-id="5eb82-650">The specified color management module is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**Ошибка при \_ недопустимом \_ профиле**</span><span class="sxs-lookup"><span data-stu-id="5eb82-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERROR\_INVALID\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-652">2011 (0x7DB)</span><span class="sxs-lookup"><span data-stu-id="5eb82-652">2011 (0x7DB)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-653">Указан недопустимый цветовой профиль.</span><span class="sxs-lookup"><span data-stu-id="5eb82-653">The specified color profile is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**\_тег ошибки \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="5eb82-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**ERROR\_TAG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-655">2012 (0x7DC)</span><span class="sxs-lookup"><span data-stu-id="5eb82-655">2012 (0x7DC)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-656">Указанный тег не найден.</span><span class="sxs-lookup"><span data-stu-id="5eb82-656">The specified tag was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**\_тег ошибки \_ отсутствует \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**ERROR\_TAG\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-658">2013 (0x7DD)</span><span class="sxs-lookup"><span data-stu-id="5eb82-658">2013 (0x7DD)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-659">Отсутствует обязательный тег.</span><span class="sxs-lookup"><span data-stu-id="5eb82-659">A required tag is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**Ошибка \_ дублирования \_ тега**</span><span class="sxs-lookup"><span data-stu-id="5eb82-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERROR\_DUPLICATE\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-661">2014 (0x7DE)</span><span class="sxs-lookup"><span data-stu-id="5eb82-661">2014 (0x7DE)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-662">Указанный тег уже существует.</span><span class="sxs-lookup"><span data-stu-id="5eb82-662">The specified tag is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**\_профиль ошибок \_ не \_ связан \_ с \_ устройством**</span><span class="sxs-lookup"><span data-stu-id="5eb82-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-664">2015 (0x7DF)</span><span class="sxs-lookup"><span data-stu-id="5eb82-664">2015 (0x7DF)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-665">Указанный цветовой профиль не связан с указанным устройством.</span><span class="sxs-lookup"><span data-stu-id="5eb82-665">The specified color profile is not associated with the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**\_профиль ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="5eb82-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**ERROR\_PROFILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-667">2016 (0x7E0)</span><span class="sxs-lookup"><span data-stu-id="5eb82-667">2016 (0x7E0)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-668">Указанный цветовой профиль не найден.</span><span class="sxs-lookup"><span data-stu-id="5eb82-668">The specified color profile was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**Ошибка \_ недопустимого \_ колорспаце**</span><span class="sxs-lookup"><span data-stu-id="5eb82-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERROR\_INVALID\_COLORSPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-670">2017 (0x7E1)</span><span class="sxs-lookup"><span data-stu-id="5eb82-670">2017 (0x7E1)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-671">Указано недопустимое цветовое пространство.</span><span class="sxs-lookup"><span data-stu-id="5eb82-671">The specified color space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**Ошибка \_ ICM \_ не \_ включена**</span><span class="sxs-lookup"><span data-stu-id="5eb82-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERROR\_ICM\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-673">2018 (0x7E2)</span><span class="sxs-lookup"><span data-stu-id="5eb82-673">2018 (0x7E2)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-674">Управление цветом изображений не включено.</span><span class="sxs-lookup"><span data-stu-id="5eb82-674">Image Color Management is not enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**Ошибка при \_ удалении \_ ICM \_ XForm**</span><span class="sxs-lookup"><span data-stu-id="5eb82-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERROR\_DELETING\_ICM\_XFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-676">2019 (0x7E3)</span><span class="sxs-lookup"><span data-stu-id="5eb82-676">2019 (0x7E3)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-677">При удалении преобразования цветов произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5eb82-677">There was an error while deleting the color transform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**Ошибка \_ недопустимого \_ преобразования**</span><span class="sxs-lookup"><span data-stu-id="5eb82-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERROR\_INVALID\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-679">2020 (0x7E4)</span><span class="sxs-lookup"><span data-stu-id="5eb82-679">2020 (0x7E4)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-680">Указано недопустимое преобразование цвета.</span><span class="sxs-lookup"><span data-stu-id="5eb82-680">The specified color transform is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**Ошибка \_ колорспаце \_ несоответствие**</span><span class="sxs-lookup"><span data-stu-id="5eb82-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERROR\_COLORSPACE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-682">2021 (0x7E5)</span><span class="sxs-lookup"><span data-stu-id="5eb82-682">2021 (0x7E5)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-683">Указанное преобразование не соответствует цветовому пространству точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="5eb82-683">The specified transform does not match the bitmap's color space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**Ошибка \_ недопустимого \_ колориндекс**</span><span class="sxs-lookup"><span data-stu-id="5eb82-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERROR\_INVALID\_COLORINDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-685">2022 (0x7E6)</span><span class="sxs-lookup"><span data-stu-id="5eb82-685">2022 (0x7E6)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-686">Указанный именованный индекс цвета отсутствует в профиле.</span><span class="sxs-lookup"><span data-stu-id="5eb82-686">The specified named color index is not present in the profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**\_профиль ошибок \_ \_ не \_ соответствует \_ устройству**</span><span class="sxs-lookup"><span data-stu-id="5eb82-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**ERROR\_PROFILE\_DOES\_NOT\_MATCH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-688">2023 (0x7E7)</span><span class="sxs-lookup"><span data-stu-id="5eb82-688">2023 (0x7E7)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-689">Указанный профиль предназначен для устройства другого типа, отличного от указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="5eb82-689">The specified profile is intended for a device of a different type than the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**Ошибка \_ подключения к \_ другому \_ паролю**</span><span class="sxs-lookup"><span data-stu-id="5eb82-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-691">2108 (0x83C)</span><span class="sxs-lookup"><span data-stu-id="5eb82-691">2108 (0x83C)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-692">Сетевое подключение успешно установлено, но пользователю пришлось запрашивать пароль, отличный от указанного ранее.</span><span class="sxs-lookup"><span data-stu-id="5eb82-692">The network connection was made successfully, but the user had to be prompted for a password other than the one originally specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**Ошибка \_ подключения к \_ другому \_ паролю \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="5eb82-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-694">2109 (0x83D)</span><span class="sxs-lookup"><span data-stu-id="5eb82-694">2109 (0x83D)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-695">Сетевое подключение успешно установлено с использованием учетных данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5eb82-695">The network connection was made successfully using default credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**Ошибка \_ неправильного \_ имени пользователя**</span><span class="sxs-lookup"><span data-stu-id="5eb82-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERROR\_BAD\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-697">2202 (0x89A)</span><span class="sxs-lookup"><span data-stu-id="5eb82-697">2202 (0x89A)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-698">Указано недопустимое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="5eb82-698">The specified username is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**Ошибка \_ не \_ подключена**</span><span class="sxs-lookup"><span data-stu-id="5eb82-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERROR\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-700">2250 (0x8CA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-700">2250 (0x8CA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-701">Это сетевое подключение не существует.</span><span class="sxs-lookup"><span data-stu-id="5eb82-701">This network connection does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**Ошибка при \_ открытии \_ файлов**</span><span class="sxs-lookup"><span data-stu-id="5eb82-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERROR\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-703">2401 (0x961)</span><span class="sxs-lookup"><span data-stu-id="5eb82-703">2401 (0x961)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-704">Это сетевое подключение имеет открытые файлы или ожидающие запросы.</span><span class="sxs-lookup"><span data-stu-id="5eb82-704">This network connection has files open or requests pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ОШИБКИ \_ активных \_ подключений**</span><span class="sxs-lookup"><span data-stu-id="5eb82-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERROR\_ACTIVE\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-706">2402 (0x962)</span><span class="sxs-lookup"><span data-stu-id="5eb82-706">2402 (0x962)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-707">Активные соединения по-прежнему существуют.</span><span class="sxs-lookup"><span data-stu-id="5eb82-707">Active connections still exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_ \_ используемое устройство с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**ERROR\_DEVICE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-709">2404 (0x964)</span><span class="sxs-lookup"><span data-stu-id="5eb82-709">2404 (0x964)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-710">Устройство используется активным процессом и не может быть отключено.</span><span class="sxs-lookup"><span data-stu-id="5eb82-710">The device is in use by an active process and cannot be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**Ошибка \_ неизвестного \_ \_ монитора печати**</span><span class="sxs-lookup"><span data-stu-id="5eb82-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERROR\_UNKNOWN\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-712">3000 (0xBB8)</span><span class="sxs-lookup"><span data-stu-id="5eb82-712">3000 (0xBB8)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-713">Указанный монитор печати неизвестен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-713">The specified print monitor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**\_ \_ используется драйвер принтера \_ ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERROR\_PRINTER\_DRIVER\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-715">3001 (0xBB9)</span><span class="sxs-lookup"><span data-stu-id="5eb82-715">3001 (0xBB9)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-716">Указанный драйвер принтера сейчас используется.</span><span class="sxs-lookup"><span data-stu-id="5eb82-716">The specified printer driver is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**\_ \_ \_ не \_ найден файл очереди сообщений об ошибках**</span><span class="sxs-lookup"><span data-stu-id="5eb82-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERROR\_SPOOL\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-718">3002 (0xBBA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-718">3002 (0xBBA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-719">Файл очереди печати не найден.</span><span class="sxs-lookup"><span data-stu-id="5eb82-719">The spool file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**Ошибка \_ СПЛ \_ No \_ стартдок**</span><span class="sxs-lookup"><span data-stu-id="5eb82-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERROR\_SPL\_NO\_STARTDOC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-721">3003 (0xBBB)</span><span class="sxs-lookup"><span data-stu-id="5eb82-721">3003 (0xBBB)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-722">Вызов Стартдокпринтер не был выдан.</span><span class="sxs-lookup"><span data-stu-id="5eb82-722">A StartDocPrinter call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**Ошибка \_ СПЛ \_ No \_ ADDJOB**</span><span class="sxs-lookup"><span data-stu-id="5eb82-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERROR\_SPL\_NO\_ADDJOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-724">3004 (0xBBC)</span><span class="sxs-lookup"><span data-stu-id="5eb82-724">3004 (0xBBC)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-725">Вызов AddJob не был выдан.</span><span class="sxs-lookup"><span data-stu-id="5eb82-725">An AddJob call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**\_обработчик печати \_ ошибок \_ уже \_ установлен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERROR\_PRINT\_PROCESSOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-727">3005 (0xBBD)</span><span class="sxs-lookup"><span data-stu-id="5eb82-727">3005 (0xBBD)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-728">Указанный обработчик печати уже установлен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-728">The specified print processor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**монитор печати "ошибка" \_ \_ \_ уже \_ установлен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERROR\_PRINT\_MONITOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-730">3006 (0xBBE)</span><span class="sxs-lookup"><span data-stu-id="5eb82-730">3006 (0xBBE)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-731">Указанный монитор печати уже установлен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-731">The specified print monitor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**Ошибка при \_ неправильном \_ \_ мониторе печати**</span><span class="sxs-lookup"><span data-stu-id="5eb82-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERROR\_INVALID\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-733">3007 (0xBBF)</span><span class="sxs-lookup"><span data-stu-id="5eb82-733">3007 (0xBBF)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-734">Указанный монитор печати не имеет необходимых функций.</span><span class="sxs-lookup"><span data-stu-id="5eb82-734">The specified print monitor does not have the required functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**Ошибка \_ \_ использования монитора \_ печати \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERROR\_PRINT\_MONITOR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-736">3008 (0xBC0)</span><span class="sxs-lookup"><span data-stu-id="5eb82-736">3008 (0xBC0)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-737">Указанный монитор печати сейчас используется.</span><span class="sxs-lookup"><span data-stu-id="5eb82-737">The specified print monitor is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**на \_ принтере ошибок \_ есть \_ задания \_ в очереди**</span><span class="sxs-lookup"><span data-stu-id="5eb82-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERROR\_PRINTER\_HAS\_JOBS\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-739">3009 (0xBC1)</span><span class="sxs-lookup"><span data-stu-id="5eb82-739">3009 (0xBC1)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-740">Запрошенная операция не разрешена при наличии заданий в очереди принтера.</span><span class="sxs-lookup"><span data-stu-id="5eb82-740">The requested operation is not allowed when there are jobs queued to the printer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**Ошибка \_ " \_ требуется перезагрузка при успешном выполнении" \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERROR\_SUCCESS\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-742">3010 (0xBC2)</span><span class="sxs-lookup"><span data-stu-id="5eb82-742">3010 (0xBC2)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-743">Запрошенная операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5eb82-743">The requested operation is successful.</span></span> <span data-ttu-id="5eb82-744">Изменения вступят в силу только после перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="5eb82-744">Changes will not be effective until the system is rebooted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**Ошибка при \_ успешном \_ перезапуске \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERROR\_SUCCESS\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-746">3011 (0xBC3)</span><span class="sxs-lookup"><span data-stu-id="5eb82-746">3011 (0xBC3)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-747">Запрошенная операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5eb82-747">The requested operation is successful.</span></span> <span data-ttu-id="5eb82-748">Изменения вступят в силу только после перезапуска службы.</span><span class="sxs-lookup"><span data-stu-id="5eb82-748">Changes will not be effective until the service is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**\_принтер ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="5eb82-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERROR\_PRINTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-750">3012 (0xBC4)</span><span class="sxs-lookup"><span data-stu-id="5eb82-750">3012 (0xBC4)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-751">Принтеры не найдены.</span><span class="sxs-lookup"><span data-stu-id="5eb82-751">No printers were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**предупреждение об ОШИБКе \_ \_ драйвера принтера \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERROR\_PRINTER\_DRIVER\_WARNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-753">3013 (0xBC5)</span><span class="sxs-lookup"><span data-stu-id="5eb82-753">3013 (0xBC5)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-754">Известно, что драйвер принтера является ненадежным.</span><span class="sxs-lookup"><span data-stu-id="5eb82-754">The printer driver is known to be unreliable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**\_драйвер принтера \_ ошибок \_ заблокирован**</span><span class="sxs-lookup"><span data-stu-id="5eb82-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERROR\_PRINTER\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-756">3014 (0xBC6)</span><span class="sxs-lookup"><span data-stu-id="5eb82-756">3014 (0xBC6)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-757">Известно, что драйвер принтера наносит вред системе.</span><span class="sxs-lookup"><span data-stu-id="5eb82-757">The printer driver is known to harm the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**\_ \_ \_ используемый пакет драйверов \_ \_ принтера ошибок**</span><span class="sxs-lookup"><span data-stu-id="5eb82-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERROR\_PRINTER\_DRIVER\_PACKAGE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-759">3015 (0xBC7)</span><span class="sxs-lookup"><span data-stu-id="5eb82-759">3015 (0xBC7)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-760">Указанный пакет драйвера принтера в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="5eb82-760">The specified printer driver package is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**\_пакет основных \_ драйверов \_ ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="5eb82-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**ERROR\_CORE\_DRIVER\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-762">3016 (0xBC8)</span><span class="sxs-lookup"><span data-stu-id="5eb82-762">3016 (0xBC8)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-763">Не удалось найти основной пакет драйверов, необходимый для пакета драйверов принтера.</span><span class="sxs-lookup"><span data-stu-id="5eb82-763">Unable to find a core driver package that is required by the printer driver package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**Ошибка \_ при \_ перезагрузке не \_ требуется**</span><span class="sxs-lookup"><span data-stu-id="5eb82-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERROR\_FAIL\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-765">3017 (0xBC9)</span><span class="sxs-lookup"><span data-stu-id="5eb82-765">3017 (0xBC9)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-766">Не удалось выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="5eb82-766">The requested operation failed.</span></span> <span data-ttu-id="5eb82-767">Для отката внесенных изменений требуется перезагрузка системы.</span><span class="sxs-lookup"><span data-stu-id="5eb82-767">A system reboot is required to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**Ошибка \_ при \_ перезагрузке не удалось \_ запустить**</span><span class="sxs-lookup"><span data-stu-id="5eb82-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERROR\_FAIL\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-769">3018 (0xBCA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-769">3018 (0xBCA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-770">Не удалось выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="5eb82-770">The requested operation failed.</span></span> <span data-ttu-id="5eb82-771">Инициирована перезагрузка системы для отката внесенных изменений.</span><span class="sxs-lookup"><span data-stu-id="5eb82-771">A system reboot has been initiated to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**\_ \_ \_ требуется загрузка драйвера принтера \_ с ошибками**</span><span class="sxs-lookup"><span data-stu-id="5eb82-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERROR\_PRINTER\_DRIVER\_DOWNLOAD\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-773">3019 (0xBCB)</span><span class="sxs-lookup"><span data-stu-id="5eb82-773">3019 (0xBCB)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-774">Указанный драйвер принтера не найден в системе и должен быть загружен.</span><span class="sxs-lookup"><span data-stu-id="5eb82-774">The specified printer driver was not found on the system and needs to be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**Ошибка \_ при \_ \_ перезапуске задания печати \_**</span><span class="sxs-lookup"><span data-stu-id="5eb82-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERROR\_PRINT\_JOB\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-776">3020 (0xBCC)</span><span class="sxs-lookup"><span data-stu-id="5eb82-776">3020 (0xBCC)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-777">Не удалось напечатать запрошенное задание печати.</span><span class="sxs-lookup"><span data-stu-id="5eb82-777">The requested print job has failed to print.</span></span> <span data-ttu-id="5eb82-778">Обновление системы печати требует повторной отправки задания.</span><span class="sxs-lookup"><span data-stu-id="5eb82-778">A print system update requires the job to be resubmitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**Ошибка при \_ неправильном \_ \_ \_ манифесте драйвера принтера**</span><span class="sxs-lookup"><span data-stu-id="5eb82-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERROR\_INVALID\_PRINTER\_DRIVER\_MANIFEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-780">3021 (0xBCD)</span><span class="sxs-lookup"><span data-stu-id="5eb82-780">3021 (0xBCD)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-781">Драйвер принтера не содержит допустимого манифеста или содержит слишком много манифестов.</span><span class="sxs-lookup"><span data-stu-id="5eb82-781">The printer driver does not contain a valid manifest, or contains too many manifests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**\_принтер ошибок \_ не является \_ общим**</span><span class="sxs-lookup"><span data-stu-id="5eb82-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERROR\_PRINTER\_NOT\_SHAREABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-783">3022 (0xBCE)</span><span class="sxs-lookup"><span data-stu-id="5eb82-783">3022 (0xBCE)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-784">Указанный принтер не может быть общим.</span><span class="sxs-lookup"><span data-stu-id="5eb82-784">The specified printer cannot be shared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**запрос на ошибку \_ \_ приостановлен**</span><span class="sxs-lookup"><span data-stu-id="5eb82-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**ERROR\_REQUEST\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-786">3050 (0xBEA)</span><span class="sxs-lookup"><span data-stu-id="5eb82-786">3050 (0xBEA)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-787">Операция приостановлена.</span><span class="sxs-lookup"><span data-stu-id="5eb82-787">The operation was paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5eb82-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**Ошибка \_ ввода-вывода при ошибке \_ \_ в \_ кэше**</span><span class="sxs-lookup"><span data-stu-id="5eb82-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERROR\_IO\_REISSUE\_AS\_CACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb82-789">3950 (0xF6E)</span><span class="sxs-lookup"><span data-stu-id="5eb82-789">3950 (0xF6E)</span></span>
</dt> <dt>



<span data-ttu-id="5eb82-790">Повторите данную операцию в виде кэшированной операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="5eb82-790">Reissue the given operation as a cached IO operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="5eb82-791">Требования</span><span class="sxs-lookup"><span data-stu-id="5eb82-791">Requirements</span></span>



| <span data-ttu-id="5eb82-792">Требование</span><span class="sxs-lookup"><span data-stu-id="5eb82-792">Requirement</span></span> | <span data-ttu-id="5eb82-793">Значение</span><span class="sxs-lookup"><span data-stu-id="5eb82-793">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb82-794">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5eb82-794">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb82-795">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5eb82-795">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5eb82-796">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5eb82-796">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb82-797">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5eb82-797">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5eb82-798">Header</span><span class="sxs-lookup"><span data-stu-id="5eb82-798">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eb82-799"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb82-799"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eb82-800">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5eb82-800">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb82-801">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="5eb82-801">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




