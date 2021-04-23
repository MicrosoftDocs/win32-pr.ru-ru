---
description: В таблице AppId или в таблице реестра указано, что установщик настраивает и регистрирует серверы DCOM для выполнения одной из следующих задач во время установки.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Таблица AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909108"
---
# <a name="appid-table"></a><span data-ttu-id="53f81-103">Таблица AppId</span><span class="sxs-lookup"><span data-stu-id="53f81-103">AppId Table</span></span>

<span data-ttu-id="53f81-104">В таблице AppId или в [таблице реестра](registry-table.md) указано, что установщик настраивает и РЕГИСТРИРУЕТ серверы DCOM для выполнения одной из следующих задач во время установки.</span><span class="sxs-lookup"><span data-stu-id="53f81-104">The AppId table or the [Registry table](registry-table.md) specifies that the installer configure and register DCOM servers to do one of the following during an installation.</span></span>

-   <span data-ttu-id="53f81-105">Запустите DCOM-сервер под другим идентификатором, отличным от идентификатора пользователя, который активирует сервер.</span><span class="sxs-lookup"><span data-stu-id="53f81-105">Run the DCOM server under a different identity than the user activating the server.</span></span> <span data-ttu-id="53f81-106">Например, чтобы настроить сервер DCOM так, чтобы он всегда выполнялся как интерактивный пользователь или как предопределенный пользователь.</span><span class="sxs-lookup"><span data-stu-id="53f81-106">For example, to configure a DCOM server to always run as an interactive user or as a predefined user.</span></span>
-   <span data-ttu-id="53f81-107">Запустите сервер DCOM как службу.</span><span class="sxs-lookup"><span data-stu-id="53f81-107">Run the DCOM server as a service.</span></span>
-   <span data-ttu-id="53f81-108">Настройте уровень доступа по умолчанию для DCOM Server.</span><span class="sxs-lookup"><span data-stu-id="53f81-108">Configure the default security access for the DCOM server.</span></span>
-   <span data-ttu-id="53f81-109">Зарегистрируйте DCOM-сервер, чтобы он был активирован на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="53f81-109">Register the DCOM server such that it is activated on a different computer.</span></span>

<span data-ttu-id="53f81-110">Эта таблица обрабатывается при установке компонента, связанного с сервером DCOM, в \_ столбце Component [таблицы Class](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="53f81-110">This table is processed at the installation of the component associated with the DCOM server in the \_Component column of the [Class table](class-table.md).</span></span> <span data-ttu-id="53f81-111">Идентификатор AppId не объявлен.</span><span class="sxs-lookup"><span data-stu-id="53f81-111">An AppId is not advertised.</span></span>

<span data-ttu-id="53f81-112">Таблица AppId содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="53f81-112">The AppId table has the following columns.</span></span>



| <span data-ttu-id="53f81-113">Столбец</span><span class="sxs-lookup"><span data-stu-id="53f81-113">Column</span></span>               | <span data-ttu-id="53f81-114">Type</span><span class="sxs-lookup"><span data-stu-id="53f81-114">Type</span></span>                       | <span data-ttu-id="53f81-115">Ключ</span><span class="sxs-lookup"><span data-stu-id="53f81-115">Key</span></span> | <span data-ttu-id="53f81-116">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="53f81-116">Nullable</span></span> |
|----------------------|----------------------------|-----|----------|
| <span data-ttu-id="53f81-117">AppId</span><span class="sxs-lookup"><span data-stu-id="53f81-117">AppId</span></span>                | [<span data-ttu-id="53f81-118">GUID</span><span class="sxs-lookup"><span data-stu-id="53f81-118">GUID</span></span>](guid.md)           | <span data-ttu-id="53f81-119">Да</span><span class="sxs-lookup"><span data-stu-id="53f81-119">Y</span></span>   | <span data-ttu-id="53f81-120">Нет</span><span class="sxs-lookup"><span data-stu-id="53f81-120">N</span></span>        |
| <span data-ttu-id="53f81-121">ремотесервернаме</span><span class="sxs-lookup"><span data-stu-id="53f81-121">RemoteServerName</span></span>     | [<span data-ttu-id="53f81-122">Формате</span><span class="sxs-lookup"><span data-stu-id="53f81-122">Formatted</span></span>](formatted.md) | <span data-ttu-id="53f81-123">Нет</span><span class="sxs-lookup"><span data-stu-id="53f81-123">N</span></span>   | <span data-ttu-id="53f81-124">Да</span><span class="sxs-lookup"><span data-stu-id="53f81-124">Y</span></span>        |
| <span data-ttu-id="53f81-125">локальная служба.</span><span class="sxs-lookup"><span data-stu-id="53f81-125">LocalService</span></span>         | [<span data-ttu-id="53f81-126">Text</span><span class="sxs-lookup"><span data-stu-id="53f81-126">Text</span></span>](text.md)           | <span data-ttu-id="53f81-127">Нет</span><span class="sxs-lookup"><span data-stu-id="53f81-127">N</span></span>   | <span data-ttu-id="53f81-128">Да</span><span class="sxs-lookup"><span data-stu-id="53f81-128">Y</span></span>        |
| <span data-ttu-id="53f81-129">сервицепараметерс</span><span class="sxs-lookup"><span data-stu-id="53f81-129">ServiceParameters</span></span>    | [<span data-ttu-id="53f81-130">Text</span><span class="sxs-lookup"><span data-stu-id="53f81-130">Text</span></span>](text.md)           | <span data-ttu-id="53f81-131">Нет</span><span class="sxs-lookup"><span data-stu-id="53f81-131">N</span></span>   | <span data-ttu-id="53f81-132">Да</span><span class="sxs-lookup"><span data-stu-id="53f81-132">Y</span></span>        |
| <span data-ttu-id="53f81-133">дллсуррогате</span><span class="sxs-lookup"><span data-stu-id="53f81-133">DllSurrogate</span></span>         | [<span data-ttu-id="53f81-134">Text</span><span class="sxs-lookup"><span data-stu-id="53f81-134">Text</span></span>](text.md)           | <span data-ttu-id="53f81-135">Нет</span><span class="sxs-lookup"><span data-stu-id="53f81-135">N</span></span>   | <span data-ttu-id="53f81-136">Да</span><span class="sxs-lookup"><span data-stu-id="53f81-136">Y</span></span>        |
| <span data-ttu-id="53f81-137">активатеатстораже</span><span class="sxs-lookup"><span data-stu-id="53f81-137">ActivateAtStorage</span></span>    | [<span data-ttu-id="53f81-138">Integer</span><span class="sxs-lookup"><span data-stu-id="53f81-138">Integer</span></span>](integer.md)     | <span data-ttu-id="53f81-139">Нет</span><span class="sxs-lookup"><span data-stu-id="53f81-139">N</span></span>   | <span data-ttu-id="53f81-140">Да</span><span class="sxs-lookup"><span data-stu-id="53f81-140">Y</span></span>        |
| <span data-ttu-id="53f81-141">рунасинтерактивеусер</span><span class="sxs-lookup"><span data-stu-id="53f81-141">RunAsInteractiveUser</span></span> | [<span data-ttu-id="53f81-142">Integer</span><span class="sxs-lookup"><span data-stu-id="53f81-142">Integer</span></span>](integer.md)     | <span data-ttu-id="53f81-143">Нет</span><span class="sxs-lookup"><span data-stu-id="53f81-143">N</span></span>   | <span data-ttu-id="53f81-144">Да</span><span class="sxs-lookup"><span data-stu-id="53f81-144">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="53f81-145">Столбцы</span><span class="sxs-lookup"><span data-stu-id="53f81-145">Columns</span></span>

<dl> <dt>

<span data-ttu-id="53f81-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>ИД</span><span class="sxs-lookup"><span data-stu-id="53f81-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span></span>
</dt> <dd>

<span data-ttu-id="53f81-147">Столбец AppId [таблицы Class](class-table.md) является внешним ключом в этом столбце таблицы AppID.</span><span class="sxs-lookup"><span data-stu-id="53f81-147">The AppId column of the [Class table](class-table.md) is a foreign key into this column of the AppId table.</span></span> <span data-ttu-id="53f81-148">Этот столбец содержит значение AppId, которое будет записано в CLSID, и создает ключ GUID AppId в разделе HKCR \\ AppID.</span><span class="sxs-lookup"><span data-stu-id="53f81-148">This column contains the AppId value that will be written under the CLSID and creates the AppId GUID key under HKCR\\AppId.</span></span>

</dd> <dt>

<span data-ttu-id="53f81-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>ремотесервернаме</span><span class="sxs-lookup"><span data-stu-id="53f81-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span></span>
</dt> <dd>

<span data-ttu-id="53f81-150">Этот столбец содержит значение "Ремотесервернаме" = <xxxx> , которое будет записано в разделе HKCR \\ AppID \\ {AppID} \\ .</span><span class="sxs-lookup"><span data-stu-id="53f81-150">This column contains the value of "RemoteServerName"=<xxxx> that will be written under HKCR\\AppID\\{AppID}\\ .</span></span>

</dd> <dt>

<span data-ttu-id="53f81-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span><span class="sxs-lookup"><span data-stu-id="53f81-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span></span>
</dt> <dd>

<span data-ttu-id="53f81-152">Этот столбец содержит значение LocalService, которое будет записано в разделе HKCR \\ AppID \\ { <appid> } "LocalService" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="53f81-152">This column contains the value of LocalService that will be written under HKCR\\AppID\\{<appid>} "LocalService"=<xxx>.</span></span>

</dd> <dt>

<span data-ttu-id="53f81-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>сервицепараметерс</span><span class="sxs-lookup"><span data-stu-id="53f81-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span></span>
</dt> <dd>

<span data-ttu-id="53f81-154">Этот столбец содержит значение Сервицепараметерс, которое будет записано в разделе HKCR \\ AppID \\ {AppID>} "сервицепараметерс".</span><span class="sxs-lookup"><span data-stu-id="53f81-154">This column contains the value of ServiceParameters that will be written under HKCR\\AppID\\{appid>} "ServiceParameters".</span></span>

</dd> <dt>

<span data-ttu-id="53f81-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>дллсуррогате</span><span class="sxs-lookup"><span data-stu-id="53f81-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span></span>
</dt> <dd>

<span data-ttu-id="53f81-156">Этот столбец содержит значение Дллсуррогате, которое будет записано в разделе HKCR \\ AppID \\ { <appid> } "дллсуррогате" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="53f81-156">This column contains the value of DllSurrogate that will be written under HKCR\\AppId\\{<appid>} "DllSurrogate"=<xxx>.</span></span> <span data-ttu-id="53f81-157">Если этот столбец уже имеется, он обычно будет пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="53f81-157">If this column is present it will typically be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="53f81-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>активатеатстораже</span><span class="sxs-lookup"><span data-stu-id="53f81-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span></span>
</dt> <dd>

<span data-ttu-id="53f81-159">Ненулевое целочисленное значение в этом поле приводит к тому, что установщик Windows записи HKCR \\ AppID \\ { <appid> } "активатеатстораже" = "Y" в реестр.</span><span class="sxs-lookup"><span data-stu-id="53f81-159">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{<appid>} "ActivateAtStorage"="Y" into the registry.</span></span> <span data-ttu-id="53f81-160">Если поле оставлено пустым или имеет нулевое значение, значение не будет записано.</span><span class="sxs-lookup"><span data-stu-id="53f81-160">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> <dt>

<span data-ttu-id="53f81-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>рунасинтерактивеусер</span><span class="sxs-lookup"><span data-stu-id="53f81-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span></span>
</dt> <dd>

<span data-ttu-id="53f81-162">Ненулевое целочисленное значение в этом поле приводит к тому, что установщик Windows записи HKCR \\ AppID \\ {AppID>} "runas" = "Interactive User" в реестр.</span><span class="sxs-lookup"><span data-stu-id="53f81-162">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{appid>} "RunAs"="Interactive User" into the registry.</span></span> <span data-ttu-id="53f81-163">Если поле оставлено пустым или имеет нулевое значение, значение не будет записано.</span><span class="sxs-lookup"><span data-stu-id="53f81-163">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53f81-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53f81-164">Remarks</span></span>

<span data-ttu-id="53f81-165">Эта таблица используется действием [регистерклассинфо](registerclassinfo-action.md) и [унрегистерклассинфо](unregisterclassinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="53f81-165">This table is used by the [RegisterClassInfo action](registerclassinfo-action.md) and [UnregisterClassInfo action](unregisterclassinfo-action.md).</span></span>

<span data-ttu-id="53f81-166">Обратите внимание, что в таблице AppId нет столбца для регистрации имени по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53f81-166">Note that the AppId table does not have a column for registering a Default name.</span></span> <span data-ttu-id="53f81-167">Поэтому в случаях, когда необходимо написать понятное имя в качестве значения имени по умолчанию, необходимо зарегистрировать его с помощью [таблицы реестра](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="53f81-167">Therefore in cases where you need to write a user friendly name as the Default name value, you must register using the [Registry table](registry-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="53f81-168">Проверка</span><span class="sxs-lookup"><span data-stu-id="53f81-168">Validation</span></span>

<dl>

[<span data-ttu-id="53f81-169">ICE03</span><span class="sxs-lookup"><span data-stu-id="53f81-169">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="53f81-170">ICE06</span><span class="sxs-lookup"><span data-stu-id="53f81-170">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="53f81-171">ICE32</span><span class="sxs-lookup"><span data-stu-id="53f81-171">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="53f81-172">ICE33</span><span class="sxs-lookup"><span data-stu-id="53f81-172">ICE33</span></span>](ice33.md)  
[<span data-ttu-id="53f81-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="53f81-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="53f81-174">ICE69</span><span class="sxs-lookup"><span data-stu-id="53f81-174">ICE69</span></span>](ice69.md)  
</dl>

 

 



