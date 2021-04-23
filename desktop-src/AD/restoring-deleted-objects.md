---
title: Восстановление удаленных объектов
description: Windows Server 2003 включает в себя \ 0034; Restore Deleted Objects \ 0034; функциями.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Восстановление удаленных объектов Active Directory
- Active Directory, использование, восстановление удаленных объектов
- объекты Active Directory, восстановление удаленных объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8f1d3511bb4246826e677aa239ca594918127a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104533089"
---
# <a name="restoring-deleted-objects"></a><span data-ttu-id="58b76-106">Восстановление удаленных объектов</span><span class="sxs-lookup"><span data-stu-id="58b76-106">Restoring Deleted Objects</span></span>

<span data-ttu-id="58b76-107">Windows Server 2003 включает функцию "восстановить удаленные объекты".</span><span class="sxs-lookup"><span data-stu-id="58b76-107">Windows Server 2003 includes the "restore deleted objects" feature.</span></span>

<span data-ttu-id="58b76-108">Чтобы включить восстановление удаленных объектов, хотя бы один контроллер домена в домене должен работать под управлением Windows Server 2003 или более поздней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="58b76-108">To enable deleted object restoration, at least one domain controller in the domain must be running on Windows Server 2003 or a later version of Windows.</span></span> <span data-ttu-id="58b76-109">По умолчанию только администраторы домена могут восстанавливать удаленные объекты, хотя это и может быть делегировано другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="58b76-109">By default, only domain administrators can restore deleted objects, though this can be delegated to others.</span></span>

<span data-ttu-id="58b76-110">Для восстановления удаленных объектов применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="58b76-110">The following limitations apply to restoring deleted objects:</span></span>

-   <span data-ttu-id="58b76-111">Невозможно восстановить объект после истечения времени существования захоронения для объекта, так как по истечении времени существования захоронения объект удаляется навсегда.</span><span class="sxs-lookup"><span data-stu-id="58b76-111">An object cannot be restored when the tombstone lifetime for the object has expired because when the tombstone lifetime has expired, the object is permanently deleted.</span></span>
-   <span data-ttu-id="58b76-112">Невозможно восстановить объекты, которые существуют в корне контекста именования, например в домене или разделе приложения.</span><span class="sxs-lookup"><span data-stu-id="58b76-112">Objects that exist at the root of the naming context, such as a domain or application partition, cannot be restored.</span></span>
-   <span data-ttu-id="58b76-113">Невозможно восстановить объекты схемы.</span><span class="sxs-lookup"><span data-stu-id="58b76-113">Schema objects cannot be restored.</span></span> <span data-ttu-id="58b76-114">Объекты схемы никогда не должны удаляться.</span><span class="sxs-lookup"><span data-stu-id="58b76-114">Schema objects should never be deleted.</span></span>
-   <span data-ttu-id="58b76-115">Можно восстановить удаленные контейнеры, но восстановление удаленных объектов, находилось в контейнере до удаления, усложняется, так как древовидная структура в контейнере должна быть перестроена вручную.</span><span class="sxs-lookup"><span data-stu-id="58b76-115">It is possible to restore deleted containers, but the restoration of the deleted objects that were in the container before the deletion is difficult because the tree structure under the container must be manually reconstructed.</span></span>

## <a name="permissions-required-to-restore-a-deleted-object"></a><span data-ttu-id="58b76-116">Разрешения, необходимые для восстановления удаленного объекта</span><span class="sxs-lookup"><span data-stu-id="58b76-116">Permissions Required to Restore a Deleted Object</span></span>

<span data-ttu-id="58b76-117">При удалении объекта дескриптор безопасности объекта сохраняется.</span><span class="sxs-lookup"><span data-stu-id="58b76-117">When an object is deleted, the object security descriptor is retained.</span></span> <span data-ttu-id="58b76-118">Хотя владелец идентифицируется из дескриптора безопасности, по соображениям безопасности только администраторы домена могут восстанавливать удаленные объекты.</span><span class="sxs-lookup"><span data-stu-id="58b76-118">Although the owner is identifiable from the security descriptor, for security reasons, only domain administrators are allowed to restore deleted objects.</span></span> <span data-ttu-id="58b76-119">Администраторы домена могут предоставить разрешение на восстановление объектов для других пользователей и групп, предоставив пользователю или группе право на управление доступом захоронения.</span><span class="sxs-lookup"><span data-stu-id="58b76-119">Domain administrators can grant the permission to restore delete objects to other users and groups by granting the user or group the "Reanimate Tombstone" control access right.</span></span> <span data-ttu-id="58b76-120">Право доступа к элементу управления "восстановить захоронение" предоставляется в корне контекста именования.</span><span class="sxs-lookup"><span data-stu-id="58b76-120">The "Reanimate Tombstone" control access right is granted at the Naming Context root.</span></span> <span data-ttu-id="58b76-121">Только пользователи с разрешением на чтение объекта и его атрибутов могут считывать объект и доступные атрибуты после удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="58b76-121">Only users that had read access permission on an object and its attributes are permitted to read the object and accessible attributes after the object is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="58b76-122">Предоставление пользователю этого разрешения может представлять угрозу безопасности, так как может позволить пользователю восстановить объект учетной записи, имеющий доступ к ресурсам, к которым пользователь обычно не имеет доступа.</span><span class="sxs-lookup"><span data-stu-id="58b76-122">Granting a user this permission can be a security risk because it could permit the user to restore an account object that has access to resources that the user would not normally have access to.</span></span> <span data-ttu-id="58b76-123">При восстановлении учетной записи пользователь, по сути, получает контроль над этой учетной записью, так как пользователь должен задать первоначальный пароль для учетной записи при восстановлении учетной записи.</span><span class="sxs-lookup"><span data-stu-id="58b76-123">By restoring an account, the user essentially gains control of this account because the user must set the initial password on the account when the account is restored.</span></span>

 

<span data-ttu-id="58b76-124">Чтобы полностью восстановить удаленный объект, пользователь должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="58b76-124">To completely restore a deleted object, the user must:</span></span>

-   <span data-ttu-id="58b76-125">Иметь или быть членом группы, имеющей право доступа "reanimate" для управления захоронением.</span><span class="sxs-lookup"><span data-stu-id="58b76-125">Have, or be a member of a group that has, the "Reanimate Tombstone" control access right.</span></span>

-   <span data-ttu-id="58b76-126">Иметь доступ на запись для каждого обязательного атрибута, требующего обновления.</span><span class="sxs-lookup"><span data-stu-id="58b76-126">Have write access for each mandatory attribute that requires updating.</span></span>

-   <span data-ttu-id="58b76-127">Иметь доступ на запись к относительному различающемся имени (RDN).</span><span class="sxs-lookup"><span data-stu-id="58b76-127">Have write access to the Relative Distinguished Name (RDN).</span></span>

-   <span data-ttu-id="58b76-128">Иметь доступ на запись к каждому необязательному атрибуту, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="58b76-128">Have write access to each optional attribute that needs to be updated.</span></span>

-   <span data-ttu-id="58b76-129">Иметь права на создание дочернего элемента в целевом контейнере для класса объекта восстановленного объекта.</span><span class="sxs-lookup"><span data-stu-id="58b76-129">Have child-creation rights on the destination container for the object class of restored object.</span></span>

    > [!Note]  
    > <span data-ttu-id="58b76-130">Атрибут **IsDeleted** не проверяется во время операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="58b76-130">The **isDeleted** attribute is not verified during the restore operation.</span></span> <span data-ttu-id="58b76-131">Ни один из них не будет проверять разрешение Delete-потомок для контейнера Deleted Objects.</span><span class="sxs-lookup"><span data-stu-id="58b76-131">Neither will the delete-child permission on the "Deleted Objects" container be verified.</span></span>

     

## <a name="restoring-a-deleted-object"></a><span data-ttu-id="58b76-132">Восстановление удаленного объекта</span><span class="sxs-lookup"><span data-stu-id="58b76-132">Restoring a Deleted Object</span></span>

<span data-ttu-id="58b76-133">Чтобы восстановить удаленный объект, сначала необходимо найти объект в контейнере удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="58b76-133">To restore a deleted object, the object must first be located in the Deleted Objects container.</span></span> <span data-ttu-id="58b76-134">Дополнительные сведения о получении удаленных объектов см. в разделе [получение удаленных объектов](retrieving-deleted-objects.md).</span><span class="sxs-lookup"><span data-stu-id="58b76-134">For more information about retrieving deleted objects, see [Retrieving Deleted Objects](retrieving-deleted-objects.md).</span></span>

<span data-ttu-id="58b76-135">Когда объект найден, в одной операции LDAP должны быть выполнены следующие операции.</span><span class="sxs-lookup"><span data-stu-id="58b76-135">When the object has been located, the following operations must be completed in a single LDAP operation.</span></span> <span data-ttu-id="58b76-136">Для этого необходимо использовать функцию [**LDAP \_ Modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) с [**сервером LDAP \_ \_ Показывать \_ Удаленный \_**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) элемент управления OID.</span><span class="sxs-lookup"><span data-stu-id="58b76-136">This requires the use of the [**ldap\_modify\_ext\_s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) function with the [**LDAP\_SERVER\_SHOW\_DELETED\_OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) control.</span></span>

-   <span data-ttu-id="58b76-137">Удалите значение атрибута **IsDeleted** .</span><span class="sxs-lookup"><span data-stu-id="58b76-137">Remove the **isDeleted** attribute value.</span></span> <span data-ttu-id="58b76-138">Необходимо удалить значение атрибута **IsDeleted** , а не значение **false**.</span><span class="sxs-lookup"><span data-stu-id="58b76-138">The **isDeleted** attribute value must be removed, not set to **FALSE**.</span></span>
-   <span data-ttu-id="58b76-139">Замените различающееся имя объекта таким образом, чтобы оно перемещалось в контейнер, отличный от контейнера удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="58b76-139">Replace the distinguished name of the object so that it is moved to a container other than the Deleted Objects container.</span></span> <span data-ttu-id="58b76-140">Это может быть любой контейнер, который обычно может содержать объект.</span><span class="sxs-lookup"><span data-stu-id="58b76-140">This can be any container that can normally contain the object.</span></span> <span data-ttu-id="58b76-141">Различающееся имя предыдущего контейнера объекта можно найти в атрибуте **lastKnownParent** удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="58b76-141">The distinguished name of the previous container of the object can be found in the deleted object's **lastKnownParent** attribute.</span></span> <span data-ttu-id="58b76-142">Атрибут **lastKnownParent** задается только в том случае, если объект был удален на контроллере домена Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="58b76-142">The **lastKnownParent** attribute is only set if the object was deleted on a Windows Server 2003 domain controller.</span></span> <span data-ttu-id="58b76-143">Поэтому возможно, что содержимое атрибута **lastKnownParent** неточно.</span><span class="sxs-lookup"><span data-stu-id="58b76-143">Thus, it is possible that the content of the **lastKnownParent** attribute is inaccurate.</span></span>
-   <span data-ttu-id="58b76-144">Восстановите обязательные атрибуты объекта, которые были удалены во время удаления.</span><span class="sxs-lookup"><span data-stu-id="58b76-144">Restore the mandatory attributes for the object that were cleared during deletion.</span></span>

> [!Note]  
> <span data-ttu-id="58b76-145">Атрибут **objectCategory** также может быть задан при восстановлении объекта, но не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="58b76-145">The **objectCategory** attribute can also be set when the object is restored, but is not required.</span></span> <span data-ttu-id="58b76-146">Если значение **objectCategory** не указано, используется **objectCategory** по умолчанию для **objectClass** объекта.</span><span class="sxs-lookup"><span data-stu-id="58b76-146">If no **objectCategory** value is specified, the default **objectCategory** for the object's **objectClass** is used.</span></span>

 

<span data-ttu-id="58b76-147">После восстановления объекта доступ к нему можно получить, как до его удаления.</span><span class="sxs-lookup"><span data-stu-id="58b76-147">After the object is restored, it can be accessed as it was before it was deleted.</span></span> <span data-ttu-id="58b76-148">На этом этапе все необязательные атрибуты, которые важны для восстановления, должны быть восстановлены.</span><span class="sxs-lookup"><span data-stu-id="58b76-148">At this point, any optional attributes that are important should be restored.</span></span> <span data-ttu-id="58b76-149">Все ссылки на объект из других объектов в каталоге также должны быть восстановлены.</span><span class="sxs-lookup"><span data-stu-id="58b76-149">Any references to the object from other objects in the directory must also be restored.</span></span>

<span data-ttu-id="58b76-150">В качестве меры безопасности объекты-пользователи отключаются при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="58b76-150">As a security measure, user objects are disabled when they are restored.</span></span> <span data-ttu-id="58b76-151">Объекты пользователя должны быть включены после восстановления необязательных атрибутов, чтобы разрешить использование объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="58b76-151">User objects must be enabled after restoring the optional attributes to allow the user object to be used.</span></span>

<span data-ttu-id="58b76-152">Дополнительные сведения и пример кода, демонстрирующий восстановление удаленного объекта, см. в описании функции Рестоределетедобжект ниже.</span><span class="sxs-lookup"><span data-stu-id="58b76-152">For more information and a code example that shows how to restore a deleted object, see the RestoreDeletedObject function below.</span></span>

## <a name="restoredeletedobject"></a><span data-ttu-id="58b76-153">рестоределетедобжект</span><span class="sxs-lookup"><span data-stu-id="58b76-153">RestoreDeletedObject</span></span>

<span data-ttu-id="58b76-154">В следующем примере кода C++ показано, как восстановить удаленный объект.</span><span class="sxs-lookup"><span data-stu-id="58b76-154">The following C++ code example shows how to restore a deleted object.</span></span>


```C++
//***************************************************************************
//
//  RestoreDeletedObject()
//
//  Restores a deleted object. 
//
//  pwszDeletedDN - Contains the fully qualified distinguished name of the 
//  deleted object.
//
//  pwszDestContainerDN - Contains the fully qualified distinguished name of 
//  the folder that the deleted object should be moved to.
//
//  Returns S_OK if successful or an HRESULT or LDAP error code otherwise.
//
//***************************************************************************

HRESULT RestoreDeletedObject(LPCWSTR pwszDeletedDN, LPCWSTR pwszDestContainerDN)
{
    if((NULL == pwszDeletedDN) || (NULL == pwszDestContainerDN))
    {
        return E_POINTER;
    }
    
    HRESULT hr = E_FAIL;

    // Build the new distinguished name.
    LPWSTR pwszNewDN = new WCHAR[lstrlenW(pwszDeletedDN) + lstrlenW(pwszDestContainerDN) + 1];
    if(pwszNewDN)
    {
        wcscpy_s(pwszNewDN, pwszDeletedDN);

        // Search for the first 0x0A character. This is the delimiter in the deleted object name.
        LPWSTR pwszChar;
        for(pwszChar = pwszNewDN; *pwszChar; pwszChar = CharNextW(pwszChar))
        {
            if(('\\' == *pwszChar) && ('0' == *(pwszChar + 1)) && ('A' == *(pwszChar + 2)))
            {
                break;
            }
            
        }

        if(0 != *pwszChar)
        {
            // Truncate the name string at the delimiter.
            *pwszChar = 0;

            // Add the last known parent DN to complete the DN.
            wcscat_s(pwszNewDN, L",");
            wcscat_s(pwszNewDN, pwszDestContainerDN);

            PLDAP ld;

            // Initialize LDAP.
            ld = ldap_init(NULL, LDAP_PORT);
            if(NULL != ld) 
            {
                ULONG ulRC;
                ULONG version = LDAP_VERSION3;

                // Set the LDAP version.
                ulRC = ldap_set_option(ld, LDAP_OPT_PROTOCOL_VERSION, (void*)&version);
                if(LDAP_SUCCESS == ulRC)
                {
                    // Establish a connection with the server.
                    ulRC = ldap_connect(ld, NULL);
                    if(LDAP_SUCCESS == ulRC)
                    {                    
                        // Bind to the LDAP server.
                        ulRC = ldap_bind_s(ld, NULL, NULL, LDAP_AUTH_NEGOTIATE);
                        if(LDAP_SUCCESS == ulRC)
                        {
                            // Setup the new values.
                            LPWSTR rgNewVals[] = {pwszNewDN, NULL};

                            /*
                            Remove the isDeleted attribute. This cannot be set 
                            to FALSE or the restore operation will not work.
                            */
                            LDAPModW modIsDeleted = { LDAP_MOD_DELETE, L"isDeleted", NULL };

                            /*
                            Set the new DN, in effect, moving the deleted 
                            object to where it resided before the deletion.
                            */
                            LDAPModW modDN = { LDAP_MOD_REPLACE, L"distinguishedName", rgNewVals };
                            
                            // Initialize the LDAPMod structure.
                            PLDAPModW ldapMods[] = 
                            {
                                &modIsDeleted,
                                &modDN,
                                NULL
                            };

                            /*
                            Use the LDAP_SERVER_SHOW_DELETED_OID control to 
                            modify deleted objects.
                            */
                            LDAPControlW showDeletedControl;
                            showDeletedControl.ldctl_oid = LDAP_SERVER_SHOW_DELETED_OID_W;
                            showDeletedControl.ldctl_value.bv_len = 0;
                            showDeletedControl.ldctl_value.bv_val = NULL;
                            showDeletedControl.ldctl_iscritical = TRUE;

                            // Initialzie the LDAPControl structure
                            PLDAPControlW ldapControls[] = { &showDeletedControl, NULL };

                            /*
                            Modify the specified attributes. This must performed 
                            in one step, which is why the LDAP APIs must be used 
                            to restore a deleted object.
                            */
                            ulRC = ldap_modify_ext_sW(ld, (PWCHAR)pwszDeletedDN, ldapMods, ldapControls, NULL);
                            if(LDAP_SUCCESS == ulRC)
                            {
                                hr = S_OK;
                            }
                            else if(LDAP_ALREADY_EXISTS == ulRC)
                            {
                                /*
                                An object already exists with the specified name 
                                in the specified target container. At this point, 
                                a new name must be selected.
                                */
                            }
                        }
                    }
                }

                if(LDAP_SUCCESS != ulRC)
                {
                    hr = ulRC;
                    
                    OutputDebugString(ldap_err2string(ulRC));
                }

                // Release the LDAP session.
                ldap_unbind(ld);
            }
        }
        else
        {
            /*
            If the end of the string is reached before the delimiter is found, just 
            end and fail.
            */
            hr = E_INVALIDARG;
        }
    
        delete pwszNewDN;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    return hr;
}

```



 

 