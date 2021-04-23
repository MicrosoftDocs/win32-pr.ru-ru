---
description: Используется для защиты отдельных частей приложения в заблокированной среде. Его можно использовать с установкой файлов, разделов реестра и созданных папок.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Таблица Локкпермиссионс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683350"
---
# <a name="lockpermissions-table"></a><span data-ttu-id="4fc38-104">Таблица Локкпермиссионс</span><span class="sxs-lookup"><span data-stu-id="4fc38-104">LockPermissions Table</span></span>

<span data-ttu-id="4fc38-105">Таблица Локкпермиссионс используется для защиты отдельных частей приложения в заблокированной среде.</span><span class="sxs-lookup"><span data-stu-id="4fc38-105">The LockPermissions Table is used to secure individual portions of an application in a locked-down environment.</span></span> <span data-ttu-id="4fc38-106">Его можно использовать с установкой файлов, разделов реестра и созданных папок.</span><span class="sxs-lookup"><span data-stu-id="4fc38-106">It can be used with the installation of files, registry keys, and created folders.</span></span>

<span data-ttu-id="4fc38-107">Пакет, предназначенный для установки в Windows Server 2008 R2 или Windows 7, должен использовать [таблицу мсилоккпермиссионсекс](msilockpermissionsex-table.md) , а не таблицу локкпермиссионс.</span><span class="sxs-lookup"><span data-stu-id="4fc38-107">A package intended for installation in Windows Server 2008 R2 or Windows 7 should use the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) rather than the LockPermissions Table.</span></span> <span data-ttu-id="4fc38-108">Установщик Windows версии, предшествующие установщик Windows 5,0, игнорируют таблицу Мсилоккпермиссионсекс.</span><span class="sxs-lookup"><span data-stu-id="4fc38-108">Windows Installer versions earlier than Windows Installer 5.0 ignore the MsiLockPermissionsEx Table.</span></span> <span data-ttu-id="4fc38-109">Установщик Windows 5,0 может установить пакет, содержащий таблицу Локкпермиссионс.</span><span class="sxs-lookup"><span data-stu-id="4fc38-109">Windows Installer 5.0 can install an package that contains the LockPermissions Table.</span></span> <span data-ttu-id="4fc38-110">Начиная с установщик Windows 5,0, установка пакета, содержащего таблицы Мсилоккпермиссионсекс и Локкпермиссионс, завершается ошибкой и возвращает сообщение об ошибке установщик Windows 1941.</span><span class="sxs-lookup"><span data-stu-id="4fc38-110">Beginning with Windows Installer 5.0, installation of a package that contains both the MsiLockPermissionsEx Table and the LockPermissions Table fails and returns Windows Installer error message 1941.</span></span>

<span data-ttu-id="4fc38-111">Таблица Локкпермиссионс содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="4fc38-111">The LockPermissions Table has the following columns.</span></span>



| <span data-ttu-id="4fc38-112">Столбец</span><span class="sxs-lookup"><span data-stu-id="4fc38-112">Column</span></span>     | <span data-ttu-id="4fc38-113">Type</span><span class="sxs-lookup"><span data-stu-id="4fc38-113">Type</span></span>                               | <span data-ttu-id="4fc38-114">Ключ</span><span class="sxs-lookup"><span data-stu-id="4fc38-114">Key</span></span> | <span data-ttu-id="4fc38-115">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="4fc38-115">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="4fc38-116">LockObject</span><span class="sxs-lookup"><span data-stu-id="4fc38-116">LockObject</span></span> | [<span data-ttu-id="4fc38-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="4fc38-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="4fc38-118">Да</span><span class="sxs-lookup"><span data-stu-id="4fc38-118">Y</span></span>   | <span data-ttu-id="4fc38-119">Нет</span><span class="sxs-lookup"><span data-stu-id="4fc38-119">N</span></span>        |
| <span data-ttu-id="4fc38-120">Таблица</span><span class="sxs-lookup"><span data-stu-id="4fc38-120">Table</span></span>      | [<span data-ttu-id="4fc38-121">Text</span><span class="sxs-lookup"><span data-stu-id="4fc38-121">Text</span></span>](text.md)                   | <span data-ttu-id="4fc38-122">Да</span><span class="sxs-lookup"><span data-stu-id="4fc38-122">Y</span></span>   | <span data-ttu-id="4fc38-123">Нет</span><span class="sxs-lookup"><span data-stu-id="4fc38-123">N</span></span>        |
| <span data-ttu-id="4fc38-124">Домен</span><span class="sxs-lookup"><span data-stu-id="4fc38-124">Domain</span></span>     | [<span data-ttu-id="4fc38-125">Формате</span><span class="sxs-lookup"><span data-stu-id="4fc38-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="4fc38-126">Да</span><span class="sxs-lookup"><span data-stu-id="4fc38-126">Y</span></span>   | <span data-ttu-id="4fc38-127">Да</span><span class="sxs-lookup"><span data-stu-id="4fc38-127">Y</span></span>        |
| <span data-ttu-id="4fc38-128">Пользователь</span><span class="sxs-lookup"><span data-stu-id="4fc38-128">User</span></span>       | [<span data-ttu-id="4fc38-129">Формате</span><span class="sxs-lookup"><span data-stu-id="4fc38-129">Formatted</span></span>](formatted.md)         | <span data-ttu-id="4fc38-130">Да</span><span class="sxs-lookup"><span data-stu-id="4fc38-130">Y</span></span>   | <span data-ttu-id="4fc38-131">Нет</span><span class="sxs-lookup"><span data-stu-id="4fc38-131">N</span></span>        |
| <span data-ttu-id="4fc38-132">Разрешение</span><span class="sxs-lookup"><span data-stu-id="4fc38-132">Permission</span></span> | [<span data-ttu-id="4fc38-133">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="4fc38-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="4fc38-134">Нет</span><span class="sxs-lookup"><span data-stu-id="4fc38-134">N</span></span>   | <span data-ttu-id="4fc38-135">Да</span><span class="sxs-lookup"><span data-stu-id="4fc38-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4fc38-136">Столбцы</span><span class="sxs-lookup"><span data-stu-id="4fc38-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4fc38-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="4fc38-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="4fc38-138">Этот столбец и столбец таблицы вместе указывают файл, каталог или раздел реестра, который должен быть защищен.</span><span class="sxs-lookup"><span data-stu-id="4fc38-138">This column and the Table column together specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="4fc38-139">Столбец LockObject — это внешний ключ, указывающий на первичный ключ таблицы, заданный столбцом таблицы.</span><span class="sxs-lookup"><span data-stu-id="4fc38-139">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="4fc38-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Таблица</span><span class="sxs-lookup"><span data-stu-id="4fc38-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="4fc38-141">В этом столбце и столбце LockObject указывается файл, каталог или ключ реестра, который должен быть защищен.</span><span class="sxs-lookup"><span data-stu-id="4fc38-141">This column and the LockObject column specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="4fc38-142">В столбце Таблица введите file, Registry или Креатефолдер, чтобы указать LockObject, перечисленные в таблице [файлов](file-table.md), [таблице реестра](registry-table.md)или [таблице креатефолдер](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="4fc38-142">In the Table column, enter File, Registry, or CreateFolder to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), or [CreateFolder Table](createfolder-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fc38-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Поддомен</span><span class="sxs-lookup"><span data-stu-id="4fc38-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domain</span></span>
</dt> <dd>

<span data-ttu-id="4fc38-144">Столбец, определяющий домен пользователя, для которого должны быть установлены разрешения.</span><span class="sxs-lookup"><span data-stu-id="4fc38-144">The column that identifies the domain of the user for which permissions are to be set.</span></span> <span data-ttu-id="4fc38-145">Это имя автономного компьютера или доменного имени.</span><span class="sxs-lookup"><span data-stu-id="4fc38-145">This is the name of a stand-alone machine or a domain name.</span></span> <span data-ttu-id="4fc38-146">Тип данных столбца [отформатирован](formatted.md), и в этом поле можно использовать строку \[ % доменпользователя, \] чтобы получить значение переменной среды доменпользователя для текущего домена.</span><span class="sxs-lookup"><span data-stu-id="4fc38-146">The column data type is [Formatted](formatted.md), and you may use the string \[%USERDOMAIN\] in this field to get the value of the USERDOMAIN environment variable for the current domain.</span></span> <span data-ttu-id="4fc38-147">Чтобы получить любой другой домен, необходимо использовать [Настраиваемые действия](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4fc38-147">To get any other domain requires using [Custom Actions](custom-actions.md).</span></span> <span data-ttu-id="4fc38-148">Дополнительные сведения см. в таблице настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="4fc38-148">For more information, see the Custom Action Table.</span></span>

</dd> <dt>

<span data-ttu-id="4fc38-149"><span id="User"></span><span id="user"></span><span id="USER"></span>Нажат</span><span class="sxs-lookup"><span data-stu-id="4fc38-149"><span id="User"></span><span id="user"></span><span id="USER"></span>User</span></span>
</dt> <dd>

<span data-ttu-id="4fc38-150">Столбец, определяющий локализованное имя пользователя, для которого задаются разрешения.</span><span class="sxs-lookup"><span data-stu-id="4fc38-150">The column that identifies the localized name of the user for which permissions are to be set.</span></span> <span data-ttu-id="4fc38-151">Это имя должно находиться на компьютере или в домене.</span><span class="sxs-lookup"><span data-stu-id="4fc38-151">This name must be located on the machine or domain.</span></span> <span data-ttu-id="4fc38-152">Установка завершается сбоем, если компьютер или контроллер домена не распознает сочетание домена и пользователя или если не удается получить идентификатор безопасности пользователя (SID).</span><span class="sxs-lookup"><span data-stu-id="4fc38-152">The installation fails if the machine or domain controller does not recognize the domain and user combination or if the user's security identifier (SID) cannot be retrieved.</span></span> <span data-ttu-id="4fc38-153">Для одного LockObject можно указать несколько пользователей.</span><span class="sxs-lookup"><span data-stu-id="4fc38-153">Multiple users can be specified for a single LockObject.</span></span>

<span data-ttu-id="4fc38-154">Общие имена пользователей "все" и "Администраторы" могут быть указаны на английском языке и сопоставлены с известными идентификаторами безопасности.</span><span class="sxs-lookup"><span data-stu-id="4fc38-154">The common user names "Everyone" and "Administrators" may be entered in English and are mapped to well-known SIDs.</span></span> <span data-ttu-id="4fc38-155">LocalSystem получает полный доступ ко всем дескрипторам безопасности, созданным с помощью таблицы Локкпермиссионс.</span><span class="sxs-lookup"><span data-stu-id="4fc38-155">LocalSystem is given full control in all security descriptors created through the LockPermissions Table.</span></span> <span data-ttu-id="4fc38-156">Для получения текущего пользователя можно использовать свойство [**ComputerName**](computername.md), [**свойство LogonUser**](logonuser.md) или [**свойство UserName**](username.md) в этом поле.</span><span class="sxs-lookup"><span data-stu-id="4fc38-156">You can use the [**ComputerName Property**](computername.md), [**LogonUser Property**](logonuser.md) or [**USERNAME Property**](username.md) in this field to get the current user.</span></span> <span data-ttu-id="4fc38-157">Для ввода локализованного имени любого другого пользователя или группы требуется настраиваемое действие.</span><span class="sxs-lookup"><span data-stu-id="4fc38-157">A custom action is required to enter the localized name of any other user or group.</span></span>

<span data-ttu-id="4fc38-158">Чтобы указать списки управления доступом для нескольких пользователей, можно использовать несколько записей с одинаковыми LockObject и записями таблицы (но разными записями пользователей).</span><span class="sxs-lookup"><span data-stu-id="4fc38-158">You can use multiple records with identical LockObject and Table entries (but different User entries) to specify access control lists for multiple users.</span></span>

</dd> <dt>

<span data-ttu-id="4fc38-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>PermissionSet</span><span class="sxs-lookup"><span data-stu-id="4fc38-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permission</span></span>
</dt> <dd>

<span data-ttu-id="4fc38-160">Столбец, определяющий целочисленное описание системных привилегий.</span><span class="sxs-lookup"><span data-stu-id="4fc38-160">The column that identifies the integer description of system privileges.</span></span> <span data-ttu-id="4fc38-161">Ниже приведены наиболее часто используемые значения (полный список находится в Winnt. h).</span><span class="sxs-lookup"><span data-stu-id="4fc38-161">The following gives the most commonly used values (a complete list exists in Winnt.h).</span></span>



| <span data-ttu-id="4fc38-162">Privilege</span><span class="sxs-lookup"><span data-stu-id="4fc38-162">Privilege</span></span>                                                              | <span data-ttu-id="4fc38-163">Описание</span><span class="sxs-lookup"><span data-stu-id="4fc38-163">Description</span></span>                     |
|------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="4fc38-164">УНИВЕРСАЛЬНые \_ все</span><span class="sxs-lookup"><span data-stu-id="4fc38-164">GENERIC\_ALL</span></span><br/> <span data-ttu-id="4fc38-165">0X10000000</span><span class="sxs-lookup"><span data-stu-id="4fc38-165">0X10000000</span></span><br/> <span data-ttu-id="4fc38-166">268435456</span><span class="sxs-lookup"><span data-stu-id="4fc38-166">268435456</span></span><br/>     | <span data-ttu-id="4fc38-167">Доступ для чтения, записи и выполнения</span><span class="sxs-lookup"><span data-stu-id="4fc38-167">Read, write, and execute access</span></span> |
| <span data-ttu-id="4fc38-168">УНИВЕРСАЛЬНое \_ выполнение</span><span class="sxs-lookup"><span data-stu-id="4fc38-168">GENERIC\_EXECUTE</span></span><br/> <span data-ttu-id="4fc38-169">0X20000000</span><span class="sxs-lookup"><span data-stu-id="4fc38-169">0X20000000</span></span><br/> <span data-ttu-id="4fc38-170">536 870 912</span><span class="sxs-lookup"><span data-stu-id="4fc38-170">536870912</span></span><br/> | <span data-ttu-id="4fc38-171">Доступ для выполнения</span><span class="sxs-lookup"><span data-stu-id="4fc38-171">Execute access</span></span>                  |
| <span data-ttu-id="4fc38-172">УНИВЕРСАЛЬНая \_ запись</span><span class="sxs-lookup"><span data-stu-id="4fc38-172">GENERIC\_WRITE</span></span><br/> <span data-ttu-id="4fc38-173">0X40000000</span><span class="sxs-lookup"><span data-stu-id="4fc38-173">0X40000000</span></span><br/> <span data-ttu-id="4fc38-174">1073741824</span><span class="sxs-lookup"><span data-stu-id="4fc38-174">1073741824</span></span><br/>  | <span data-ttu-id="4fc38-175">Доступ на запись</span><span class="sxs-lookup"><span data-stu-id="4fc38-175">Write access</span></span>                    |



 

<span data-ttu-id="4fc38-176">Нельзя указать УНИВЕРСАЛЬНое \_ чтение в столбце разрешений.</span><span class="sxs-lookup"><span data-stu-id="4fc38-176">You cannot specify GENERIC\_READ in the Permission column.</span></span> <span data-ttu-id="4fc38-177">Попытка выполнить это приведет к сбою.</span><span class="sxs-lookup"><span data-stu-id="4fc38-177">Attempting to do so will fail.</span></span> <span data-ttu-id="4fc38-178">Вместо этого необходимо указать значение, например \_ чтение ключа или \_ универсальное чтение файла \_ .</span><span class="sxs-lookup"><span data-stu-id="4fc38-178">Instead, you must specify a value such as KEY\_READ or FILE\_GENERIC\_READ.</span></span>

<span data-ttu-id="4fc38-179">Значение null, указанное в этом столбце, зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="4fc38-179">Null entered in this column is reserved for future use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fc38-180">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fc38-180">Remarks</span></span>

<span data-ttu-id="4fc38-181">Действия [инсталлфилес](installfiles-action.md), [вритерегистривалуес](writeregistryvalues-action.md)и [креатефолдерс](createfolders-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="4fc38-181">The [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md), and [CreateFolders](createfolders-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="4fc38-182">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4fc38-182">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="4fc38-183">Разрешение можно задать только в таблице Локкпермиссионс для пользователей, которые уже существуют на компьютере или в домене.</span><span class="sxs-lookup"><span data-stu-id="4fc38-183">Permission can only be set in the LockPermissions Table for users that already exist on the computer or domain.</span></span> <span data-ttu-id="4fc38-184">Попытка задать разрешения для неизвестного пользователя приводит к сбою установки, даже если эта учетная запись пользователя создается во время установки с помощью отложенного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="4fc38-184">An attempt to set permissions for an unknown user causes the installation to fail, even if that user account is created during the installation by a deferred custom action.</span></span>

<span data-ttu-id="4fc38-185">Рекомендуется включать локальную группу системных администраторов во все списки управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="4fc38-185">It is recommended that the system administrator's local group be included in all access control lists (ACL).</span></span> <span data-ttu-id="4fc38-186">Это гарантирует, что системный администратор сможет получать доступ к объектам и обслуживать их.</span><span class="sxs-lookup"><span data-stu-id="4fc38-186">This ensures that the system administrator can access and maintain objects.</span></span>

<span data-ttu-id="4fc38-187">Каждый файл, раздел реестра или каталог, указанный в таблице Локкпермиссионс, получает явный дескриптор безопасности, независимо от того, заменяет ли он существующий объект или нет.</span><span class="sxs-lookup"><span data-stu-id="4fc38-187">Every file, registry key, or directory that is listed in the LockPermissions Table receives an explicit security descriptor, whether it replaces an existing object or not.</span></span> <span data-ttu-id="4fc38-188">Установщик Windows пытается сохранить безопасность объектов, уже существующих в системе.</span><span class="sxs-lookup"><span data-stu-id="4fc38-188">The Windows Installer attempts to preserve the security on objects that already exist on the system.</span></span> <span data-ttu-id="4fc38-189">Если объект не перечислен в таблице Локкпермиссионс и заменяет существующий объект, замена Возвращает параметры безопасности заменяемого объекта.</span><span class="sxs-lookup"><span data-stu-id="4fc38-189">If an object is not listed in the LockPermissions Table, and replaces an existing object, the replacement gets the security settings of the object that it replaces.</span></span>

<span data-ttu-id="4fc38-190">Если объект не указан в таблице Локкпермиссионс и не заменяет существующий объект, он не получает явно заданного дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="4fc38-190">If an object is not listed in the LockPermissions Table, and does not replace an existing object, it receives no explicit security descriptor.</span></span> <span data-ttu-id="4fc38-191">Доступ к новому объекту основан на атрибутах его родительского объекта или контейнера.</span><span class="sxs-lookup"><span data-stu-id="4fc38-191">The access to the new object is based on the attributes of its parent or container object.</span></span> <span data-ttu-id="4fc38-192">Если объект не перечислен в таблице и заменяет объект без явного дескриптора безопасности, доступ к новому объекту основан на атрибутах его родительского объекта или контейнера.</span><span class="sxs-lookup"><span data-stu-id="4fc38-192">If an object is not listed in the table, and replaces an object with no explicit security descriptor, the access to the new object is based on the attributes of its parent or container object.</span></span>

<span data-ttu-id="4fc38-193">Установщик Windows задает [**для свойства скользящего значения идентификатор**](usersid.md) безопасности (SID) или пользователя, запускающего установку.</span><span class="sxs-lookup"><span data-stu-id="4fc38-193">The Windows Installer sets the [**UserSID**](usersid.md) property to the security identifier (SID) or the user running the installation.</span></span>

## <a name="validation"></a><span data-ttu-id="4fc38-194">Проверка</span><span class="sxs-lookup"><span data-stu-id="4fc38-194">Validation</span></span>

<dl>

[<span data-ttu-id="4fc38-195">ICE03</span><span class="sxs-lookup"><span data-stu-id="4fc38-195">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4fc38-196">ICE06</span><span class="sxs-lookup"><span data-stu-id="4fc38-196">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4fc38-197">ICE46</span><span class="sxs-lookup"><span data-stu-id="4fc38-197">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="4fc38-198">ICE55</span><span class="sxs-lookup"><span data-stu-id="4fc38-198">ICE55</span></span>](ice55.md)  
</dl>

 

 




