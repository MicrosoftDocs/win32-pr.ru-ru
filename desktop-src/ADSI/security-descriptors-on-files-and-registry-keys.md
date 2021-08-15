---
title: Дескрипторы безопасности для файлов и разделов реестра
description: Интерфейсы служб Active Directory (ADSI) можно использовать для управления файловыми системами в Организации и обеспечения их безопасности, включая возможность установки или изменения списков управления доступом для файлов или файловых ресурсов, созданных пользователями.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Дескрипторы безопасности для файлов и разделов реестра ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae567e9550989153f0b85207be49a729bc0499c320f410c92fc993269d997da7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333224"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a>Дескрипторы безопасности для файлов и разделов реестра

Интерфейсы служб Active Directory (ADSI) можно использовать для управления файловыми системами в Организации и обеспечения их безопасности, включая возможность установки или изменения списков управления доступом для файлов или файловых ресурсов, созданных пользователями. такие интерфейсы безопасности, как [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**иадсакцессконтроллист**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)и [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , устанавливают списки управления доступом для Active Directory, Exchange, файлов, файловых ресурсов или объектов разделов реестра. Перед использованием этих интерфейсов может потребоваться изменить дескриптор безопасности, если он использует другой формат интерфейса, или если у вас нет прав доступа к SACL дескриптора безопасности, так как вы не являетесь членом группы администраторов безопасности.

Чтобы получить, задать или изменить дескриптор безопасности, используйте интерфейс [**иадссекуритютилити**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) . этот интерфейс позволяет получить дескриптор безопасности из различных ресурсов в исходном формате, например в формате ADSI [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), необработанном дескрипторе безопасности или в виде шестнадцатеричной строки, используемой в Exchange 5,5. При извлечении можно преобразовать его в другой формат, например из необработанного дескриптора безопасности в **иадссекуритидескриптор**. Затем можно записать новый формат обратно в ресурс.

Некоторые значения свойств [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , такие как [**AccessMask**](iadsaccesscontrolentry-property-methods.md) и **AceFlags**, будут отличаться для разных типов объектов. Например, для свойства **иадсакцессконтролентри. AccessMask** объект Active Directory будет использовать **\_ \_ обобщенный универсальный член \_ Read** в перечислении [**\_ прав \_ на рекламу**](/windows/win32/api/iads/ne-iads-ads_rights_enum) , но эквивалентное право доступа для файлового объекта — это **\_ универсальный файл \_ Read**. Нельзя считать, что все значения свойств будут одинаковыми для Active Directory объектов и объектов, не являющихся Active Directory. В следующем списке показаны свойства **иадсакцессконтролентри** , которые отличаются для объектов, не являющихся Active Directory, и там, где можно получить соответствующие значения.

<dl> <dt>

<span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Дополнительные сведения и список возможных значений для объектов файловых или файловых ресурсов см. в разделе [безопасность и права доступа к](/windows/desktop/FileIO/file-security-and-access-rights)файлам.

Дополнительные сведения и список возможных значений для объектов реестра см. в разделе раздел [реестра Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).

</dd> <dt>

<span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Дополнительные сведения см. в описании элемента **AceType** структуры [**\_ заголовка ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

</dd> <dt>

<span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Дополнительные сведения см. в описании элемента **AceFlags** структуры [**\_ заголовка ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

</dd> <dt>

<span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Метки**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Содержит ноль или сочетание одного или нескольких из следующих значений в WinNT. h.

<dl> <dt>

<span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ \_ \_ Представлен тип объекта** (1)
</dt> <dd>

[**ObjectType**](iadsaccesscontrolentry-property-methods.md) содержит допустимое значение.

</dd> <dt>

<span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ Имеется наследуемый \_ \_ тип \_ объекта** (2)
</dt> <dd>

[**Инхеритедобжекттипе**](iadsaccesscontrolentry-property-methods.md) содержит допустимое значение.

</dd> </dl> </dd> <dt>

<span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Дополнительные сведения см. в разделе **ObjectType** элемента [**\_ \_ \_ ACE доступ запрещенный**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace)объект, [**доступ к \_ \_ \_ ACE разрешенного объекта**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)и аналогичные структуры. Это свойство не следует задавать или изменять для объектов, не являющихся Active Directory.

</dd> <dt>

<span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**инхеритедобжекттипе**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Дополнительные сведения см. в разделе **инхеритедобжекттипе** элемента [**\_ \_ \_ ACE доступ запрещенный**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace)объект, [**доступ к \_ \_ \_ ACE разрешенного объекта**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)и аналогичные структуры. Это свойство не следует задавать или изменять для объектов, не являющихся Active Directory.

</dd> </dl>

Обычно [**иадссекуритютилити. жетсекуритидескриптор**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) получает все части дескриптора безопасности, такие как владелец, группа, SACL или DACL. Аналогичным образом [**иадссекуритютилити. сетсекуритидескриптор**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) будет перезаписывать все части дескриптора безопасности по умолчанию. Свойство [**иадссекуритютилити. секуритимаск**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) можно использовать для указания отдельных частей дескриптора безопасности, которые необходимо извлечь или задать. Например, можно задать для **секуритимаск** в [**ADS \_ \_ \_ DACL сведения о безопасности**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) перед вызовом **жетсекуритидескриптор** , чтобы получить список DACL, не извлекая другие части дескриптора безопасности.

Дополнительные сведения и пример кода, в котором используется интерфейс [**иадссекуритютилити**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) для добавления ACE в файл, см. в разделе [пример кода для добавления ACE в файл](example-code-for-adding-an-ace-to-a-file.md).

в следующем примере кода представлены константные идентификаторы для файлов, файловых ресурсов и объектов реестра для свойств [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** и **flags** для использования с Visual Basic и Microsoft Visual Basic scripting Edition.


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



 

 