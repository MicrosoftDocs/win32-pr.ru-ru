---
title: Дескрипторы безопасности для файлов и разделов реестра
description: Интерфейсы служб Active Directory (ADSI) можно использовать для управления файловыми системами в Организации и обеспечения их безопасности, включая возможность установки или изменения списков управления доступом для файлов или файловых ресурсов, созданных пользователями.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Дескрипторы безопасности для файлов и разделов реестра ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11600a495b9a70513b9bd401777e9cdd61449ede
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488284"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a><span data-ttu-id="4af9f-104">Дескрипторы безопасности для файлов и разделов реестра</span><span class="sxs-lookup"><span data-stu-id="4af9f-104">Security Descriptors on Files and Registry Keys</span></span>

<span data-ttu-id="4af9f-105">Интерфейсы служб Active Directory (ADSI) можно использовать для управления файловыми системами в Организации и обеспечения их безопасности, включая возможность установки или изменения списков управления доступом для файлов или файловых ресурсов, созданных пользователями.</span><span class="sxs-lookup"><span data-stu-id="4af9f-105">Active Directory Service Interfaces (ADSI) can be used to manage and secure file systems within an organization, including the ability to set or modify ACLs on files or file shares created by users.</span></span> <span data-ttu-id="4af9f-106">Такие интерфейсы безопасности, как [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**иадсакцессконтроллист**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)и [**Иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , устанавливают списки управления доступом на Active Directory, Exchange, файл, общую папку или объекты разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="4af9f-106">Security interfaces, such as [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) set ACLs on Active Directory, Exchange, file, file share, or registry key objects.</span></span> <span data-ttu-id="4af9f-107">Перед использованием этих интерфейсов может потребоваться изменить дескриптор безопасности, если он использует другой формат интерфейса, или если у вас нет прав доступа к SACL дескриптора безопасности, так как вы не являетесь членом группы администраторов безопасности.</span><span class="sxs-lookup"><span data-stu-id="4af9f-107">Before using these interfaces, the security descriptor may need to be modified if it uses a different format from the interface, or if you do not have access rights to the SACL of the security descriptor because you are not a member of the security administrator group.</span></span>

<span data-ttu-id="4af9f-108">Чтобы получить, задать или изменить дескриптор безопасности, используйте интерфейс [**иадссекуритютилити**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) .</span><span class="sxs-lookup"><span data-stu-id="4af9f-108">To get, set, or modify the security descriptor, use the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface.</span></span> <span data-ttu-id="4af9f-109">Этот интерфейс позволяет получить дескриптор безопасности из различных ресурсов в исходном формате, например в формате ADSI [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), необработанном дескрипторе безопасности или в виде шестнадцатеричной строки, используемой в Exchange 5,5.</span><span class="sxs-lookup"><span data-stu-id="4af9f-109">This interface enables you to retrieve a security descriptor from various resources in its original format, such as the ADSI format [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), a raw security descriptor, or as a hexadecimal string as used in Exchange 5.5.</span></span> <span data-ttu-id="4af9f-110">При извлечении можно преобразовать его в другой формат, например из необработанного дескриптора безопасности в **иадссекуритидескриптор**.</span><span class="sxs-lookup"><span data-stu-id="4af9f-110">When retrieved, you can convert it to another format, for example, from a raw security descriptor to **IADsSecurityDescriptor**.</span></span> <span data-ttu-id="4af9f-111">Затем можно записать новый формат обратно в ресурс.</span><span class="sxs-lookup"><span data-stu-id="4af9f-111">You can then write the new format back to the resource.</span></span>

<span data-ttu-id="4af9f-112">Некоторые значения свойств [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , такие как [**AccessMask**](iadsaccesscontrolentry-property-methods.md) и **AceFlags**, будут отличаться для разных типов объектов.</span><span class="sxs-lookup"><span data-stu-id="4af9f-112">Some of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property values, such as [**AccessMask**](iadsaccesscontrolentry-property-methods.md) and **AceFlags**, will be different for different object types.</span></span> <span data-ttu-id="4af9f-113">Например, для свойства **иадсакцессконтролентри. AccessMask** объект Active Directory будет использовать **\_ \_ обобщенный универсальный член \_ Read** в перечислении [**\_ прав \_ на рекламу**](/windows/win32/api/iads/ne-iads-ads_rights_enum) , но эквивалентное право доступа для файлового объекта — это **\_ универсальный файл \_ Read**.</span><span class="sxs-lookup"><span data-stu-id="4af9f-113">For example, an Active Directory object will use the **ADS\_RIGHT\_GENERIC\_READ** member of the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration for the **IADsAccessControlEntry.AccessMask** property, but the equivalent access right for a file object is **FILE\_GENERIC\_READ**.</span></span> <span data-ttu-id="4af9f-114">Нельзя считать, что все значения свойств будут одинаковыми для Active Directory объектов и объектов, не являющихся Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4af9f-114">It is not safe to assume that all property values will be the same for Active Directory objects and non-Active Directory objects.</span></span> <span data-ttu-id="4af9f-115">В следующем списке показаны свойства **иадсакцессконтролентри** , которые отличаются для объектов, не являющихся Active Directory, и там, где можно получить соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="4af9f-115">The following list shows the **IADsAccessControlEntry** properties that differ for non-Active Directory objects and where the proper values can be obtained.</span></span>

<dl> <dt>

<span data-ttu-id="4af9f-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="4af9f-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="4af9f-117">Дополнительные сведения и список возможных значений для объектов файловых или файловых ресурсов см. в разделе [безопасность и права доступа к](/windows/desktop/FileIO/file-security-and-access-rights)файлам.</span><span class="sxs-lookup"><span data-stu-id="4af9f-117">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="4af9f-118">Дополнительные сведения и список возможных значений для объектов реестра см. в разделе раздел [реестра Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="4af9f-118">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

</dd> <dt>

<span data-ttu-id="4af9f-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="4af9f-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="4af9f-120">Дополнительные сведения см. в описании элемента **AceType** структуры [**\_ заголовка ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="4af9f-120">For more information, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4af9f-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="4af9f-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="4af9f-122">Дополнительные сведения см. в описании элемента **AceFlags** структуры [**\_ заголовка ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="4af9f-122">For more information, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4af9f-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Метки**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="4af9f-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Flags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="4af9f-124">Содержит ноль или сочетание одного или нескольких из следующих значений в WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="4af9f-124">Contains zero or a combination of one or more of the following values from WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="4af9f-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ \_ \_ Представлен тип объекта** (1)</span><span class="sxs-lookup"><span data-stu-id="4af9f-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE\_OBJECT\_TYPE\_PRESENT** (1)</span></span>
</dt> <dd>

<span data-ttu-id="4af9f-126">[**ObjectType**](iadsaccesscontrolentry-property-methods.md) содержит допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="4af9f-126">[**ObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> <dt>

<span data-ttu-id="4af9f-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ Имеется наследуемый \_ \_ тип \_ объекта** (2)</span><span class="sxs-lookup"><span data-stu-id="4af9f-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE\_INHERITED\_OBJECT\_TYPE\_PRESENT** (2)</span></span>
</dt> <dd>

<span data-ttu-id="4af9f-128">[**Инхеритедобжекттипе**](iadsaccesscontrolentry-property-methods.md) содержит допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="4af9f-128">[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4af9f-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="4af9f-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="4af9f-130">Дополнительные сведения см. в разделе **ObjectType** элемента [**\_ \_ \_ ACE доступ запрещенный**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace)объект, [**доступ к \_ \_ \_ ACE разрешенного объекта**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)и аналогичные структуры.</span><span class="sxs-lookup"><span data-stu-id="4af9f-130">For more information, see the **ObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="4af9f-131">Это свойство не следует задавать или изменять для объектов, не являющихся Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4af9f-131">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> <dt>

<span data-ttu-id="4af9f-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**инхеритедобжекттипе**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="4af9f-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="4af9f-133">Дополнительные сведения см. в разделе **инхеритедобжекттипе** элемента [**\_ \_ \_ ACE доступ запрещенный**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace)объект, [**доступ к \_ \_ \_ ACE разрешенного объекта**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)и аналогичные структуры.</span><span class="sxs-lookup"><span data-stu-id="4af9f-133">For more information, see the **InheritedObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="4af9f-134">Это свойство не следует задавать или изменять для объектов, не являющихся Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4af9f-134">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> </dl>

<span data-ttu-id="4af9f-135">Обычно [**иадссекуритютилити. жетсекуритидескриптор**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) получает все части дескриптора безопасности, такие как владелец, группа, SACL или DACL.</span><span class="sxs-lookup"><span data-stu-id="4af9f-135">Normally, [**IADsSecurityUtility.GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) will retrieve all parts of the security descriptor, such as owner, group, SACL, or DACL.</span></span> <span data-ttu-id="4af9f-136">Аналогичным образом [**иадссекуритютилити. сетсекуритидескриптор**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) будет перезаписывать все части дескриптора безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4af9f-136">Similarly, [**IADsSecurityUtility.SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) will overwrite all parts of the security descriptor by default.</span></span> <span data-ttu-id="4af9f-137">Свойство [**иадссекуритютилити. секуритимаск**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) можно использовать для указания отдельных частей дескриптора безопасности, которые необходимо извлечь или задать.</span><span class="sxs-lookup"><span data-stu-id="4af9f-137">You can use the [**IADsSecurityUtility.SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) property to specify individual parts of the security descriptor to retrieve or set.</span></span> <span data-ttu-id="4af9f-138">Например, можно задать для **секуритимаск** в [**ADS \_ \_ \_ DACL сведения о безопасности**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) перед вызовом **жетсекуритидескриптор** , чтобы получить список DACL, не извлекая другие части дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="4af9f-138">For example, you can set **SecurityMask** to [**ADS\_SECURITY\_INFO\_DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) before calling **GetSecurityDescriptor** to only retrieve the DACL without retrieving the other parts of the security descriptor.</span></span>

<span data-ttu-id="4af9f-139">Дополнительные сведения и пример кода, в котором используется интерфейс [**иадссекуритютилити**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) для добавления ACE в файл, см. в разделе [пример кода для добавления ACE в файл](example-code-for-adding-an-ace-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="4af9f-139">For more information and a code example that uses the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface to add an ACE to a file, see [Example Code for Adding an ACE to a File](example-code-for-adding-an-ace-to-a-file.md).</span></span>

<span data-ttu-id="4af9f-140">В следующем примере кода представлены константные идентификаторы для файлов, файловых ресурсов и объектов реестра для свойств [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** и **flags** для использования с Visual Basic и Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="4af9f-140">The following example code provides the constant identifiers for file, file share and registry objects for the [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags**, and **Flags** properties for use with Visual Basic and Microsoft Visual Basic Scripting Edition.</span></span>


```VB
' Identifiers for the IADsAccessControlEntry.AccessMask property for file,
' file share, and registry objects.
Const DELETE = &H10000
Const READ_CONTROL = &H20000
Const WRITE_DAC = &H40000
Const WRITE_OWNER = &H80000
Const SYNCHRONIZE = &H100000

Const STANDARD_RIGHTS_REQUIRED = &HF0000

Const STANDARD_RIGHTS_READ = &H20000
Const STANDARD_RIGHTS_WRITE = &H20000
Const STANDARD_RIGHTS_EXECUTE = &H20000

Const STANDARD_RIGHTS_ALL = &H1F0000

Const SPECIFIC_RIGHTS_ALL = &HFFFF

' Identifiers for the IADsAccessControlEntry.AccessMask property for file and
' file share objects.
Const FILE_READ_DATA = &H1                  '  file & pipe
Const FILE_LIST_DIRECTORY = &H1             '  directory

Const FILE_WRITE_DATA = &H2                 '  file & pipe
Const FILE_ADD_FILE = &H2                   '  directory

Const FILE_APPEND_DATA = &H4                '  file
Const FILE_ADD_SUBDIRECTORY = &H4           '  directory
Const FILE_CREATE_PIPE_INSTANCE = &H4       '  named pipe

Const FILE_READ_EA = &H8                    '  file & directory

Const FILE_WRITE_EA = &H10                  '  file & directory

Const FILE_EXECUTE = &H20                   '  file
Const FILE_TRAVERSE = &H20                  '  directory

Const FILE_DELETE_CHILD = &H40              '  directory

Const FILE_READ_ATTRIBUTES = &H80           '  all

Const FILE_WRITE_ATTRIBUTES = &H100         '  all

Const FILE_ALL_ACCESS = STANDARD_RIGHTS_REQUIRED Or SYNCHRONIZE Or &H1FF

Const FILE_GENERIC_READ = STANDARD_RIGHTS_READ Or FILE_READ_DATA Or FILE_READ_ATTRIBUTES Or _
                          FILE_READ_EA Or SYNCHRONIZE

Const FILE_GENERIC_WRITE = STANDARD_RIGHTS_WRITE Or FILE_WRITE_DATA Or FILE_WRITE_ATTRIBUTES Or _
                           FILE_WRITE_EA Or FILE_APPEND_DATA Or SYNCHRONIZE

Const FILE_GENERIC_EXECUTE = STANDARD_RIGHTS_EXECUTE Or FILE_READ_ATTRIBUTES Or FILE_EXECUTE Or SYNCHRONIZE


' Identifiers for the IADsAccessControlEntry.AccessMask property for registry
' objects.
Const KEY_QUERY_VALUE = &H1
Const KEY_SET_VALUE = &H2
Const KEY_CREATE_SUB_KEY = &H4
Const KEY_ENUMERATE_SUB_KEYS = &H8
Const KEY_NOTIFY = &H10
Const KEY_CREATE_LINK = &H20
Const KEY_WOW64_32KEY = &H200
Const KEY_WOW64_64KEY = &H100
Const KEY_WOW64_RES = &H300

Const KEY_READ = ((STANDARD_RIGHTS_READ Or KEY_QUERY_VALUE Or KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY) And _
                  (Not SYNCHRONIZE))

Const KEY_WRITE = ((STANDARD_RIGHTS_WRITE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY) And (Not SYNCHRONIZE))

Const KEY_EXECUTE = ((KEY_READ) And (Not SYNCHRONIZE))

Const KEY_ALL_ACCESS = ((STANDARD_RIGHTS_ALL Or KEY_QUERY_VALUE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY Or _
                         KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY Or KEY_CREATE_LINK) And (Not SYNCHRONIZE))
    

' Identifiers for the IADsAccessControlEntry.AceFlags property for file and
' file share objects.
Const OBJECT_INHERIT_ACE = &H1
Const CONTAINER_INHERIT_ACE = &H2
Const NO_PROPAGATE_INHERIT_ACE = &H4
Const INHERIT_ONLY_ACE = &H8
Const INHERITED_ACE = &H10
    

' Identifiers for the IADsAccessControlEntry.Flags property.
Const ACE_OBJECT_TYPE_PRESENT = 1
Const ACE_INHERITED_OBJECT_TYPE_PRESENT = 2
```



 

 