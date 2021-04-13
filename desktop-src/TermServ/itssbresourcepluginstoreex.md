---
title: Интерфейс Итссбресаурцеплугинсторикс
description: Предоставляет методы, позволяющие подключаемым модулям ресурсов хранить объекты, такие как сеансы и целевые объекты.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Итссбресаурцеплугинсторикс
- Службы удаленных рабочих столов интерфейса Итссбресаурцеплугинсторикс, описание
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136310"
---
# <a name="itssbresourcepluginstoreex-interface"></a><span data-ttu-id="a753b-105">Интерфейс Итссбресаурцеплугинсторикс</span><span class="sxs-lookup"><span data-stu-id="a753b-105">ITsSbResourcePluginStoreEx interface</span></span>

<span data-ttu-id="a753b-106">Предоставляет методы, позволяющие подключаемым модулям ресурсов хранить объекты, такие как сеансы и целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="a753b-106">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span> <span data-ttu-id="a753b-107">Эти методы добавляют, удаляют и запрашивают эти объекты.</span><span class="sxs-lookup"><span data-stu-id="a753b-107">These methods add, delete, and query these objects.</span></span>

<span data-ttu-id="a753b-108">Этот интерфейс доступен только в Windows Server 2012 R2 с установленным [KB3091411](https://support.microsoft.com/kb/3091411) .</span><span class="sxs-lookup"><span data-stu-id="a753b-108">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="a753b-109">Методы [**аккуиретаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) и [**релеасетаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) интерфейса [**Итссбресаурцеплугинсторе**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) доступны начиная с Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a753b-109">The [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) and [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) methods of the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface are available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="a753b-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="a753b-110">Members</span></span>

<span data-ttu-id="a753b-111">Интерфейс **итссбресаурцеплугинсторикс** наследует от [**итссбресаурцеплугинсторе**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span><span class="sxs-lookup"><span data-stu-id="a753b-111">The **ITsSbResourcePluginStoreEx** interface inherits from [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span></span> <span data-ttu-id="a753b-112">**Итссбресаурцеплугинсторикс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a753b-112">**ITsSbResourcePluginStoreEx** also has these types of members:</span></span>

-   [<span data-ttu-id="a753b-113">Методы</span><span class="sxs-lookup"><span data-stu-id="a753b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a753b-114">Методы</span><span class="sxs-lookup"><span data-stu-id="a753b-114">Methods</span></span>

<span data-ttu-id="a753b-115">Интерфейс **итссбресаурцеплугинсторикс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a753b-115">The **ITsSbResourcePluginStoreEx** interface has these methods.</span></span>



| <span data-ttu-id="a753b-116">Метод</span><span class="sxs-lookup"><span data-stu-id="a753b-116">Method</span></span>                                                                                                            | <span data-ttu-id="a753b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a753b-117">Description</span></span>                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a753b-118">**аккуиретаржетлокк**</span><span class="sxs-lookup"><span data-stu-id="a753b-118">**AcquireTargetLock**</span></span>](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | <span data-ttu-id="a753b-119">Блокирует целевой объект.</span><span class="sxs-lookup"><span data-stu-id="a753b-119">Locks a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="a753b-120">**адденвиронменттосторе**</span><span class="sxs-lookup"><span data-stu-id="a753b-120">**AddEnvironmentToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | <span data-ttu-id="a753b-121">Добавляет среду в хранилище подключаемых модулей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a753b-121">Adds an environment to the resource plug-in store.</span></span><br/>                                                   |
| [<span data-ttu-id="a753b-122">**аддсессионтосторе**</span><span class="sxs-lookup"><span data-stu-id="a753b-122">**AddSessionToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | <span data-ttu-id="a753b-123">Добавляет новый сеанс в хранилище подключаемых модулей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a753b-123">Adds a new session to the resource plug-in store.</span></span><br/>                                                    |
| [<span data-ttu-id="a753b-124">**аддтаржеттосторе**</span><span class="sxs-lookup"><span data-stu-id="a753b-124">**AddTargetToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | <span data-ttu-id="a753b-125">Добавляет целевой объект в хранилище подключаемых модулей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a753b-125">Adds a target to the resource plug-in store.</span></span><br/>                                                         |
| [<span data-ttu-id="a753b-126">**делететаржет**</span><span class="sxs-lookup"><span data-stu-id="a753b-126">**DeleteTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | <span data-ttu-id="a753b-127">Удаляет целевой объект.</span><span class="sxs-lookup"><span data-stu-id="a753b-127">Deletes a target.</span></span><br/>                                                                                    |
| [<span data-ttu-id="a753b-128">**енумератинвиронментс**</span><span class="sxs-lookup"><span data-stu-id="a753b-128">**EnumerateEnvironments**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | <span data-ttu-id="a753b-129">Возвращает массив, содержащий среды, которые находятся в хранилище подключаемых модулей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a753b-129">Returns an array that contains the environments present in the resource plug-in store.</span></span><br/>               |
| [<span data-ttu-id="a753b-130">**енумератефармс**</span><span class="sxs-lookup"><span data-stu-id="a753b-130">**EnumerateFarms**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | <span data-ttu-id="a753b-131">Перечисляет все фермы, добавленные в хранилище подключаемых модулей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a753b-131">Enumerates all the farms that have been added to the resource plug-in store.</span></span><br/>                         |
| [<span data-ttu-id="a753b-132">**енумератесессионс**</span><span class="sxs-lookup"><span data-stu-id="a753b-132">**EnumerateSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | <span data-ttu-id="a753b-133">Перечисляет заданный набор сеансов.</span><span class="sxs-lookup"><span data-stu-id="a753b-133">Enumerates a specified set of sessions.</span></span><br/>                                                              |
| [<span data-ttu-id="a753b-134">**енумератетаржетс**</span><span class="sxs-lookup"><span data-stu-id="a753b-134">**EnumerateTargets**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | <span data-ttu-id="a753b-135">Возвращает массив, содержащий указанные целевые объекты, которые имеются в хранилище подключаемых модулей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a753b-135">Returns an array that contains the specified targets that are present in the resource plug-in store.</span></span><br/> |
| [<span data-ttu-id="a753b-136">**жетфармпроперти**</span><span class="sxs-lookup"><span data-stu-id="a753b-136">**GetFarmProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | <span data-ttu-id="a753b-137">Извлекает свойство фермы.</span><span class="sxs-lookup"><span data-stu-id="a753b-137">Retrieves a property of a farm.</span></span><br/>                                                                      |
| [<span data-ttu-id="a753b-138">**куеренвиронмент**</span><span class="sxs-lookup"><span data-stu-id="a753b-138">**QueryEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | <span data-ttu-id="a753b-139">Возвращает указанный объект среды.</span><span class="sxs-lookup"><span data-stu-id="a753b-139">Returns the specified environment object.</span></span><br/>                                                            |
| [<span data-ttu-id="a753b-140">**куерисессионбисессионид**</span><span class="sxs-lookup"><span data-stu-id="a753b-140">**QuerySessionBySessionId**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | <span data-ttu-id="a753b-141">Возвращает объект Session с указанным ИДЕНТИФИКАТОРом сеанса.</span><span class="sxs-lookup"><span data-stu-id="a753b-141">Returns the session object that has the specified session ID.</span></span><br/>                                        |
| [<span data-ttu-id="a753b-142">**куеритаржет**</span><span class="sxs-lookup"><span data-stu-id="a753b-142">**QueryTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | <span data-ttu-id="a753b-143">Возвращает целевой объект с указанным именем целевого объекта и именем фермы.</span><span class="sxs-lookup"><span data-stu-id="a753b-143">Returns the target that has the specified target name and farm name.</span></span><br/>                                 |
| [<span data-ttu-id="a753b-144">**релеасетаржетлокк**</span><span class="sxs-lookup"><span data-stu-id="a753b-144">**ReleaseTargetLock**</span></span>](itssbresourcepluginstoreex-releasetargetlock.md)                                         | <span data-ttu-id="a753b-145">Снимает блокировку на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="a753b-145">Releases a lock on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="a753b-146">**ремовинвиронментфромсторе**</span><span class="sxs-lookup"><span data-stu-id="a753b-146">**RemoveEnvironmentFromStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | <span data-ttu-id="a753b-147">Удаляет указанную среду из хранилища подключаемых модулей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a753b-147">Removes the specified environment from the resource plug-in store.</span></span><br/>                                   |
| [<span data-ttu-id="a753b-148">**савинвиронмент**</span><span class="sxs-lookup"><span data-stu-id="a753b-148">**SaveEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | <span data-ttu-id="a753b-149">Сохраняет окружение.</span><span class="sxs-lookup"><span data-stu-id="a753b-149">Saves an environment.</span></span><br/>                                                                                |
| [<span data-ttu-id="a753b-150">**савесессион**</span><span class="sxs-lookup"><span data-stu-id="a753b-150">**SaveSession**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | <span data-ttu-id="a753b-151">Сохраняет сеанс.</span><span class="sxs-lookup"><span data-stu-id="a753b-151">Saves a session.</span></span><br/>                                                                                     |
| [<span data-ttu-id="a753b-152">**саветаржет**</span><span class="sxs-lookup"><span data-stu-id="a753b-152">**SaveTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | <span data-ttu-id="a753b-153">Сохраняет целевой объект.</span><span class="sxs-lookup"><span data-stu-id="a753b-153">Saves a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="a753b-154">**сетенвиронментпроперти**</span><span class="sxs-lookup"><span data-stu-id="a753b-154">**SetEnvironmentProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | <span data-ttu-id="a753b-155">Задает свойство среды.</span><span class="sxs-lookup"><span data-stu-id="a753b-155">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="a753b-156">**сетенвиронментпропертивисверсиончекк**</span><span class="sxs-lookup"><span data-stu-id="a753b-156">**SetEnvironmentPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | <span data-ttu-id="a753b-157">Задает свойство среды.</span><span class="sxs-lookup"><span data-stu-id="a753b-157">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="a753b-158">**сетсессионстате**</span><span class="sxs-lookup"><span data-stu-id="a753b-158">**SetSessionState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | <span data-ttu-id="a753b-159">Установка состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="a753b-159">Sets the state of a session.</span></span><br/>                                                                         |
| [<span data-ttu-id="a753b-160">**сеттаржетпроперти**</span><span class="sxs-lookup"><span data-stu-id="a753b-160">**SetTargetProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | <span data-ttu-id="a753b-161">Задает свойство для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="a753b-161">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="a753b-162">**сеттаржетпропертивисверсиончекк**</span><span class="sxs-lookup"><span data-stu-id="a753b-162">**SetTargetPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | <span data-ttu-id="a753b-163">Задает свойство для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="a753b-163">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="a753b-164">**сеттаржетстате**</span><span class="sxs-lookup"><span data-stu-id="a753b-164">**SetTargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | <span data-ttu-id="a753b-165">Задает состояние целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="a753b-165">Sets the state of a target.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="a753b-166">Требования</span><span class="sxs-lookup"><span data-stu-id="a753b-166">Requirements</span></span>



| <span data-ttu-id="a753b-167">Требование</span><span class="sxs-lookup"><span data-stu-id="a753b-167">Requirement</span></span> | <span data-ttu-id="a753b-168">Значение</span><span class="sxs-lookup"><span data-stu-id="a753b-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a753b-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a753b-169">Minimum supported client</span></span><br/> | <span data-ttu-id="a753b-170">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a753b-170">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a753b-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a753b-171">Minimum supported server</span></span><br/> | <span data-ttu-id="a753b-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a753b-172">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="a753b-173">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a753b-173">End of server support</span></span><br/>    | <span data-ttu-id="a753b-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a753b-174">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="a753b-175">IID</span><span class="sxs-lookup"><span data-stu-id="a753b-175">IID</span></span><br/>                      | <span data-ttu-id="a753b-176">IID \_ итссбресаурцеплугинсторикс определен как 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="a753b-176">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a753b-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a753b-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a753b-178">**итссбресаурцеплугинсторе**</span><span class="sxs-lookup"><span data-stu-id="a753b-178">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[<span data-ttu-id="a753b-179">Интерфейсы виртуализации удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="a753b-179">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





