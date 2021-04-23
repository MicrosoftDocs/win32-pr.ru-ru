---
title: Структура RAS_PORT_1 (Рассапи. h)
description: '\_Структура порта RAS \_ 1 содержит сведения о порте RAS.'
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS структуры RAS_PORT_1
- RAS — указатель структуры PRAS_PORT_1
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650376"
---
# <a name="ras_port_1-structure"></a><span data-ttu-id="c0eb5-105">\_Структура порта \_ 1 RAS</span><span class="sxs-lookup"><span data-stu-id="c0eb5-105">RAS\_PORT\_1 structure</span></span>

<span data-ttu-id="c0eb5-106">\[Эта версия структуры **порта RAS \_ \_ 1** не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-106">\[This version of the **RAS\_PORT\_1** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="c0eb5-107">Используйте более новый [**\_ порт RAS \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) , определенный в мпрапи. h.\]</span><span class="sxs-lookup"><span data-stu-id="c0eb5-107">Use the newer [**RAS\_PORT\_1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="c0eb5-108">Структура **\_ порта RAS \_ 1** содержит сведения о порте RAS.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-108">The **RAS\_PORT\_1** structure contains information about a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0eb5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0eb5-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a><span data-ttu-id="c0eb5-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c0eb5-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0eb5-111">**rasport0**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-111">**rasport0**</span></span>
</dt> <dd>

<span data-ttu-id="c0eb5-112">Указывает структуру [**\_ порта RAS \_ 0**](ras-port-0-str.md) , содержащую сведения о порте, например имя порта, имя удаленного пользователя, подключенного к порту, и т. д.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-112">Specifies a [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port, such as the name of the port, the name of the remote user connected to the port, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c0eb5-113">**линекондитион**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-113">**LineCondition**</span></span>
</dt> <dd>

<span data-ttu-id="c0eb5-114">Указывает состояние порта.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-114">Specifies the state of the port.</span></span> <span data-ttu-id="c0eb5-115">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-115">This member can be one of the following values.</span></span>



| <span data-ttu-id="c0eb5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c0eb5-116">Value</span></span>                                                                                                                                                                                            | <span data-ttu-id="c0eb5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c0eb5-117">Meaning</span></span>                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <span data-ttu-id="c0eb5-118"><dt>**\_порт RAS \_ не \_ работает**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-118"><dt>**RAS\_PORT\_NON\_OPERATIONAL**</dt></span></span> </dl> | <span data-ttu-id="c0eb5-119">Порт неработоспособен.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-119">The port is not operational.</span></span> <span data-ttu-id="c0eb5-120">Проверьте журнал событий на наличие ошибок, о которых сообщает сервер.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-120">Check the event log for errors reported by the server.</span></span><br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <span data-ttu-id="c0eb5-121"><dt>**\_порт RAS \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-121"><dt>**RAS\_PORT\_DISCONNECTED**</dt></span></span> </dl>           | <span data-ttu-id="c0eb5-122">Порт в данный момент отключен.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-122">The port is currently disconnected.</span></span><br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <span data-ttu-id="c0eb5-123"><dt>**\_ \_ обратный вызов порта \_ RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-123"><dt>**RAS\_PORT\_CALLING\_BACK**</dt></span></span> </dl>          | <span data-ttu-id="c0eb5-124">Сервер RAS вызывает обратный вызов клиента RAS.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-124">The RAS server is calling back the RAS client.</span></span><br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <span data-ttu-id="c0eb5-125"><dt>**\_ \_ прослушивание порта RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-125"><dt>**RAS\_PORT\_LISTENING**</dt></span></span> </dl>                    | <span data-ttu-id="c0eb5-126">Порт ожидает вызова клиентом.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-126">The port is waiting for a client to call in.</span></span><br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <span data-ttu-id="c0eb5-127"><dt>**\_ \_ Проверка подлинности порта RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-127"><dt>**RAS\_PORT\_AUTHENTICATING**</dt></span></span> </dl>     | <span data-ttu-id="c0eb5-128">Сервер находится в процессе проверки подлинности удаленного клиента.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-128">The server is in the process of authenticating the remote client.</span></span><br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <span data-ttu-id="c0eb5-129"><dt>**\_ \_ Проверка подлинности порта RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-129"><dt>**RAS\_PORT\_AUTHENTICATED**</dt></span></span> </dl>        | <span data-ttu-id="c0eb5-130">Удаленный клиент теперь прошел проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-130">The remote client is now authenticated.</span></span><br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <span data-ttu-id="c0eb5-131"><dt>**\_ \_ Инициализация порта RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-131"><dt>**RAS\_PORT\_INITIALIZING**</dt></span></span> </dl>           | <span data-ttu-id="c0eb5-132">Устройство, подключенное к порту, инициализируется.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-132">The device attached to the port is being initialized.</span></span> <span data-ttu-id="c0eb5-133">Состояние порта изменится на порт RAS, \_ \_ прослушиваемый по завершении инициализации.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-133">The state of the port will change to RAS\_PORT\_LISTENING when the initialization has been completed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c0eb5-134">**хардварекондитион**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-134">**HardwareCondition**</span></span>
</dt> <dd>

<span data-ttu-id="c0eb5-135">Задает одно из следующих значений для указания состояния устройства, подключенного к порту.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-135">Specifies one of the following values to indicate the state of the device attached to the port.</span></span>



| <span data-ttu-id="c0eb5-136">Значение</span><span class="sxs-lookup"><span data-stu-id="c0eb5-136">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="c0eb5-137">Значение</span><span class="sxs-lookup"><span data-stu-id="c0eb5-137">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <span data-ttu-id="c0eb5-138"><dt>**\_работоспособность модема RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-138"><dt>**RAS\_MODEM\_OPERATIONAL**</dt></span></span> </dl>                 | <span data-ttu-id="c0eb5-139">Модем, подключенный к этому порту, является работоспособным и готов к приему клиентских вызовов.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-139">The modem attached to this port is operational and is ready to receive client calls.</span></span><br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <span data-ttu-id="c0eb5-140"><dt>**\_ \_ сбой аппаратного обеспечения МОДЕМа RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-140"><dt>**RAS\_MODEM\_HARDWARE\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="c0eb5-141">У модема, подключенного к этому порту, возникла проблема с оборудованием.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-141">The modem attached to this port has a hardware problem.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="c0eb5-142">**линеспид**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-142">**LineSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="c0eb5-143">Указывает скорость (в битах в секунду), с которой компьютер может обмениваться данными с портом.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-143">Specifies the speed, in bits per second, with which the computer can communicate with the port.</span></span>

</dd> <dt>

<span data-ttu-id="c0eb5-144">**нумстатистикс**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-144">**NumStatistics**</span></span>
</dt> <dd>

<span data-ttu-id="c0eb5-145">Этот элемент не используется.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-145">This member is not used.</span></span> <span data-ttu-id="c0eb5-146">Функции администрирования RAS, такие как функция [**расадминпортжетинфо**](rasadminportgetinfo.md) , используют структуру [**\_ \_ статистики порта RAS**](ras-port-statistics-str.md) для получения статистики порта.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-146">The RAS administration functions, such as the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function, use the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure to return port statistics.</span></span>

</dd> <dt>

<span data-ttu-id="c0eb5-147">**нуммедиапармс**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-147">**NumMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="c0eb5-148">Указывает число параметров для этого порта, характерных для носителя.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-148">Specifies the number of media-specific parameters for this port.</span></span> <span data-ttu-id="c0eb5-149">Для последовательного носителя это обычно число значений, которые отображаются в файле SERIAL.INI.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-149">For serial media this is typically the number of values that appear in the SERIAL.INI file.</span></span>

</dd> <dt>

<span data-ttu-id="c0eb5-150">**сиземедиапармс**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-150">**SizeMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="c0eb5-151">Указывает размер (в байтах) буфера, необходимого для всех параметров, относящихся к носителю.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-151">Specifies the size, in bytes, of the buffer required for all media-specific parameters.</span></span> <span data-ttu-id="c0eb5-152">Функция [**расадминпортжетинфо**](rasadminportgetinfo.md) возвращает буфер, содержащий массив [**\_ параметров RAS**](ras-parameters-str.md) с параметрами носителя и значениями для порта.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-152">The [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function returns a buffer that contains an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures with the media parameters and values for the port.</span></span>

</dd> <dt>

<span data-ttu-id="c0eb5-153">**прожресулт**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-153">**ProjResult**</span></span>
</dt> <dd>

<span data-ttu-id="c0eb5-154">Структура [**\_ \_ \_ результата проекции PPP для RAS**](ras-ppp-projection-result-str.md) , указывающая сведения о проекции PPP для этого порта.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-154">A [**RAS\_PPP\_PROJECTION\_RESULT**](ras-ppp-projection-result-str.md) structure that specifies the PPP projection information for this port.</span></span> <span data-ttu-id="c0eb5-155">Эта структура предоставляет сведения для каждого протокола, который согласовывается при подключении клиента удаленного доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="c0eb5-155">This structure provides information for each protocol that is negotiated when a RAS client connects to a server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0eb5-156">Требования</span><span class="sxs-lookup"><span data-stu-id="c0eb5-156">Requirements</span></span>



| <span data-ttu-id="c0eb5-157">Требование</span><span class="sxs-lookup"><span data-stu-id="c0eb5-157">Requirement</span></span> | <span data-ttu-id="c0eb5-158">Значение</span><span class="sxs-lookup"><span data-stu-id="c0eb5-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c0eb5-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0eb5-159">Minimum supported client</span></span><br/> | <span data-ttu-id="c0eb5-160">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c0eb5-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c0eb5-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0eb5-161">Minimum supported server</span></span><br/> | <span data-ttu-id="c0eb5-162">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c0eb5-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c0eb5-163">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c0eb5-163">End of client support</span></span><br/>    | <span data-ttu-id="c0eb5-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0eb5-164">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="c0eb5-165">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c0eb5-165">End of server support</span></span><br/>    | <span data-ttu-id="c0eb5-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0eb5-166">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="c0eb5-167">Header</span><span class="sxs-lookup"><span data-stu-id="c0eb5-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0eb5-168"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb5-168"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0eb5-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0eb5-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0eb5-170">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="c0eb5-170">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="c0eb5-171">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="c0eb5-171">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="c0eb5-172">**\_Параметры RAS**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-172">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="c0eb5-173">**\_Порт RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-173">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="c0eb5-174">**\_Статистика порта \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-174">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="c0eb5-175">**\_ \_ результат проекции PPP для RAS \_**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-175">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="c0eb5-176">**расадминакцептневконнектион**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-176">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="c0eb5-177">**расадминконнектионхангупнотификатион**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-177">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="c0eb5-178">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="c0eb5-178">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





