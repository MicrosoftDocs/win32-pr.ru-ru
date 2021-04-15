---
title: Режим ядра SSL
description: Режим ядра SSL
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- Режим ядра SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661639"
---
# <a name="kernel-mode-ssl"></a><span data-ttu-id="831a0-104">Режим ядра SSL</span><span class="sxs-lookup"><span data-stu-id="831a0-104">Kernel Mode SSL</span></span>

<span data-ttu-id="831a0-105">Режим ядра SSL появился в Windows Server 2003 с пакетом обновления 1 (SP1) с ограниченной поддержкой.</span><span class="sxs-lookup"><span data-stu-id="831a0-105">Kernel mode SSL was introduced in Windows Server 2003 with Service Pack 1 (SP1) with limited support.</span></span> <span data-ttu-id="831a0-106">Для компьютеров под управлением Windows Server 2003 с пакетом обновления 1 (SP1) необходимо установить раздел реестра, чтобы включить SSL ядра.</span><span class="sxs-lookup"><span data-stu-id="831a0-106">For computers running on Windows Server 2003 with SP1 a registry key must be set to enable kernel SSL.</span></span> <span data-ttu-id="831a0-107">Для компьютеров под управлением Windows Server 2008 и Windows Vista предоставляется полная поддержка режима ядра SSL.</span><span class="sxs-lookup"><span data-stu-id="831a0-107">For computers running on Windows Server 2008 and Windows Vista, full kernel mode support for SSL is provided.</span></span>

<span data-ttu-id="831a0-108">В следующих разделах описывается поддержка SSL в режиме ядра:</span><span class="sxs-lookup"><span data-stu-id="831a0-108">The following sections describe kernel mode SSL support:</span></span>

-   <span data-ttu-id="831a0-109">Режимы ядра SSL в Windows Server 2003 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="831a0-109">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>
-   <span data-ttu-id="831a0-110">Режим ядра SSL в Windows Server 2008 и Windows Vista</span><span class="sxs-lookup"><span data-stu-id="831a0-110">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a><span data-ttu-id="831a0-111">Режимы ядра SSL в Windows Server 2003 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="831a0-111">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>

<span data-ttu-id="831a0-112">В Windows Server 2003 с пакетом обновления 1 (SP1) API HTTP-сервера предоставляет возможность запуска безопасности SSL в режиме ядра (по умолчанию используется SSL в пользовательском режиме).</span><span class="sxs-lookup"><span data-stu-id="831a0-112">In Windows Server 2003 with SP1, HTTP Server API provides the option of running SSL security in kernel mode (user mode SSL is the default).</span></span> <span data-ttu-id="831a0-113">Режим ядра повышает производительность SSL за счет перемещения операций шифрования и расшифровки в ядро, уменьшая число переходов между режимом ядра и пользовательским режимом.</span><span class="sxs-lookup"><span data-stu-id="831a0-113">The kernel mode feature improves SSL performance by moving encryption and decryption operations to the kernel, thus reducing the number of transitions between kernel mode and user mode.</span></span>

<span data-ttu-id="831a0-114">Следующие функции не поддерживаются при запуске SSL в режиме ядра:</span><span class="sxs-lookup"><span data-stu-id="831a0-114">The following features are not supported when SSL is run in kernel mode:</span></span>

-   <span data-ttu-id="831a0-115">Client certificates</span><span class="sxs-lookup"><span data-stu-id="831a0-115">Client certificates</span></span>
-   <span data-ttu-id="831a0-116">Шифры RC2</span><span class="sxs-lookup"><span data-stu-id="831a0-116">RC2 ciphers</span></span>
-   <span data-ttu-id="831a0-117">Протокол PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="831a0-117">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="831a0-118">Изменение конфигурации сертификата сервера требует перезапуска службы HTTP</span><span class="sxs-lookup"><span data-stu-id="831a0-118">Server certificate configuration changes require a restart of the HTTP service</span></span>
-   <span data-ttu-id="831a0-119">Поддержка множественного шифрования и разгрузки</span><span class="sxs-lookup"><span data-stu-id="831a0-119">Bulk encryption and offload support</span></span>

## <a name="configuring-kernel-mode-ssl"></a><span data-ttu-id="831a0-120">Настройка режима ядра SSL</span><span class="sxs-lookup"><span data-stu-id="831a0-120">Configuring Kernel Mode SSL</span></span>

<span data-ttu-id="831a0-121">Режим ядра SSL управляется параметром реестра **енаблекернелссл** и включается путем установки значения 1.</span><span class="sxs-lookup"><span data-stu-id="831a0-121">Kernel mode SSL is controlled by the **EnableKernelSSL** registry value and is enabled by setting the value to 1.</span></span> <span data-ttu-id="831a0-122">Включение режима ядра SSL отключит пользовательский режим SSL и требует перезапуска службы HTTP для вступления в силу.</span><span class="sxs-lookup"><span data-stu-id="831a0-122">Enabling kernel mode SSL will disable user mode SSL and requires the HTTP service to be restarted to take effect.</span></span> <span data-ttu-id="831a0-123">Раздел реестра **енаблекернелссл** находится по адресу:</span><span class="sxs-lookup"><span data-stu-id="831a0-123">The **EnableKernelSSL** registry key is located at:</span></span>

<span data-ttu-id="831a0-124">**HKey \_ \_** Параметры HTTP для локальной \\ **системы** \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **енаблекернелссл**</span><span class="sxs-lookup"><span data-stu-id="831a0-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**HTTP**\\**Parameters**\\**EnableKernelSSL**</span></span>

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a><span data-ttu-id="831a0-125">Режим ядра SSL в Windows Server 2008 и Windows Vista</span><span class="sxs-lookup"><span data-stu-id="831a0-125">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

<span data-ttu-id="831a0-126">Для компьютеров, работающих под управлением Windows Server 2008 и Windows Vista, API сервера HTTP включает расширенные функции SSL.</span><span class="sxs-lookup"><span data-stu-id="831a0-126">For computers running on Windows Server 2008 and Windows Vista, the HTTP Server API features enhanced SSL functionality.</span></span>

<span data-ttu-id="831a0-127">Поддерживаются следующие новые возможности:</span><span class="sxs-lookup"><span data-stu-id="831a0-127">The following new features are supported:</span></span>

-   <span data-ttu-id="831a0-128">Полная поддержка сертификата клиента в режиме ядра SSL</span><span class="sxs-lookup"><span data-stu-id="831a0-128">Full client certificate support in kernel mode SSL</span></span>
-   <span data-ttu-id="831a0-129">Режим ядра SSL для всех HTTP-транзакций SSL</span><span class="sxs-lookup"><span data-stu-id="831a0-129">Kernel mode SSL for all HTTP SSL transactions</span></span>
-   <span data-ttu-id="831a0-130">Поддержка множественного шифрования и разгрузки</span><span class="sxs-lookup"><span data-stu-id="831a0-130">Bulk encryption and offload support</span></span>
-   <span data-ttu-id="831a0-131">Протокол PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="831a0-131">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="831a0-132">Шифры RC2</span><span class="sxs-lookup"><span data-stu-id="831a0-132">RC2 ciphers</span></span>
-   <span data-ttu-id="831a0-133">Повышенная производительность в пользовательском режиме SSL</span><span class="sxs-lookup"><span data-stu-id="831a0-133">Increased performance over user mode SSL</span></span>

## <a name="configuration"></a><span data-ttu-id="831a0-134">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="831a0-134">Configuration</span></span>

<span data-ttu-id="831a0-135">Режим ядра SSL можно настроить с помощью двух значений реестра в разделе параметров HTTP, расположенном по адресу:</span><span class="sxs-lookup"><span data-stu-id="831a0-135">Kernel mode SSL is configurable through two registry values under the HTTP Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

<span data-ttu-id="831a0-136">Пользователь должен иметь права администратора или локальной системы, чтобы изменить значения реестра, а также просмотреть или изменить файлы журнала и папку, в которой они находятся.</span><span class="sxs-lookup"><span data-stu-id="831a0-136">A user must have Administrator/Local System privileges to modify the registry values and view, or modify, the log files and the folder that contains them.</span></span>

<span data-ttu-id="831a0-137">Сведения о конфигурации в значениях реестра считываются при запуске драйвера API сервера HTTP.</span><span class="sxs-lookup"><span data-stu-id="831a0-137">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="831a0-138">В результате, если параметры изменены, драйвер должен быть остановлен и перезапущен для считывания новых значений.</span><span class="sxs-lookup"><span data-stu-id="831a0-138">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="831a0-139">Это можно сделать с помощью следующих команд консоли:</span><span class="sxs-lookup"><span data-stu-id="831a0-139">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="831a0-140">**NET останавливает HTTP**</span><span class="sxs-lookup"><span data-stu-id="831a0-140">**net stop http**</span></span>

<span data-ttu-id="831a0-141">**NET start http**</span><span class="sxs-lookup"><span data-stu-id="831a0-141">**net start http**</span></span>

<span data-ttu-id="831a0-142">В следующей таблице перечислены значения конфигурации реестра.</span><span class="sxs-lookup"><span data-stu-id="831a0-142">The following table lists registry configuration values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="831a0-143">Значение реестра</span><span class="sxs-lookup"><span data-stu-id="831a0-143">Registry Value</span></span></th>
<th><span data-ttu-id="831a0-144">Описание</span><span class="sxs-lookup"><span data-stu-id="831a0-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="831a0-145">енаблекернелссл</span><span class="sxs-lookup"><span data-stu-id="831a0-145">EnableKernelSSL</span></span></td>
<td><span data-ttu-id="831a0-146"><strong>Windows Server 2008 и Windows Vista:</strong> Это значение реестра устарело.</span><span class="sxs-lookup"><span data-stu-id="831a0-146"><strong>Windows Server 2008 and Windows Vista:</strong> This registry value is obsolete.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="831a0-147">енаблесслклосенотифи</span><span class="sxs-lookup"><span data-stu-id="831a0-147">EnableSslCloseNotify</span></span></td>
<td><span data-ttu-id="831a0-148">Значение <strong>типа DWORD</strong> , равное <strong>true</strong> , чтобы включить функцию Close-notify, или <strong>false</strong> , чтобы отключить требование Close-notify.</span><span class="sxs-lookup"><span data-stu-id="831a0-148">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable close-notify, or <strong>FALSE</strong> to disable the close-notify requirement.</span></span> <span data-ttu-id="831a0-149">По умолчанию Close — notify отключен.</span><span class="sxs-lookup"><span data-stu-id="831a0-149">Close-notify is disabled by default.</span></span><br/> <span data-ttu-id="831a0-150">Если параметр Close-notify включен, клиентское приложение должно отправить сообщение Close (уведомление) перед закрытием TCP-подключений.</span><span class="sxs-lookup"><span data-stu-id="831a0-150">When close-notify is enabled, the client application is required to send a close-notify message before closing TCP connections.</span></span> <span data-ttu-id="831a0-151">API-интерфейс сервера HTTP также отправляет запрос Close — notify перед закрытием соединения.</span><span class="sxs-lookup"><span data-stu-id="831a0-151">The HTTP Server API also sends a close-notify before closing the connection.</span></span><br/> <span data-ttu-id="831a0-152">Если функция Close-notify включена и клиент отправляет сообщение Close-notify, то API HTTP-сервера будет повторно использовать сеанс SSL при последующих подключениях к клиенту.</span><span class="sxs-lookup"><span data-stu-id="831a0-152">When close-notify is enabled, and the client sends a close-notify message, the HTTP Server API will reuse the SSL session on future connections to the client.</span></span> <span data-ttu-id="831a0-153">Если клиент не отправляет сообщение Close-notify, API сервера HTTP не будет повторно использовать тот же сеанс SSL для будущих соединений.</span><span class="sxs-lookup"><span data-stu-id="831a0-153">If the client does not send a close-notify, the HTTP Server API will not reuse the same SSL session on future connections.</span></span> <span data-ttu-id="831a0-154">Таким образом, для нового подключения активируется полное подтверждение SSL, что снижает производительность.</span><span class="sxs-lookup"><span data-stu-id="831a0-154">Thus, a full SSL handshake is triggered on the new connection thereby reducing performance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="831a0-155">Включение функции Close — notify помогает устранить атаки усечения для HTTPS-запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="831a0-155">Enabling close-notify helps mitigate truncation attacks against the HTTPS requests and responses.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="831a0-156">Если функция Close-notify отключена, API сервера HTTP повторно использует сеанс SSL для будущих подключений.</span><span class="sxs-lookup"><span data-stu-id="831a0-156">When close-notify is disabled, the HTTP Server API reuses the SSL session for future connections.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="831a0-157">дисаблесслцертчаинкачеонлюрлретриевал</span><span class="sxs-lookup"><span data-stu-id="831a0-157">DisableSslCertChainCacheOnlyUrlRetrieval</span></span></td>
<td><span data-ttu-id="831a0-158">Значение <strong>типа DWORD</strong> , равное <strong>true</strong> , чтобы разрешить API HTTP-сервера получать промежуточные сертификаты из Интернета или локального хранилища или <strong>false</strong> для получения промежуточных сертификатов только из локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="831a0-158">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable the HTTP Server API to retrieve intermediate certificates from either the Internet, or the local store, or <strong>FALSE</strong> to retrieve intermediate certificates from the local store only.</span></span> <span data-ttu-id="831a0-159">Значение реестра по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="831a0-159">The default registry value is <strong>FALSE</strong>.</span></span><br/> <span data-ttu-id="831a0-160">По умолчанию API сервера HTTP создает цепочку сертификатов клиента, получая промежуточные сертификаты из промежуточного хранилища центра сертификации под учетной записью локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="831a0-160">By default, the HTTP Server API builds a client certificate chain by retrieving the intermediate certificates from the Intermediate Certificate Authority store under the local machine account.</span></span> <span data-ttu-id="831a0-161">Установка этого значения равным <strong>true</strong> позволяет API-интерфейсу сервера HTTP получать промежуточные сертификаты не только из локального хранилища, но и из промежуточного центра сертификации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="831a0-161">Setting this value to <strong>TRUE</strong> enables the HTTP Server API to retrieve the intermediate certificates not only from the local store, but also from the Intermediate Certificate Authority on the Internet.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





