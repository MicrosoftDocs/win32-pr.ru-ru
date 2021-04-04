---
description: Формат строки дескриптора безопасности — это текстовый формат для хранения или передачи сведений в дескрипторе безопасности.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Формат строки дескриптора безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5182de796ee8d3c61f079d3704ab29ad552457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897777"
---
# <a name="security-descriptor-string-format"></a><span data-ttu-id="9c6c4-103">Формат строки дескриптора безопасности</span><span class="sxs-lookup"><span data-stu-id="9c6c4-103">Security Descriptor String Format</span></span>

<span data-ttu-id="9c6c4-104">**Формат строки дескриптора безопасности** — это текстовый формат для хранения или передачи сведений в дескрипторе безопасности.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="9c6c4-105">Функции [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) и [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) используют этот формат.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="9c6c4-106">Формат является строкой, завершающейся **нулем**, с токенами для указания каждого из четырех основных компонентов дескриптора безопасности: владелец (O:), основная группа (G:), DACL (D:) и SACL (S:).</span><span class="sxs-lookup"><span data-stu-id="9c6c4-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="9c6c4-107">[*Записи контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE) и условные элементы ACE имеют разные форматы.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="9c6c4-108">Сведения об элементах ACE см. в разделе [строки ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="9c6c4-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="9c6c4-109">Сведения об условных ACE см. в разделе [язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="9c6c4-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="9c6c4-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>\_идентификатор безопасности владельца</span><span class="sxs-lookup"><span data-stu-id="9c6c4-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="9c6c4-111">[Строка идентификатора безопасности](sid-strings.md) , определяющая владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="9c6c4-112"><span id="group_sid"></span><span id="GROUP_SID"></span>\_идентификатор безопасности группы</span><span class="sxs-lookup"><span data-stu-id="9c6c4-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="9c6c4-113">Строка идентификатора безопасности, определяющая основную группу объекта.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="9c6c4-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>\_Флаги DACL</span><span class="sxs-lookup"><span data-stu-id="9c6c4-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="9c6c4-115">Флаги управления дескрипторами безопасности, применяемые к DACL.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="9c6c4-116">Описание этих флагов управления см. в описании функции [**сетсекуритидескрипторконтрол**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .</span><span class="sxs-lookup"><span data-stu-id="9c6c4-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="9c6c4-117">\_Строка флагов DACL может представлять собой объединение, равное нулю или нескольким следующим строкам.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="9c6c4-118">Control</span><span class="sxs-lookup"><span data-stu-id="9c6c4-118">Control</span></span>               | <span data-ttu-id="9c6c4-119">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="9c6c4-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="9c6c4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9c6c4-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="9c6c4-121">Ш</span><span class="sxs-lookup"><span data-stu-id="9c6c4-121">"P"</span></span>                   | <span data-ttu-id="9c6c4-122">\_ЗАЩИЩЕН SDDL</span><span class="sxs-lookup"><span data-stu-id="9c6c4-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="9c6c4-123">\_ \_ Установлен флаг защищенного списка DACL SE.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="9c6c4-124">AR</span><span class="sxs-lookup"><span data-stu-id="9c6c4-124">"AR"</span></span>                  | <span data-ttu-id="9c6c4-125">запрос на \_ Автоматическое \_ НАСЛЕДОВАНие SDDL \_</span><span class="sxs-lookup"><span data-stu-id="9c6c4-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="9c6c4-126">\_ \_ \_ Установлен флаг автоматического наследования \_ req DACL.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="9c6c4-127">AI</span><span class="sxs-lookup"><span data-stu-id="9c6c4-127">"AI"</span></span>                  | <span data-ttu-id="9c6c4-128">\_Автоматический \_ НАСЛЕДОВАНный SDDL</span><span class="sxs-lookup"><span data-stu-id="9c6c4-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="9c6c4-129">\_ \_ \_ Установлен флаг автоматического наследования DACL SE.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="9c6c4-130">"без \_ \_ контроля доступа"</span><span class="sxs-lookup"><span data-stu-id="9c6c4-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="9c6c4-131">\_ACL NULL для языка SSDL \_</span><span class="sxs-lookup"><span data-stu-id="9c6c4-131">SSDL\_NULL\_ACL</span></span>          | <span data-ttu-id="9c6c4-132">Список ACL имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-132">The ACL is null.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="9c6c4-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_Флаги SACL</span><span class="sxs-lookup"><span data-stu-id="9c6c4-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="9c6c4-134">Флаги управления дескрипторами безопасности, применяемые к SACL.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-134">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="9c6c4-135">\_Строка флагов SACL использует те же контрольные строки, что и \_ строка флагов DACL.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-135">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="9c6c4-136"><span id="string_ace"></span><span id="STRING_ACE"></span>строковый \_ ACE</span><span class="sxs-lookup"><span data-stu-id="9c6c4-136"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="9c6c4-137">Строка, описывающая запись ACE в списке DACL или SACL дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-137">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="9c6c4-138">Описание формата строки ACE см. в разделе [строки ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="9c6c4-138">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="9c6c4-139">Каждая строка ACE заключается в круглые скобки (()).</span><span class="sxs-lookup"><span data-stu-id="9c6c4-139">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="9c6c4-140">Ненужные компоненты можно опустить в строке дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-140">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="9c6c4-141">Например, если \_ флаг присутствия DACL SE \_ не установлен во входном дескрипторе безопасности, [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) не включает компонент D: в выходную строку.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-141">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="9c6c4-142">Также можно использовать битовые флаги [**\_ сведений о безопасности**](security-information.md) , чтобы указать компоненты, включаемые в строку дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-142">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="9c6c4-143">Формат строки дескриптора безопасности не поддерживает списки ACL **со значением NULL** .</span><span class="sxs-lookup"><span data-stu-id="9c6c4-143">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="9c6c4-144">Для обозначения пустого списка ACL строка дескриптора безопасности включает маркер D: или S: без дополнительных строковых данных.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-144">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="9c6c4-145">В строке дескриптора безопасности [**Контрольные**](security-descriptor-control.md) биты сохраняются различными способами.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-145">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="9c6c4-146">Список DACL SE присутствует или присутствует в списке SACL, так как в \_ \_ строке есть \_ \_ наличие токена D: или S:.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-146">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="9c6c4-147">Другие биты, применимые к спискам DACL или SACL, хранятся в флагах DACL \_ и списках SACL \_ .</span><span class="sxs-lookup"><span data-stu-id="9c6c4-147">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="9c6c4-148">Владелец по \_ \_ умолчанию SE, SE \_ Group Default, SE по умолчанию \_ и список SACL по умолчанию \_ \_ \_ \_ не хранятся в строке дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-148">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="9c6c4-149">\_ \_ Относительный бит SE не хранится в строке, но [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) всегда задает этот бит в выходном дескрипторе безопасности.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-149">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="9c6c4-150">В следующих примерах показаны строки дескриптора безопасности и сведения в связанных с ними описательах безопасности.</span><span class="sxs-lookup"><span data-stu-id="9c6c4-150">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="9c6c4-151">Строка 1:</span><span class="sxs-lookup"><span data-stu-id="9c6c4-151">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="9c6c4-152">Дескриптор безопасности 1:</span><span class="sxs-lookup"><span data-stu-id="9c6c4-152">Security Descriptor 1:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0004
        SE_DACL_PRESENT
    Owner: (S-1-5-32-548)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x02
    Size:     0x001c
    AceCount: 0x0001
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x100e003f
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            GENERIC_ALL
                            Others(0x0000003f)
        Ace Sid      : (S-1-0-0)
SACL
    Not present
```



<span data-ttu-id="9c6c4-153">Строка 2:</span><span class="sxs-lookup"><span data-stu-id="9c6c4-153">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="9c6c4-154">Дескриптор безопасности 2:</span><span class="sxs-lookup"><span data-stu-id="9c6c4-154">Security Descriptor 2:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0014
        SE_DACL_PRESENT
        SE_SACL_PRESENT
    Owner: (S-1-5-21-397955417-626881126-188441444-512)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x04
    Size:     0x0104
    AceCount: 0x0007
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-18)
    Ace[01]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0024
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-21-397955417-626881126-188441444-512)
    Ace[02]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_USER
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[03]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_GROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[04]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_LOCALGROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[05]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_PRINT_QUEUE
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-550)
    Ace[06]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x00020014
                            READ_CONTROL
                            Others(0x00000014)
        Ace Sid:       (S-1-5-11)
    SACL
        Revision: 0x02
        Size:     0x001c
        AceCount: 0x0001
        Ace[00]
            AceType:       0x02 (SYSTEM_AUDIT_ACE_TYPE)
            AceSize:       0x0014
            InheritFlags:  0xc0
                SUCCESSFUL_ACCESS_ACE_FLAG
                FAILED_ACCESS_ACE_FLAG
            Access Mask:    0x000d002b
                                DELETE
                                WRITE_DAC
                                WRITE_OWNER
                                Others(0x0000002b)
            Ace Sid:       (S-1-1-0)
```



## <a name="related-topics"></a><span data-ttu-id="9c6c4-155">См. также</span><span class="sxs-lookup"><span data-stu-id="9c6c4-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c6c4-156">Строки ACE</span><span class="sxs-lookup"><span data-stu-id="9c6c4-156">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="9c6c4-157">Язык определения дескрипторов безопасности для условных элементов ACE</span><span class="sxs-lookup"><span data-stu-id="9c6c4-157">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
