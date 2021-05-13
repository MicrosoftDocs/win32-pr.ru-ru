---
description: Позволяет администратору управлять свойствами дисковой квоты тома.
title: Объект Дисккуотаконтрол
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841555"
---
# <a name="diskquotacontrol-object"></a><span data-ttu-id="bcd99-103">Объект Дисккуотаконтрол</span><span class="sxs-lookup"><span data-stu-id="bcd99-103">DiskQuotaControl object</span></span>

<span data-ttu-id="bcd99-104">Позволяет администратору управлять свойствами дисковой квоты тома.</span><span class="sxs-lookup"><span data-stu-id="bcd99-104">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="bcd99-105">Файловая система NTFS позволяет администратору управлять использованием дискового пространства на общем томе, выделяя заданный объем места на диске или *предельную квоту* для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="bcd99-105">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or *quota limit*, to each user.</span></span> <span data-ttu-id="bcd99-106">Этот объект можно использовать для задания предельной квоты по умолчанию, которая будет автоматически назначена всем новым пользователям.</span><span class="sxs-lookup"><span data-stu-id="bcd99-106">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span>

## <a name="members"></a><span data-ttu-id="bcd99-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="bcd99-107">Members</span></span>

<span data-ttu-id="bcd99-108">Объект **дисккуотаконтрол** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bcd99-108">The **DiskQuotaControl** object has these types of members:</span></span>

-   [<span data-ttu-id="bcd99-109">События</span><span class="sxs-lookup"><span data-stu-id="bcd99-109">Events</span></span>](#events)
-   [<span data-ttu-id="bcd99-110">Методы</span><span class="sxs-lookup"><span data-stu-id="bcd99-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bcd99-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="bcd99-111">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="bcd99-112">События</span><span class="sxs-lookup"><span data-stu-id="bcd99-112">Events</span></span>

<span data-ttu-id="bcd99-113">Объект **дисккуотаконтрол** содержит эти события.</span><span class="sxs-lookup"><span data-stu-id="bcd99-113">The **DiskQuotaControl** object has these events.</span></span>



| <span data-ttu-id="bcd99-114">Событие</span><span class="sxs-lookup"><span data-stu-id="bcd99-114">Event</span></span>                                                           | <span data-ttu-id="bcd99-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bcd99-115">Description</span></span>                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcd99-116">**онусернамечанжед**</span><span class="sxs-lookup"><span data-stu-id="bcd99-116">**OnUserNameChanged**</span></span>](diskquotacontrol-onusernamechanged.md) | <span data-ttu-id="bcd99-117">Происходит при разрешении сведений об имени для объекта [**дидисккуотаусер**](didiskquotauser-object.md) .</span><span class="sxs-lookup"><span data-stu-id="bcd99-117">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="bcd99-118">Методы</span><span class="sxs-lookup"><span data-stu-id="bcd99-118">Methods</span></span>

<span data-ttu-id="bcd99-119">Объект **дисккуотаконтрол** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="bcd99-119">The **DiskQuotaControl** object has these methods.</span></span>



| <span data-ttu-id="bcd99-120">Метод</span><span class="sxs-lookup"><span data-stu-id="bcd99-120">Method</span></span>                                                                                    | <span data-ttu-id="bcd99-121">Описание</span><span class="sxs-lookup"><span data-stu-id="bcd99-121">Description</span></span>                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcd99-122">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="bcd99-122">**AddUser**</span></span>](diskquotacontrol-adduser.md)                                               | <span data-ttu-id="bcd99-123">Назначает для нового пользователя квоту диска, не используемую по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bcd99-123">Assigns a nondefault disk quota to a new user.</span></span><br/>                                  |
| [<span data-ttu-id="bcd99-124">**DeleteUser**</span><span class="sxs-lookup"><span data-stu-id="bcd99-124">**DeleteUser**</span></span>](diskquotacontrol-deleteuser.md)                                         | <span data-ttu-id="bcd99-125">Удаляет пользователя из тома.</span><span class="sxs-lookup"><span data-stu-id="bcd99-125">Deletes a user from the volume.</span></span><br/>                                                 |
| [<span data-ttu-id="bcd99-126">**финдусер**</span><span class="sxs-lookup"><span data-stu-id="bcd99-126">**FindUser**</span></span>](diskquotacontrol-finduser.md)                                             | <span data-ttu-id="bcd99-127">Поиск записи пользователя по имени в файле квоты тома.</span><span class="sxs-lookup"><span data-stu-id="bcd99-127">Finds a user's entry, by name, in the volume's quota file.</span></span><br/>                      |
| [<span data-ttu-id="bcd99-128">**гивеусернамересолутионприорити**</span><span class="sxs-lookup"><span data-stu-id="bcd99-128">**GiveUserNameResolutionPriority**</span></span>](diskquotacontrol-giveusernameresolutionpriority.md) | <span data-ttu-id="bcd99-129">Помещает указанный объект пользователя в строке для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="bcd99-129">Places the specified user object next in line for name resolution.</span></span><br/>              |
| [<span data-ttu-id="bcd99-130">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="bcd99-130">**Initialize**</span></span>](diskquotacontrol-initialize.md)                                         | <span data-ttu-id="bcd99-131">Открывает указанный том и инициализирует его объект управления квотой.</span><span class="sxs-lookup"><span data-stu-id="bcd99-131">Opens a specified volume and initializes its quota control object.</span></span><br/>              |
| [<span data-ttu-id="bcd99-132">**инвалидатесиднамекаче**</span><span class="sxs-lookup"><span data-stu-id="bcd99-132">**InvalidateSidNameCache**</span></span>](diskquotacontrol-invalidatesidnamecache.md)                 | <span data-ttu-id="bcd99-133">Делает недействительным кэш имен пользователей с ИДЕНТИФИКАТОРом безопасности.</span><span class="sxs-lookup"><span data-stu-id="bcd99-133">Invalidates the security ID user name cache.</span></span><br/>                                    |
| [<span data-ttu-id="bcd99-134">**шутдовннамересолутион**</span><span class="sxs-lookup"><span data-stu-id="bcd99-134">**ShutdownNameResolution**</span></span>](diskquotacontrol-shutdownnameresolution.md)                 | <span data-ttu-id="bcd99-135">Завершает работу потока разрешения имен пользователей.</span><span class="sxs-lookup"><span data-stu-id="bcd99-135">Shuts down the user name resolution thread.</span></span><br/>                                     |
| [<span data-ttu-id="bcd99-136">**транслателогоннаметосид**</span><span class="sxs-lookup"><span data-stu-id="bcd99-136">**TranslateLogonNameToSID**</span></span>](diskquotacontrol-translatelogonnametosid.md)               | <span data-ttu-id="bcd99-137">Преобразует имя входа в соответствующий идентификатор безопасности пользователя в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="bcd99-137">Translates a logon name to the corresponding user security ID in string format.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bcd99-138">Свойства</span><span class="sxs-lookup"><span data-stu-id="bcd99-138">Properties</span></span>

<span data-ttu-id="bcd99-139">Объект **дисккуотаконтрол** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bcd99-139">The **DiskQuotaControl** object has these properties.</span></span>



| <span data-ttu-id="bcd99-140">Свойство</span><span class="sxs-lookup"><span data-stu-id="bcd99-140">Property</span></span>                                                                                   | <span data-ttu-id="bcd99-141">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="bcd99-141">Access type</span></span>           | <span data-ttu-id="bcd99-142">Описание</span><span class="sxs-lookup"><span data-stu-id="bcd99-142">Description</span></span>                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcd99-143">**дефаулткуоталимит**</span><span class="sxs-lookup"><span data-stu-id="bcd99-143">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)<br/>                 | <span data-ttu-id="bcd99-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="bcd99-144">Read/write</span></span><br/> | <span data-ttu-id="bcd99-145">Задает или возвращает предельную квоту по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bcd99-145">Sets or gets the default quota limit.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="bcd99-146">**дефаулткуоталимиттекст**</span><span class="sxs-lookup"><span data-stu-id="bcd99-146">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)<br/>         | <span data-ttu-id="bcd99-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcd99-147">Read-only</span></span><br/>  | <span data-ttu-id="bcd99-148">Возвращает предельную квоту по умолчанию в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="bcd99-148">Gets the default quota limit as a text string.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="bcd99-149">**дефаулткуотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="bcd99-149">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)<br/>         | <span data-ttu-id="bcd99-150">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="bcd99-150">Read/write</span></span><br/> | <span data-ttu-id="bcd99-151">Задает или возвращает пороговое значение квоты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bcd99-151">Sets or gets the default quota threshold.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="bcd99-152">**дефаулткуотасрешолдтекст**</span><span class="sxs-lookup"><span data-stu-id="bcd99-152">**DefaultQuotaThresholdText**</span></span>](diskquotacontrol-defaultquotathresholdtext.md)<br/> | <span data-ttu-id="bcd99-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcd99-153">Read-only</span></span><br/>  | <span data-ttu-id="bcd99-154">Возвращает пороговое значение квоты по умолчанию в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="bcd99-154">Gets the default quota threshold as a text string.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="bcd99-155">**логкуоталимит**</span><span class="sxs-lookup"><span data-stu-id="bcd99-155">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)<br/>                         | <span data-ttu-id="bcd99-156">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="bcd99-156">Read/write</span></span><br/> | <span data-ttu-id="bcd99-157">Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем назначенной квоты.</span><span class="sxs-lookup"><span data-stu-id="bcd99-157">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span><br/>     |
| [<span data-ttu-id="bcd99-158">**логкуотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="bcd99-158">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)<br/>                 | <span data-ttu-id="bcd99-159">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="bcd99-159">Read/write</span></span><br/> | <span data-ttu-id="bcd99-160">Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем порога назначенной квоты.</span><span class="sxs-lookup"><span data-stu-id="bcd99-160">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span><br/> |
| [<span data-ttu-id="bcd99-161">**куотафилеинкомплете**</span><span class="sxs-lookup"><span data-stu-id="bcd99-161">**QuotaFileIncomplete**</span></span>](diskquotacontrol-quotafileincomplete.md)<br/>             | <span data-ttu-id="bcd99-162">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcd99-162">Read-only</span></span><br/>  | <span data-ttu-id="bcd99-163">Возвращает логическое значение, указывающее, завершен ли файл квоты для тома.</span><span class="sxs-lookup"><span data-stu-id="bcd99-163">Gets a Boolean value that indicates whether the quota file for the volume is complete.</span></span><br/>                                                             |
| [<span data-ttu-id="bcd99-164">**куотафилеребуилдинг**</span><span class="sxs-lookup"><span data-stu-id="bcd99-164">**QuotaFileRebuilding**</span></span>](diskquotacontrol-quotafilerebuilding.md)<br/>             | <span data-ttu-id="bcd99-165">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcd99-165">Read-only</span></span><br/>  | <span data-ttu-id="bcd99-166">Возвращает логическое значение, указывающее, выполняется ли перестроение файла квоты для тома.</span><span class="sxs-lookup"><span data-stu-id="bcd99-166">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span><br/>                                              |
| [<span data-ttu-id="bcd99-167">**куотастате**</span><span class="sxs-lookup"><span data-stu-id="bcd99-167">**QuotaState**</span></span>](diskquotacontrol-quotastate.md)<br/>                               | <span data-ttu-id="bcd99-168">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="bcd99-168">Read/write</span></span><br/> | <span data-ttu-id="bcd99-169">Задает или возвращает состояние дисковых квот тома.</span><span class="sxs-lookup"><span data-stu-id="bcd99-169">Sets or gets the state of the volume's disk quotas.</span></span><br/>                                                                                                |
| [<span data-ttu-id="bcd99-170">**усернамересолутион**</span><span class="sxs-lookup"><span data-stu-id="bcd99-170">**UserNameResolution**</span></span>](diskquotacontrol-usernameresolution.md)<br/>               | <span data-ttu-id="bcd99-171">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="bcd99-171">Read/write</span></span><br/> | <span data-ttu-id="bcd99-172">Задает или возвращает значение, которое управляет тем, как идентификатор безопасности пользователя разрешается в имена пользователей.</span><span class="sxs-lookup"><span data-stu-id="bcd99-172">Sets or gets a value that controls how user SID are resolved to user names.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="bcd99-173">Remarks</span><span class="sxs-lookup"><span data-stu-id="bcd99-173">Remarks</span></span>

<span data-ttu-id="bcd99-174">Администратор может использовать объект **дисккуотаконтрол** для выполнения ряда задач, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="bcd99-174">An administrator can use the **DiskQuotaControl** object to do a number of tasks, including the following:</span></span>

-   <span data-ttu-id="bcd99-175">Включение и отключение системы дисковой квоты тома.</span><span class="sxs-lookup"><span data-stu-id="bcd99-175">Enabling and disabling the volume's disk quota system.</span></span>
-   <span data-ttu-id="bcd99-176">Получение состояния системы квот на томе.</span><span class="sxs-lookup"><span data-stu-id="bcd99-176">Obtaining the status of the quota system on the volume.</span></span>
-   <span data-ttu-id="bcd99-177">Запрет места на диске для пользователей, превышающих предельную квоту.</span><span class="sxs-lookup"><span data-stu-id="bcd99-177">Denying disk space to users exceeding their quota limit.</span></span>
-   <span data-ttu-id="bcd99-178">Указание значения порога предупреждения по умолчанию и предельной квоты, которые будут назначены новым пользователям.</span><span class="sxs-lookup"><span data-stu-id="bcd99-178">Specifying the default warning threshold and quota limit values that will be assigned to new users.</span></span>
-   <span data-ttu-id="bcd99-179">Добавление и удаление пользователей.</span><span class="sxs-lookup"><span data-stu-id="bcd99-179">Adding and removing users.</span></span>

<span data-ttu-id="bcd99-180">Объект **дисккуотаконтрол** позволяет задать глобальные значения по умолчанию для тома для таких свойств, как ограничение квоты.</span><span class="sxs-lookup"><span data-stu-id="bcd99-180">The **DiskQuotaControl** object allows you to set global default values for the volume for properties such as quota limits.</span></span> <span data-ttu-id="bcd99-181">Однако каждый пользователь представлен объектом [**дидисккуотаусер**](didiskquotauser-object.md) , который можно использовать для указания отдельных параметров квоты.</span><span class="sxs-lookup"><span data-stu-id="bcd99-181">However, each user is represented by a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to specify individual quota settings.</span></span>

<span data-ttu-id="bcd99-182">Существует несколько способов получить объект [**дидисккуотаусер**](didiskquotauser-object.md) пользователя:</span><span class="sxs-lookup"><span data-stu-id="bcd99-182">There are several ways to obtain a user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object:</span></span>

-   <span data-ttu-id="bcd99-183">Объекты [**дидисккуотаусер**](didiskquotauser-object.md) для всех пользователей с квотами на томе предоставляются в виде коллекции, и их можно перечислить.</span><span class="sxs-lookup"><span data-stu-id="bcd99-183">The [**DIDiskQuotaUser**](didiskquotauser-object.md) objects for all users with quotas on the volume are exposed as a collection, and can be enumerated.</span></span> <span data-ttu-id="bcd99-184">Обсуждение того, как перечислить объекты **дидисккуотаусер** , см. в разделе **перечисление пользователей дисковой квоты** раздела "Примечания" в **дидисккуотаусер**.</span><span class="sxs-lookup"><span data-stu-id="bcd99-184">For a discussion of how to enumerate **DIDiskQuotaUser** objects, see **Enumerating Disk Quota Users** in the Remarks section of **DIDiskQuotaUser**.</span></span>
-   <span data-ttu-id="bcd99-185">При добавлении нового пользователя метод [**adduser**](diskquotacontrol-adduser.md) возвращает объект пользователя [**дидисккуотаусер**](didiskquotauser-object.md) .</span><span class="sxs-lookup"><span data-stu-id="bcd99-185">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>
-   <span data-ttu-id="bcd99-186">Если у вас есть имя пользователя, метод [**финдусер**](diskquotacontrol-finduser.md) возвращает объект [**дидисккуотаусер**](didiskquotauser-object.md) пользователя.</span><span class="sxs-lookup"><span data-stu-id="bcd99-186">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

<span data-ttu-id="bcd99-187">Этот объект делает необходимые функции интерфейса Идисккуотаконтрол доступными для создания сценариев и приложений на основе Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bcd99-187">This object makes the essential functionality of the IDiskQuotaControl interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcd99-188">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="bcd99-188">Requirements</span></span>



| <span data-ttu-id="bcd99-189">Требование</span><span class="sxs-lookup"><span data-stu-id="bcd99-189">Requirement</span></span> | <span data-ttu-id="bcd99-190">Значение</span><span class="sxs-lookup"><span data-stu-id="bcd99-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd99-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcd99-191">Minimum supported client</span></span><br/> | <span data-ttu-id="bcd99-192">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bcd99-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bcd99-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcd99-193">Minimum supported server</span></span><br/> | <span data-ttu-id="bcd99-194">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bcd99-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bcd99-195">DLL</span><span class="sxs-lookup"><span data-stu-id="bcd99-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcd99-196"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="bcd99-196"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcd99-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcd99-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd99-198">**Объект оболочки**</span><span class="sxs-lookup"><span data-stu-id="bcd99-198">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




