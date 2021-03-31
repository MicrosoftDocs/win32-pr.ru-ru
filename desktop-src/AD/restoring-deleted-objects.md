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
# <a name="restoring-deleted-objects"></a>Восстановление удаленных объектов

Windows Server 2003 включает функцию "восстановить удаленные объекты".

Чтобы включить восстановление удаленных объектов, хотя бы один контроллер домена в домене должен работать под управлением Windows Server 2003 или более поздней версии Windows. По умолчанию только администраторы домена могут восстанавливать удаленные объекты, хотя это и может быть делегировано другим пользователям.

Для восстановления удаленных объектов применяются следующие ограничения.

-   Невозможно восстановить объект после истечения времени существования захоронения для объекта, так как по истечении времени существования захоронения объект удаляется навсегда.
-   Невозможно восстановить объекты, которые существуют в корне контекста именования, например в домене или разделе приложения.
-   Невозможно восстановить объекты схемы. Объекты схемы никогда не должны удаляться.
-   Можно восстановить удаленные контейнеры, но восстановление удаленных объектов, находилось в контейнере до удаления, усложняется, так как древовидная структура в контейнере должна быть перестроена вручную.

## <a name="permissions-required-to-restore-a-deleted-object"></a>Разрешения, необходимые для восстановления удаленного объекта

При удалении объекта дескриптор безопасности объекта сохраняется. Хотя владелец идентифицируется из дескриптора безопасности, по соображениям безопасности только администраторы домена могут восстанавливать удаленные объекты. Администраторы домена могут предоставить разрешение на восстановление объектов для других пользователей и групп, предоставив пользователю или группе право на управление доступом захоронения. Право доступа к элементу управления "восстановить захоронение" предоставляется в корне контекста именования. Только пользователи с разрешением на чтение объекта и его атрибутов могут считывать объект и доступные атрибуты после удаления объекта.

> [!Note]  
> Предоставление пользователю этого разрешения может представлять угрозу безопасности, так как может позволить пользователю восстановить объект учетной записи, имеющий доступ к ресурсам, к которым пользователь обычно не имеет доступа. При восстановлении учетной записи пользователь, по сути, получает контроль над этой учетной записью, так как пользователь должен задать первоначальный пароль для учетной записи при восстановлении учетной записи.

 

Чтобы полностью восстановить удаленный объект, пользователь должен выполнить следующие действия.

-   Иметь или быть членом группы, имеющей право доступа "reanimate" для управления захоронением.

-   Иметь доступ на запись для каждого обязательного атрибута, требующего обновления.

-   Иметь доступ на запись к относительному различающемся имени (RDN).

-   Иметь доступ на запись к каждому необязательному атрибуту, который необходимо обновить.

-   Иметь права на создание дочернего элемента в целевом контейнере для класса объекта восстановленного объекта.

    > [!Note]  
    > Атрибут **IsDeleted** не проверяется во время операции восстановления. Ни один из них не будет проверять разрешение Delete-потомок для контейнера Deleted Objects.

     

## <a name="restoring-a-deleted-object"></a>Восстановление удаленного объекта

Чтобы восстановить удаленный объект, сначала необходимо найти объект в контейнере удаленных объектов. Дополнительные сведения о получении удаленных объектов см. в разделе [получение удаленных объектов](retrieving-deleted-objects.md).

Когда объект найден, в одной операции LDAP должны быть выполнены следующие операции. Для этого необходимо использовать функцию [**LDAP \_ Modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) с [**сервером LDAP \_ \_ Показывать \_ Удаленный \_**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) элемент управления OID.

-   Удалите значение атрибута **IsDeleted** . Необходимо удалить значение атрибута **IsDeleted** , а не значение **false**.
-   Замените различающееся имя объекта таким образом, чтобы оно перемещалось в контейнер, отличный от контейнера удаленных объектов. Это может быть любой контейнер, который обычно может содержать объект. Различающееся имя предыдущего контейнера объекта можно найти в атрибуте **lastKnownParent** удаленного объекта. Атрибут **lastKnownParent** задается только в том случае, если объект был удален на контроллере домена Windows Server 2003. Поэтому возможно, что содержимое атрибута **lastKnownParent** неточно.
-   Восстановите обязательные атрибуты объекта, которые были удалены во время удаления.

> [!Note]  
> Атрибут **objectCategory** также может быть задан при восстановлении объекта, но не является обязательным. Если значение **objectCategory** не указано, используется **objectCategory** по умолчанию для **objectClass** объекта.

 

После восстановления объекта доступ к нему можно получить, как до его удаления. На этом этапе все необязательные атрибуты, которые важны для восстановления, должны быть восстановлены. Все ссылки на объект из других объектов в каталоге также должны быть восстановлены.

В качестве меры безопасности объекты-пользователи отключаются при восстановлении. Объекты пользователя должны быть включены после восстановления необязательных атрибутов, чтобы разрешить использование объекта пользователя.

Дополнительные сведения и пример кода, демонстрирующий восстановление удаленного объекта, см. в описании функции Рестоределетедобжект ниже.

## <a name="restoredeletedobject"></a>рестоределетедобжект

В следующем примере кода C++ показано, как восстановить удаленный объект.


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



 

 