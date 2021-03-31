---
description: Объясняет строки, используемые в записи управления доступом.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Строки ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813289"
---
# <a name="ace-strings"></a><span data-ttu-id="fc2dd-103">Строки ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-103">ACE Strings</span></span>

<span data-ttu-id="fc2dd-104">На [языке определения дескрипторов безопасности](security-descriptor-definition-language.md) (SDDL) строки ACE используются в компонентах DACL и SACL строки [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="fc2dd-104">The [security descriptor definition language](security-descriptor-definition-language.md) (SDDL) uses ACE strings in the DACL and SACL components of a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string.</span></span>

<span data-ttu-id="fc2dd-105">Как показано в примерах [формата строки дескриптора безопасности](security-descriptor-string-format.md) , каждая запись ACE в строке дескриптора безопасности заключается в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-105">As shown in the [Security Descriptor String Format](security-descriptor-string-format.md) examples, each ACE in a security descriptor string is enclosed in parentheses.</span></span> <span data-ttu-id="fc2dd-106">Поля ACE находятся в следующем порядке и разделены точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="fc2dd-106">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="fc2dd-107">Существует другой формат [*записей управления*](/windows/desktop/SecGloss/a-gly) условным доступом (ACE), отличных от других типов ACE.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-107">There is a different format for conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) than other ACE types.</span></span> <span data-ttu-id="fc2dd-108">Сведения об условных ACE см. в разделе [язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="fc2dd-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a><span data-ttu-id="fc2dd-109">Поля</span><span class="sxs-lookup"><span data-stu-id="fc2dd-109">Fields</span></span>

<dl> <dt>

<span data-ttu-id="fc2dd-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**\_Тип ACE**</span><span class="sxs-lookup"><span data-stu-id="fc2dd-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace\_type**</span></span>
</dt> <dd>

<span data-ttu-id="fc2dd-111">Строка, указывающая значение элемента **AceType** структуры [**\_ заголовка ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="fc2dd-111">A string that indicates the value of the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="fc2dd-112">Строка типа ACE может быть одной из следующих строк, определенных в SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-112">The ACE type string can be one of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="fc2dd-113">Строка типа ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-113">ACE type string</span></span> | <span data-ttu-id="fc2dd-114">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="fc2dd-114">Constant in Sddl.h</span></span>                      | <span data-ttu-id="fc2dd-115">Значение AceType</span><span class="sxs-lookup"><span data-stu-id="fc2dd-115">AceType value</span></span>                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2dd-116">"A"</span><span class="sxs-lookup"><span data-stu-id="fc2dd-116">"A"</span></span>             | <span data-ttu-id="fc2dd-117">\_разрешен доступ \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-117">SDDL\_ACCESS\_ALLOWED</span></span>                   | <span data-ttu-id="fc2dd-118">ДОСТУП к \_ разрешенному \_ \_ типу ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-118">ACCESS\_ALLOWED\_ACE\_TYPE</span></span>                                                                                                                                         |
| <span data-ttu-id="fc2dd-119">"D"</span><span class="sxs-lookup"><span data-stu-id="fc2dd-119">"D"</span></span>             | <span data-ttu-id="fc2dd-120">\_отказано в доступе к SDDL \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-120">SDDL\_ACCESS\_DENIED</span></span>                    | <span data-ttu-id="fc2dd-121">ДОСТУП \_ запрещенный \_ \_ Тип ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-121">ACCESS\_DENIED\_ACE\_TYPE</span></span>                                                                                                                                          |
| <span data-ttu-id="fc2dd-122">OA</span><span class="sxs-lookup"><span data-stu-id="fc2dd-122">"OA"</span></span>            | <span data-ttu-id="fc2dd-123">\_ \_ доступ к объектам SDDL \_ разрешен</span><span class="sxs-lookup"><span data-stu-id="fc2dd-123">SDDL\_OBJECT\_ACCESS\_ALLOWED</span></span>           | <span data-ttu-id="fc2dd-124">ДОСТУП к \_ разрешенному \_ \_ типу ACE объекта \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-124">ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                 |
| <span data-ttu-id="fc2dd-125">OD</span><span class="sxs-lookup"><span data-stu-id="fc2dd-125">"OD"</span></span>            | <span data-ttu-id="fc2dd-126">\_ \_ доступ к объекту SDDL \_ запрещен</span><span class="sxs-lookup"><span data-stu-id="fc2dd-126">SDDL\_OBJECT\_ACCESS\_DENIED</span></span>            | <span data-ttu-id="fc2dd-127">\_ \_ \_ Тип ACE "запрещен доступ к объекту" \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-127">ACCESS\_DENIED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                  |
| <span data-ttu-id="fc2dd-128">СЛУЖБЫ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-128">"AU"</span></span>            | <span data-ttu-id="fc2dd-129">\_Аудит SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-129">SDDL\_AUDIT</span></span>                             | <span data-ttu-id="fc2dd-130">\_ \_ Тип ACE аудита \_ системы</span><span class="sxs-lookup"><span data-stu-id="fc2dd-130">SYSTEM\_AUDIT\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="fc2dd-131">«AL»</span><span class="sxs-lookup"><span data-stu-id="fc2dd-131">"AL"</span></span>            | <span data-ttu-id="fc2dd-132">\_оповещение SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-132">SDDL\_ALARM</span></span>                             | <span data-ttu-id="fc2dd-133">\_ \_ Тип ACE системного \_ оповещения</span><span class="sxs-lookup"><span data-stu-id="fc2dd-133">SYSTEM\_ALARM\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="fc2dd-134">НИХ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-134">"OU"</span></span>            | <span data-ttu-id="fc2dd-135">\_аудит объектов \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-135">SDDL\_OBJECT\_AUDIT</span></span>                     | <span data-ttu-id="fc2dd-136">\_ \_ \_ Тип ACE объекта системного \_ аудита</span><span class="sxs-lookup"><span data-stu-id="fc2dd-136">SYSTEM\_AUDIT\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="fc2dd-137">OL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-137">"OL"</span></span>            | <span data-ttu-id="fc2dd-138">\_ \_ оповещение объекта SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-138">SDDL\_OBJECT\_ALARM</span></span>                     | <span data-ttu-id="fc2dd-139">\_ \_ \_ Тип ACE объекта системного \_ оповещения</span><span class="sxs-lookup"><span data-stu-id="fc2dd-139">SYSTEM\_ALARM\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="fc2dd-140">СТУДИ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-140">"ML"</span></span>            | <span data-ttu-id="fc2dd-141">\_обязательная \_ Метка SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-141">SDDL\_MANDATORY\_LABEL</span></span>                  | <span data-ttu-id="fc2dd-142">\_Тип ACE обязательных системных \_ меток \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-142">SYSTEM\_MANDATORY\_LABEL\_ACE\_TYPE</span></span>                                                                                                                                |
| <span data-ttu-id="fc2dd-143">СООБЩЕН</span><span class="sxs-lookup"><span data-stu-id="fc2dd-143">"XA"</span></span>            | <span data-ttu-id="fc2dd-144">\_ \_ разрешен доступ к обратному ВЫЗОВу SDDL \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-144">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span>         | <span data-ttu-id="fc2dd-145">ДОСТУП к \_ разрешенному \_ ответу на обратный вызов \_ Тип ACE для \_ **windows Vista и Windows Server 2003:** недоступен.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-145">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                           |
| <span data-ttu-id="fc2dd-146">XD</span><span class="sxs-lookup"><span data-stu-id="fc2dd-146">"XD"</span></span>            | <span data-ttu-id="fc2dd-147">\_доступ к обратному вызову SDDL \_ \_ запрещен</span><span class="sxs-lookup"><span data-stu-id="fc2dd-147">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span>          | <span data-ttu-id="fc2dd-148">\_ \_ Тип ACE для обратного вызова с запретом доступа \_ \_ **windows Vista и Windows Server 2003:** недоступен.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-148">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                            |
| <span data-ttu-id="fc2dd-149">ЦЕНТРА</span><span class="sxs-lookup"><span data-stu-id="fc2dd-149">"RA"</span></span>            | <span data-ttu-id="fc2dd-150">\_атрибут ресурса \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-150">SDDL\_RESOURCE\_ATTRIBUTE</span></span>               | <span data-ttu-id="fc2dd-151">\_Атрибут системного \_ ресурса \_ \_ тип ACE **Windows Server 2008 R2, windows 7, Windows Server 2008, windows Vista и Windows Server 2003:** недоступно.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-151">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/> |
| <span data-ttu-id="fc2dd-152">ПОРТОВ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-152">"SP"</span></span>            | <span data-ttu-id="fc2dd-153">\_идентификатор политики с областью действия SDDL \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-153">SDDL\_SCOPED\_POLICY\_ID</span></span>                | <span data-ttu-id="fc2dd-154">\_ \_ Идентификатор политики уровня системы \_ \_ тип ACE \_ **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista и Windows Server 2003:** недоступно.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-154">SYSTEM\_SCOPED\_POLICY\_ID\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>  |
| <span data-ttu-id="fc2dd-155">"КСУ"</span><span class="sxs-lookup"><span data-stu-id="fc2dd-155">"XU"</span></span>            | <span data-ttu-id="fc2dd-156">\_Аудит обратного вызова SDDL \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-156">SDDL\_CALLBACK\_AUDIT</span></span>                   | <span data-ttu-id="fc2dd-157">\_ \_ Тип ACE обратного вызова аудита системы \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows Vista и Windows Server 2003:** недоступно.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-157">SYSTEM\_AUDIT\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>     |
| <span data-ttu-id="fc2dd-158">ZA</span><span class="sxs-lookup"><span data-stu-id="fc2dd-158">"ZA"</span></span>            | <span data-ttu-id="fc2dd-159">\_ \_ \_ разрешен доступ к объекту ОБРАТНОго вызова SDDL \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-159">SDDL\_CALLBACK\_OBJECT\_ACCESS\_ALLOWED</span></span> | <span data-ttu-id="fc2dd-160">ДОСТУП к \_ разрешенному \_ ответному вызову \_ Тип ACE " \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows Vista и Windows Server 2003"** недоступен.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-160">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="fc2dd-161">Если **\_ Тип ACE** имеет доступ к \_ разрешенному \_ \_ типу ACE объекта, \_ а ни **\_ GUID объекта** , ни **наследование \_ \_ GUID объекта** не имеют указанного [**идентификатора GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) , [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) преобразует **\_ Тип ACE** для доступа к \_ разрешенному \_ \_ типу ACE.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-161">If **ace\_type** is ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE and neither **object\_guid** nor **inherit\_object\_guid** has a [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specified, then [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converts **ace\_type** to ACCESS\_ALLOWED\_ACE\_TYPE.</span></span>

 

</dd> <dt>

<span data-ttu-id="fc2dd-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**\_Флаги ACE**</span><span class="sxs-lookup"><span data-stu-id="fc2dd-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace\_flags**</span></span>
</dt> <dd>

<span data-ttu-id="fc2dd-163">Строка, указывающая значение элемента **AceFlags** структуры [**\_ заголовка ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="fc2dd-163">A string that indicates the value of the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="fc2dd-164">Строка флагов ACE может быть объединением следующих строк, определенных в SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-164">The ACE flags string can be a concatenation of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="fc2dd-165">Строка флагов ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-165">ACE flags string</span></span> | <span data-ttu-id="fc2dd-166">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="fc2dd-166">Constant in Sddl.h</span></span>       | <span data-ttu-id="fc2dd-167">Значение Ацефлаг</span><span class="sxs-lookup"><span data-stu-id="fc2dd-167">AceFlag value</span></span>                 |
|------------------|--------------------------|-------------------------------|
| <span data-ttu-id="fc2dd-168">ЭЛЕМЕНТ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-168">"CI"</span></span>             | <span data-ttu-id="fc2dd-169">\_ \_ наследование контейнера SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-169">SDDL\_CONTAINER\_INHERIT</span></span> | <span data-ttu-id="fc2dd-170">КОНТЕЙНЕР \_ наследует \_ ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-170">CONTAINER\_INHERIT\_ACE</span></span>       |
| <span data-ttu-id="fc2dd-171">Oi</span><span class="sxs-lookup"><span data-stu-id="fc2dd-171">"OI"</span></span>             | <span data-ttu-id="fc2dd-172">\_ \_ наследование объектов SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-172">SDDL\_OBJECT\_INHERIT</span></span>    | <span data-ttu-id="fc2dd-173">Объект \_ наследует \_ ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-173">OBJECT\_INHERIT\_ACE</span></span>          |
| <span data-ttu-id="fc2dd-174">Протокол</span><span class="sxs-lookup"><span data-stu-id="fc2dd-174">"NP"</span></span>             | <span data-ttu-id="fc2dd-175">SDDL \_ без \_ распространения</span><span class="sxs-lookup"><span data-stu-id="fc2dd-175">SDDL\_NO\_PROPAGATE</span></span>      | <span data-ttu-id="fc2dd-176">НЕТ \_ распространения \_ наследования \_ ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-176">NO\_PROPAGATE\_INHERIT\_ACE</span></span>   |
| <span data-ttu-id="fc2dd-177">IO</span><span class="sxs-lookup"><span data-stu-id="fc2dd-177">"IO"</span></span>             | <span data-ttu-id="fc2dd-178">\_наследование \_ только SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-178">SDDL\_INHERIT\_ONLY</span></span>      | <span data-ttu-id="fc2dd-179">наследовать \_ только \_ ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-179">INHERIT\_ONLY\_ACE</span></span>            |
| <span data-ttu-id="fc2dd-180">ID</span><span class="sxs-lookup"><span data-stu-id="fc2dd-180">"ID"</span></span>             | <span data-ttu-id="fc2dd-181">\_унаследовано SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-181">SDDL\_INHERITED</span></span>          | <span data-ttu-id="fc2dd-182">УНАСЛЕДОВАНный \_ элемент ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-182">INHERITED\_ACE</span></span>                |
| <span data-ttu-id="fc2dd-183">СРОК</span><span class="sxs-lookup"><span data-stu-id="fc2dd-183">"SA"</span></span>             | <span data-ttu-id="fc2dd-184">\_ \_ успешный аудит SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-184">SDDL\_AUDIT\_SUCCESS</span></span>     | <span data-ttu-id="fc2dd-185">\_ \_ флаг ACE успешного \_ доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-185">SUCCESSFUL\_ACCESS\_ACE\_FLAG</span></span> |
| <span data-ttu-id="fc2dd-186">СЕРИЮ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-186">"FA"</span></span>             | <span data-ttu-id="fc2dd-187">\_сбой аудита \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-187">SDDL\_AUDIT\_FAILURE</span></span>     | <span data-ttu-id="fc2dd-188">неудачный \_ доступ к \_ \_ флагу ACE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-188">FAILED\_ACCESS\_ACE\_FLAG</span></span>     |



 

</dd> <dt>

<span data-ttu-id="fc2dd-189"><span id="rights"></span><span id="RIGHTS"></span>**LiveCycle**</span><span class="sxs-lookup"><span data-stu-id="fc2dd-189"><span id="rights"></span><span id="RIGHTS"></span>**rights**</span></span>
</dt> <dd>

<span data-ttu-id="fc2dd-190">Строка, указывающая [права доступа](access-rights-and-access-masks.md) , контролируемые элементом управления доступом.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-190">A string that indicates the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span> <span data-ttu-id="fc2dd-191">Эта строка может быть шестнадцатеричным строковым представлением прав доступа, например "0x7800003F", или объединением следующих строк.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-191">This string can be a hexadecimal string representation of the access rights, such as "0x7800003F", or it can be a concatenation of the following strings.</span></span>



### <a name="generic-access-rights"></a><span data-ttu-id="fc2dd-192">Универсальные права доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-192">Generic access rights</span></span>

| <span data-ttu-id="fc2dd-193">Строка прав доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-193">Access rights string</span></span> | <span data-ttu-id="fc2dd-194">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="fc2dd-194">Constant in Sddl.h</span></span> | <span data-ttu-id="fc2dd-195">Значение право доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-195">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="fc2dd-196">ОБЩЕДОСТУПНОЙ версии</span><span class="sxs-lookup"><span data-stu-id="fc2dd-196">"GA"</span></span>                 | <span data-ttu-id="fc2dd-197">\_Общий \_ список SDDL ALL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-197">SDDL\_GENERIC\_ALL</span></span> | <span data-ttu-id="fc2dd-198">УНИВЕРСАЛЬНые \_ все</span><span class="sxs-lookup"><span data-stu-id="fc2dd-198">GENERIC\_ALL</span></span>       |
| <span data-ttu-id="fc2dd-199">Группа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-199">"GR"</span></span>                 | <span data-ttu-id="fc2dd-200">\_универсальное \_ Чтение SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-200">SDDL\_GENERIC\_READ</span></span> | <span data-ttu-id="fc2dd-201">УНИВЕРСАЛЬНое \_ чтение</span><span class="sxs-lookup"><span data-stu-id="fc2dd-201">GENERIC\_READ</span></span>     |
| <span data-ttu-id="fc2dd-202">GW</span><span class="sxs-lookup"><span data-stu-id="fc2dd-202">"GW"</span></span>                 | <span data-ttu-id="fc2dd-203">\_Общая \_ запись SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-203">SDDL\_GENERIC\_WRITE</span></span> | <span data-ttu-id="fc2dd-204">УНИВЕРСАЛЬНая \_ запись</span><span class="sxs-lookup"><span data-stu-id="fc2dd-204">GENERIC\_WRITE</span></span> |
| <span data-ttu-id="fc2dd-205">GX</span><span class="sxs-lookup"><span data-stu-id="fc2dd-205">"GX"</span></span>                 | <span data-ttu-id="fc2dd-206">\_универсальное \_ выполнение SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-206">SDDL\_GENERIC\_EXECUTE</span></span> | <span data-ttu-id="fc2dd-207">УНИВЕРСАЛЬНое \_ выполнение</span><span class="sxs-lookup"><span data-stu-id="fc2dd-207">GENERIC\_EXECUTE</span></span> |


### <a name="standard-access-rights"></a><span data-ttu-id="fc2dd-208">Стандартные права доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-208">Standard access rights</span></span>

| <span data-ttu-id="fc2dd-209">Строка прав доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-209">Access rights string</span></span> | <span data-ttu-id="fc2dd-210">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="fc2dd-210">Constant in Sddl.h</span></span> | <span data-ttu-id="fc2dd-211">Значение право доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-211">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="fc2dd-212">RC</span><span class="sxs-lookup"><span data-stu-id="fc2dd-212">"RC"</span></span>                 | <span data-ttu-id="fc2dd-213">\_ \_ элемент управления SDDL Read</span><span class="sxs-lookup"><span data-stu-id="fc2dd-213">SDDL\_READ\_CONTROL</span></span> | <span data-ttu-id="fc2dd-214">\_Контроль чтения</span><span class="sxs-lookup"><span data-stu-id="fc2dd-214">READ\_CONTROL</span></span>      |
| <span data-ttu-id="fc2dd-215">ПАМЯТИ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-215">"SD"</span></span>                 | <span data-ttu-id="fc2dd-216">\_стандартное \_ Удаление SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-216">SDDL\_STANDARD\_DELETE</span></span> | <span data-ttu-id="fc2dd-217">DELETE</span><span class="sxs-lookup"><span data-stu-id="fc2dd-217">DELETE</span></span>          |
| <span data-ttu-id="fc2dd-218">WD</span><span class="sxs-lookup"><span data-stu-id="fc2dd-218">"WD"</span></span>                 | <span data-ttu-id="fc2dd-219">\_запись SDDL записи \_ DAC</span><span class="sxs-lookup"><span data-stu-id="fc2dd-219">SDDL\_WRITE\_DAC</span></span> | <span data-ttu-id="fc2dd-220">ЗАПИСЬ \_ DAC</span><span class="sxs-lookup"><span data-stu-id="fc2dd-220">WRITE\_DAC</span></span>            |
| <span data-ttu-id="fc2dd-221">ДВ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-221">"WO"</span></span>                 | <span data-ttu-id="fc2dd-222">\_владелец записи \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-222">SDDL\_WRITE\_OWNER</span></span> | <span data-ttu-id="fc2dd-223">\_владелец записи</span><span class="sxs-lookup"><span data-stu-id="fc2dd-223">WRITE\_OWNER</span></span>        |

### <a name="directory-service-object-access-rights"></a><span data-ttu-id="fc2dd-224">Права доступа к объекту службы каталогов</span><span class="sxs-lookup"><span data-stu-id="fc2dd-224">Directory service object access rights</span></span>

| <span data-ttu-id="fc2dd-225">Строка прав доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-225">Access rights string</span></span> | <span data-ttu-id="fc2dd-226">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="fc2dd-226">Constant in Sddl.h</span></span> | <span data-ttu-id="fc2dd-227">Значение право доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-227">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="fc2dd-228">RP</span><span class="sxs-lookup"><span data-stu-id="fc2dd-228">"RP"</span></span>                 | <span data-ttu-id="fc2dd-229">\_свойство чтения \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-229">SDDL\_READ\_PROPERTY</span></span> | <span data-ttu-id="fc2dd-230">AD — \_ право на \_ \_ чтение DS \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-230">ADS\_RIGHT\_DS\_READ\_PROP</span></span> |
| <span data-ttu-id="fc2dd-231">ВЧ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-231">"WP"</span></span>                 | <span data-ttu-id="fc2dd-232">\_свойство записи \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-232">SDDL\_WRITE\_PROPERTY</span></span> | <span data-ttu-id="fc2dd-233">Реклама \_ справа \_ DS \_ запись \_ prop</span><span class="sxs-lookup"><span data-stu-id="fc2dd-233">ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="fc2dd-234">КОМУ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-234">"CC"</span></span>                 | <span data-ttu-id="fc2dd-235">\_Создание \_ дочернего элемента SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-235">SDDL\_CREATE\_CHILD</span></span> | <span data-ttu-id="fc2dd-236">БАННЕРы \_ справа \_ \_ Создание \_ дочернего каталога</span><span class="sxs-lookup"><span data-stu-id="fc2dd-236">ADS\_RIGHT\_DS\_CREATE\_CHILD</span></span> |
| <span data-ttu-id="fc2dd-237">Постоянный</span><span class="sxs-lookup"><span data-stu-id="fc2dd-237">"DC"</span></span>                 | <span data-ttu-id="fc2dd-238">\_Удаление \_ дочернего элемента SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-238">SDDL\_DELETE\_CHILD</span></span> | <span data-ttu-id="fc2dd-239">Реклама \_ справа \_ DS \_ Удаление \_ дочернего элемента</span><span class="sxs-lookup"><span data-stu-id="fc2dd-239">ADS\_RIGHT\_DS\_DELETE\_CHILD</span></span> |
| <span data-ttu-id="fc2dd-240">АККРЕДИТИВ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-240">"LC"</span></span>                 | <span data-ttu-id="fc2dd-241">\_ \_ дочерние элементы списка SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-241">SDDL\_LIST\_CHILDREN</span></span> | <span data-ttu-id="fc2dd-242">\_ \_ список служб AD справа актрл \_ DS \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-242">ADS\_RIGHT\_ACTRL\_DS\_LIST</span></span> |
| <span data-ttu-id="fc2dd-243">СИНТЕЗАТОР</span><span class="sxs-lookup"><span data-stu-id="fc2dd-243">"SW"</span></span>                 | <span data-ttu-id="fc2dd-244">\_самостоятельная \_ запись SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-244">SDDL\_SELF\_WRITE</span></span>    | <span data-ttu-id="fc2dd-245">AD — \_ правая \_ доменная служба \_ Self</span><span class="sxs-lookup"><span data-stu-id="fc2dd-245">ADS\_RIGHT\_DS\_SELF</span></span> |
| <span data-ttu-id="fc2dd-246">Lo</span><span class="sxs-lookup"><span data-stu-id="fc2dd-246">"LO"</span></span>                  | <span data-ttu-id="fc2dd-247">\_объект списка \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-247">SDDL\_LIST\_OBJECT</span></span> | <span data-ttu-id="fc2dd-248">\_ \_ \_ объект списка DS right \_ AD</span><span class="sxs-lookup"><span data-stu-id="fc2dd-248">ADS\_RIGHT\_DS\_LIST\_OBJECT</span></span> |
| <span data-ttu-id="fc2dd-249">MICROSOF</span><span class="sxs-lookup"><span data-stu-id="fc2dd-249">"DT"</span></span>                 | <span data-ttu-id="fc2dd-250">\_дерево удаления \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-250">SDDL\_DELETE\_TREE</span></span> | <span data-ttu-id="fc2dd-251">\_дерево прав \_ Active Directory — \_ Удаление \_ дерева</span><span class="sxs-lookup"><span data-stu-id="fc2dd-251">ADS\_RIGHT\_DS\_DELETE\_TREE</span></span> |
| <span data-ttu-id="fc2dd-252">Кредит</span><span class="sxs-lookup"><span data-stu-id="fc2dd-252">"CR"</span></span>                  | <span data-ttu-id="fc2dd-253">\_доступ к элементу управления SDDL \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-253">SDDL\_CONTROL\_ACCESS</span></span> | <span data-ttu-id="fc2dd-254">AD \_ , \_ права \_ \_ доступа к управлению DS</span><span class="sxs-lookup"><span data-stu-id="fc2dd-254">ADS\_RIGHT\_DS\_CONTROL\_ACCESS</span></span> |

### <a name="file-access-rights"></a><span data-ttu-id="fc2dd-255">Права доступа к файлам</span><span class="sxs-lookup"><span data-stu-id="fc2dd-255">File access rights</span></span>

| <span data-ttu-id="fc2dd-256">Строка прав доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-256">Access rights string</span></span> | <span data-ttu-id="fc2dd-257">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="fc2dd-257">Constant in Sddl.h</span></span> | <span data-ttu-id="fc2dd-258">Значение право доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-258">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="fc2dd-259">СЕРИЮ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-259">"FA"</span></span>                 | <span data-ttu-id="fc2dd-260">\_файл SDDL \_ все</span><span class="sxs-lookup"><span data-stu-id="fc2dd-260">SDDL\_FILE\_ALL</span></span>    | <span data-ttu-id="fc2dd-261">ФАЙЛ \_ все \_ доступ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-261">FILE\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="fc2dd-262">ФРАНЦУЗСКИЙ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-262">"FR"</span></span>                 | <span data-ttu-id="fc2dd-263">\_чтение файла \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-263">SDDL\_FILE\_READ</span></span>   | <span data-ttu-id="fc2dd-264">\_Общее \_ чтение файла</span><span class="sxs-lookup"><span data-stu-id="fc2dd-264">FILE\_GENERIC\_READ</span></span> |
| <span data-ttu-id="fc2dd-265">ПРОЕКТОР</span><span class="sxs-lookup"><span data-stu-id="fc2dd-265">"FW"</span></span>                 | <span data-ttu-id="fc2dd-266">\_запись файла \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-266">SDDL\_FILE\_WRITE</span></span>  | <span data-ttu-id="fc2dd-267">\_Общая \_ запись в файл</span><span class="sxs-lookup"><span data-stu-id="fc2dd-267">FILE\_GENERIC\_WRITE</span></span> |
| <span data-ttu-id="fc2dd-268">FX</span><span class="sxs-lookup"><span data-stu-id="fc2dd-268">"FX"</span></span>                 | <span data-ttu-id="fc2dd-269">\_выполнение файла \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-269">SDDL\_FILE\_EXECUTE</span></span> | <span data-ttu-id="fc2dd-270">\_Общий \_ Запуск файла</span><span class="sxs-lookup"><span data-stu-id="fc2dd-270">FILE\_GENERIC\_EXECUTE</span></span> |


### <a name="registry-key-access-rights"></a><span data-ttu-id="fc2dd-271">Права доступа к разделу реестра</span><span class="sxs-lookup"><span data-stu-id="fc2dd-271">Registry key access rights</span></span>

| <span data-ttu-id="fc2dd-272">Строка прав доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-272">Access rights string</span></span> | <span data-ttu-id="fc2dd-273">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="fc2dd-273">Constant in Sddl.h</span></span> | <span data-ttu-id="fc2dd-274">Значение право доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-274">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="fc2dd-275">KA</span><span class="sxs-lookup"><span data-stu-id="fc2dd-275">"KA"</span></span>                 | <span data-ttu-id="fc2dd-276">\_все ключи \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-276">SDDL\_KEY\_ALL</span></span>     | <span data-ttu-id="fc2dd-277">КЛЮЧЕВОЙ \_ полный \_ доступ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-277">KEY\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="fc2dd-278">Республика Корея</span><span class="sxs-lookup"><span data-stu-id="fc2dd-278">"KR"</span></span>                 | <span data-ttu-id="fc2dd-279">\_чтение ключа \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-279">SDDL\_KEY\_READ</span></span>    | <span data-ttu-id="fc2dd-280">\_чтение ключа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-280">KEY\_READ</span></span>          |
| <span data-ttu-id="fc2dd-281">КВт \*</span><span class="sxs-lookup"><span data-stu-id="fc2dd-281">"KW"</span></span>                 | <span data-ttu-id="fc2dd-282">\_запись ключа \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-282">SDDL\_KEY\_WRITE</span></span>   | <span data-ttu-id="fc2dd-283">\_запись ключа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-283">KEY\_WRITE</span></span>         |
| <span data-ttu-id="fc2dd-284">"ККС"</span><span class="sxs-lookup"><span data-stu-id="fc2dd-284">"KX"</span></span>                 | <span data-ttu-id="fc2dd-285">\_выполнение ключа \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-285">SDDL\_KEY\_EXECUTE</span></span> | <span data-ttu-id="fc2dd-286">\_выполнение ключа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-286">KEY\_EXECUTE</span></span>       |

### <a name="mandatory-label-rights"></a><span data-ttu-id="fc2dd-287">Обязательные права для меток</span><span class="sxs-lookup"><span data-stu-id="fc2dd-287">Mandatory label rights</span></span>

| <span data-ttu-id="fc2dd-288">Строка прав доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-288">Access rights string</span></span> | <span data-ttu-id="fc2dd-289">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="fc2dd-289">Constant in Sddl.h</span></span> | <span data-ttu-id="fc2dd-290">Значение право доступа</span><span class="sxs-lookup"><span data-stu-id="fc2dd-290">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="fc2dd-291">Nr</span><span class="sxs-lookup"><span data-stu-id="fc2dd-291">"NR"</span></span>                 | <span data-ttu-id="fc2dd-292">SDDL \_ — \_ Чтение не производится \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-292">SDDL\_NO\_READ\_UP</span></span> | <span data-ttu-id="fc2dd-293">\_обязательная \_ Метка системы \_ не \_ читается \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-293">SYSTEM\_MANDATORY\_LABEL\_NO\_READ\_UP</span></span> |
| <span data-ttu-id="fc2dd-294">NW</span><span class="sxs-lookup"><span data-stu-id="fc2dd-294">"NW"</span></span>                 | <span data-ttu-id="fc2dd-295">\_запись SDDL без \_ записи \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-295">SDDL\_NO\_WRITE\_UP</span></span> | <span data-ttu-id="fc2dd-296">СИСТЕМная \_ обязательная \_ метка \_ без \_ записи \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-296">SYSTEM\_MANDATORY\_LABEL\_NO\_WRITE\_UP</span></span> |
| <span data-ttu-id="fc2dd-297">NX</span><span class="sxs-lookup"><span data-stu-id="fc2dd-297">"NX"</span></span>                 | <span data-ttu-id="fc2dd-298">SDDL \_ без \_ выполнения \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-298">SDDL\_NO\_EXECUTE\_UP</span></span> | <span data-ttu-id="fc2dd-299">\_обязательная система \_ метка \_ No не \_ выполняется \_</span><span class="sxs-lookup"><span data-stu-id="fc2dd-299">SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP</span></span> |
</dd> <dt>

<span data-ttu-id="fc2dd-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**\_GUID объекта**</span><span class="sxs-lookup"><span data-stu-id="fc2dd-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="fc2dd-301">Строковое представление идентификатора GUID, которое указывает значение элемента **ObjectType** структуры ACE, относящейся к объекту, например, [**доступное \_ \_ \_ ACE для объекта**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span><span class="sxs-lookup"><span data-stu-id="fc2dd-301">A string representation of a GUID that indicates the value of the **ObjectType** member of an object-specific ACE structure, such as [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span></span> <span data-ttu-id="fc2dd-302">Строка GUID использует формат, возвращаемый функцией [**ууидтостринг**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="fc2dd-302">The GUID string uses the format returned by the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) function.</span></span>

<span data-ttu-id="fc2dd-303">В следующей таблице перечислены некоторые часто используемые идентификаторы GUID объектов.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-303">The following table lists some commonly used object GUIDs.</span></span>



| <span data-ttu-id="fc2dd-304">Права и идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="fc2dd-304">Rights and GUID</span></span>                         | <span data-ttu-id="fc2dd-305">Разрешение</span><span class="sxs-lookup"><span data-stu-id="fc2dd-305">Permission</span></span>      |
|-----------------------------------------|-----------------|
| <span data-ttu-id="fc2dd-306">CR; ab721a53-1e2f-11D0-9819-00aa0040529b</span><span class="sxs-lookup"><span data-stu-id="fc2dd-306">CR;ab721a53-1e2f-11d0-9819-00aa0040529b</span></span> | <span data-ttu-id="fc2dd-307">Изменить пароль</span><span class="sxs-lookup"><span data-stu-id="fc2dd-307">Change password</span></span> |
| <span data-ttu-id="fc2dd-308">CR; 00299570-246d-11D0-a768-00aa006e0529</span><span class="sxs-lookup"><span data-stu-id="fc2dd-308">CR;00299570-246d-11d0-a768-00aa006e0529</span></span> | <span data-ttu-id="fc2dd-309">Сброс пароля</span><span class="sxs-lookup"><span data-stu-id="fc2dd-309">Reset password</span></span>  |



 

</dd> <dt>

<span data-ttu-id="fc2dd-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**наследование \_ \_ GUID объекта**</span><span class="sxs-lookup"><span data-stu-id="fc2dd-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**inherit\_object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="fc2dd-311">Строковое представление идентификатора GUID, которое указывает значение элемента **инхеритедобжекттипе** структуры ACE конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-311">A string representation of a GUID that indicates the value of the **InheritedObjectType** member of an object-specific ACE structure.</span></span> <span data-ttu-id="fc2dd-312">Строка GUID использует формат [**ууидтостринг**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="fc2dd-312">The GUID string uses the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) format.</span></span>

</dd> <dt>

<span data-ttu-id="fc2dd-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**Идентификатор безопасности учетной записи \_**</span><span class="sxs-lookup"><span data-stu-id="fc2dd-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account\_sid**</span></span>
</dt> <dd>

<span data-ttu-id="fc2dd-314">[Строка идентификатора безопасности](sid-strings.md) , определяющая [доверенное лицо](trustees.md) ACE.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-314">[SID string](sid-strings.md) that identifies the [trustee](trustees.md) of the ACE.</span></span>

</dd> <dt>

<span data-ttu-id="fc2dd-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**\_атрибут ресурса**</span><span class="sxs-lookup"><span data-stu-id="fc2dd-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**resource\_attribute**</span></span>
</dt> <dd>

<span data-ttu-id="fc2dd-316">\[Необязательный \] \_ атрибут ресурса предназначен только для ресурсов ACE ресурса и является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-316">\[OPTIONAL\] The resource\_attribute is only for resource ACEs and is optional.</span></span> <span data-ttu-id="fc2dd-317">Строка, указывающая тип данных.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-317">A string that indicates the data type.</span></span> <span data-ttu-id="fc2dd-318">Тип данных ACE атрибута ресурса может быть одним из следующих типов данных, определенных в SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-318">The resource attribute ace data type can be one of the following data types defined in Sddl.h.</span></span>

<span data-ttu-id="fc2dd-319">Знак " \# " является синонимом "0" в атрибутах ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-319">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="fc2dd-320">Например, Д:АИ (XA; ОИЦИ; FA;;; WD; (Октетстрингтипе = = \# 1 \# 2 \# 3 \# \# )) эквивалентен и интерпретируется как д:АИ (XA; оиЦи; FA;;; WD; (Октетстрингтипе = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="fc2dd-320">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

<span data-ttu-id="fc2dd-321">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista и Windows server 2003:** Атрибуты ресурсов недоступны.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-321">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Resource attributes are not available.</span></span>



| <span data-ttu-id="fc2dd-322">Строка типа данных ACE атрибута ресурса</span><span class="sxs-lookup"><span data-stu-id="fc2dd-322">Resource attribute ace data type string</span></span> | <span data-ttu-id="fc2dd-323">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="fc2dd-323">Constant in Sddl.h</span></span> | <span data-ttu-id="fc2dd-324">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fc2dd-324">Data type</span></span>        |
|-----------------------------------------|--------------------|------------------|
| <span data-ttu-id="fc2dd-325">Ti</span><span class="sxs-lookup"><span data-stu-id="fc2dd-325">"TI"</span></span>                                    | <span data-ttu-id="fc2dd-326">\_тип SDDL int</span><span class="sxs-lookup"><span data-stu-id="fc2dd-326">SDDL\_INT</span></span>          | <span data-ttu-id="fc2dd-327">Целое число со знаком</span><span class="sxs-lookup"><span data-stu-id="fc2dd-327">Signed integer</span></span>   |
| <span data-ttu-id="fc2dd-328">Tu</span><span class="sxs-lookup"><span data-stu-id="fc2dd-328">"TU"</span></span>                                    | <span data-ttu-id="fc2dd-329">SDDL \_ uint</span><span class="sxs-lookup"><span data-stu-id="fc2dd-329">SDDL\_UINT</span></span>         | <span data-ttu-id="fc2dd-330">Целое число без знака</span><span class="sxs-lookup"><span data-stu-id="fc2dd-330">Unsigned integer</span></span> |
| <span data-ttu-id="fc2dd-331">ЛИЦЕНЗИИ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-331">"TS"</span></span>                                    | <span data-ttu-id="fc2dd-332">\_WSTRING SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-332">SDDL\_WSTRING</span></span>      | <span data-ttu-id="fc2dd-333">Расширенная строка</span><span class="sxs-lookup"><span data-stu-id="fc2dd-333">Wide string</span></span>      |
| <span data-ttu-id="fc2dd-334"><</span><span class="sxs-lookup"><span data-stu-id="fc2dd-334">"TD"</span></span>                                    | <span data-ttu-id="fc2dd-335">\_идентификатор безопасности SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-335">SDDL\_SID</span></span>          | <span data-ttu-id="fc2dd-336">SID</span><span class="sxs-lookup"><span data-stu-id="fc2dd-336">SID</span></span>              |
| <span data-ttu-id="fc2dd-337">ДАНО</span><span class="sxs-lookup"><span data-stu-id="fc2dd-337">"TX"</span></span>                                    | <span data-ttu-id="fc2dd-338">\_большой двоичный объект SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-338">SDDL\_BLOB</span></span>         | <span data-ttu-id="fc2dd-339">Строка октета</span><span class="sxs-lookup"><span data-stu-id="fc2dd-339">Octet string</span></span>     |
| <span data-ttu-id="fc2dd-340">ТБАЙТ</span><span class="sxs-lookup"><span data-stu-id="fc2dd-340">"TB"</span></span>                                    | <span data-ttu-id="fc2dd-341">\_логическое значение SDDL</span><span class="sxs-lookup"><span data-stu-id="fc2dd-341">SDDL\_BOOLEAN</span></span>      | <span data-ttu-id="fc2dd-342">Логическое</span><span class="sxs-lookup"><span data-stu-id="fc2dd-342">Boolean</span></span>          |



 

</dd> </dl>

<span data-ttu-id="fc2dd-343">В следующем примере показана строка ACE для ACE, разрешенного доступом.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-343">The following example shows an ACE string for an access-allowed ACE.</span></span> <span data-ttu-id="fc2dd-344">Он не является элементом ACE, зависящим от объекта, поэтому он не имеет сведений **в \_ GUID объекта** и не **наследует поля \_ \_ GUID объекта** .</span><span class="sxs-lookup"><span data-stu-id="fc2dd-344">It is not an object-specific ACE, so it has no information in the **object\_guid** and **inherit\_object\_guid** fields.</span></span> <span data-ttu-id="fc2dd-345">Поле **\_ флагов ACE** также пусто, что означает, что ни один из флагов ACE не задан.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-345">The **ace\_flags** field is also empty, which indicates that none of the ACE flags are set.</span></span>


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



<span data-ttu-id="fc2dd-346">Приведенная выше строка ACE описывает следующие сведения ACE.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-346">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



<span data-ttu-id="fc2dd-347">В следующем примере показан файл, классифицированный с утверждениями ресурсов для Windows и язык SQL (SQL) с параметром PFS, имеющим значение высокий уровень влияния на бизнес.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-347">The following example shows a file classified with resource claims for Windows and Structured Query Language (SQL) with Secrecy set to High Business Impact.</span></span>


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



<span data-ttu-id="fc2dd-348">Приведенная выше строка ACE описывает следующие сведения ACE.</span><span class="sxs-lookup"><span data-stu-id="fc2dd-348">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



<span data-ttu-id="fc2dd-349">Дополнительные сведения см. в разделе [Формат строки дескриптора безопасности](security-descriptor-string-format.md) и [строки SID](sid-strings.md).</span><span class="sxs-lookup"><span data-stu-id="fc2dd-349">For more information, see [Security Descriptor String Format](security-descriptor-string-format.md) and [SID Strings](sid-strings.md).</span></span> <span data-ttu-id="fc2dd-350">Сведения об условных ACE см. в разделе [язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="fc2dd-350">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc2dd-351">См. также</span><span class="sxs-lookup"><span data-stu-id="fc2dd-351">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fc2dd-352">[\[MS-ДТИП \] : язык описания дескрипторов безопасности](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="fc2dd-352">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

