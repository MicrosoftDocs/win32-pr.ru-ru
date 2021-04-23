---
title: Сценарии LDIF
description: Формат обмена данными LDAP (LDIF) — это стандарт IETF, который определяет способ импорта и экспорта данных каталога между серверами каталогов, использующими поставщики служб LDAP.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- Active Directory скриптов LDIF
- Сценарии LDIF Active Directory, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e228e48770e1190065a16c95b4011f794127fbdd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103987219"
---
# <a name="ldif-scripts"></a><span data-ttu-id="1b0cc-105">Сценарии LDIF</span><span class="sxs-lookup"><span data-stu-id="1b0cc-105">LDIF Scripts</span></span>

<span data-ttu-id="1b0cc-106">Формат обмена данными LDAP (LDIF) — это стандарт IETF, который определяет способ импорта и экспорта данных каталога между серверами каталогов, использующими поставщики служб LDAP.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-106">The LDAP Data Interchange Format (LDIF) is an Internet Engineering Task Force (IETF) standard that defines how to import and export directory data between directory servers that use LDAP service providers.</span></span> <span data-ttu-id="1b0cc-107">Windows 2000 и Windows Server 2003 включают в себя программу командной строки LDIFDE, которая может использоваться для импорта объектов каталога в службы домен Active Directory Services с помощью LDIF-файлов.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-107">Windows 2000 and Windows Server 2003 include a command-line utility, LDIFDE, which can be used to import directory objects into Active Directory Domain Services using LDIF files.</span></span> <span data-ttu-id="1b0cc-108">LDIFDE позволяет задать фильтр для определенной строки, чтобы искать и перечислять объекты каталога в домен Active Directory Services в виде LDIF-файлов, которые могут быть легко прочитаны администраторами схемы.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-108">LDIFDE enables you to set a filter to a specific string in order to search for and list directory objects in Active Directory Domain Services as LDIF files which can be easily read by schema administrators.</span></span>

<span data-ttu-id="1b0cc-109">При импорте файла Юникода программа LDIFDE импортирует файл как Юникод, если он содержит идентификатор Юникода в начале файла.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-109">When importing a Unicode file, LDIFDE imports the file as Unicode if it contains the Unicode identifier at the beginning of the file.</span></span> <span data-ttu-id="1b0cc-110">Если вы хотите импортировать файл в формате Юникод, если он не содержит идентификатор Юникода в начале файла, можно использовать параметр-u, чтобы принудительно импортировать его в Юникод.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-110">If you wish to import a file as Unicode when it does not contain the Unicode identifier at the beginning of the file, you can use the -u switch in order to force it to be imported as Unicode.</span></span>

<span data-ttu-id="1b0cc-111">Режимом по умолчанию для экспорта файлов является ANSI.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-111">The default mode for exporting files is ANSI.</span></span> <span data-ttu-id="1b0cc-112">Если имеются записи в Юникоде, они будут преобразованы в базовый формат 64.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-112">If there are Unicode entries, they will be converted into base 64 format.</span></span> <span data-ttu-id="1b0cc-113">Чтобы экспортировать файл в формате Юникод, используйте параметр-u.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-113">To export a file into Unicode format, use the -u switch.</span></span>

<span data-ttu-id="1b0cc-114">LDIF-файл должен применять изменения схемы при наличии зависимостей между добавляемыми атрибутами.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-114">An LDIF file must apply schema changes when there are dependencies between the attributes that are added.</span></span> <span data-ttu-id="1b0cc-115">Например, необходимо добавить атрибуты прямой ссылки перед соответствующим атрибутом ссылки назад.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-115">For example, forward link attributes should be added before the corresponding back link attribute.</span></span> <span data-ttu-id="1b0cc-116">Кроме того, необходимо обновить кэш схемы перед добавлением классов, зависящих от атрибутов или классов, добавленных ранее в скрипте LDIF.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-116">You must also update the schema cache before adding classes that depend on attributes or classes added earlier in the LDIF script.</span></span> <span data-ttu-id="1b0cc-117">Дополнительные сведения см. в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-117">For more information, see the following code example.</span></span>

<span data-ttu-id="1b0cc-118">Имейте в виду, что для двоичных значений необходимо кодировать значения в формате Base64.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-118">Be aware that for binary values, you must encode the values as base64.</span></span> <span data-ttu-id="1b0cc-119">Кодировка base64 определяется в стандарте IETF RFC 2045, раздел 6,8.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-119">Base64 encoding is defined in IETF RFC 2045, Section 6.8.</span></span>

<span data-ttu-id="1b0cc-120">Дополнительные сведения о формате LDIF-файлов см. в статье [Спецификация формата обмена данными LDAP (LDIF)](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) на веб-сайте Web Engineering Task Force.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-120">For more information about the format of LDIF files, see [The LDAP Data Interchange Format (LDIF) - Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) on the Internet Engineering Task Force website.</span></span>

## <a name="ntds-specific-ldif-changetypes"></a><span data-ttu-id="1b0cc-121">LDIF-чанжетипес для конкретного NTDS</span><span class="sxs-lookup"><span data-stu-id="1b0cc-121">NTDS-specific LDIF changetypes</span></span>

<span data-ttu-id="1b0cc-122">Лучше использовать Нтдссчема \* чанжетипес вместо вызова ldifde-k.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-122">It is better to use ntdsSchema\* changetypes rather than calling ldifde -k.</span></span> <span data-ttu-id="1b0cc-123">Параметр-k команды ldifde игнорирует больший набор ошибок LDAP.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-123">The -k option of ldifde ignores a larger set of LDAP errors.</span></span> <span data-ttu-id="1b0cc-124">Полный список игнорируемых ошибок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b0cc-124">The complete list of ignored errors is as follows:</span></span>

-   <span data-ttu-id="1b0cc-125">Объект уже является членом группы.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-125">The object is already a member of the group.</span></span>
-   <span data-ttu-id="1b0cc-126">Нарушение класса объекта (то есть указанный класс объекта не существует), если импортируемый объект не имеет других атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-126">An object class violation (meaning the specified object class does not exist), if the object being imported has no other attributes.</span></span>
-   <span data-ttu-id="1b0cc-127">объект уже существует (**LDAP \_ уже \_ существует**)</span><span class="sxs-lookup"><span data-stu-id="1b0cc-127">object already exists (**LDAP\_ALREADY\_EXISTS**)</span></span>
-   <span data-ttu-id="1b0cc-128">нарушение ограничения (**\_ \_ нарушение ограничения LDAP**)</span><span class="sxs-lookup"><span data-stu-id="1b0cc-128">constraint violation (**LDAP\_CONSTRAINT\_VIOLATION**)</span></span>
-   <span data-ttu-id="1b0cc-129">атрибут или значение уже существует (**\_ атрибут \_ или значение \_ LDAP \_ существует**)</span><span class="sxs-lookup"><span data-stu-id="1b0cc-129">attribute or value already exists (**LDAP\_ATTRIBUTE\_OR\_VALUE\_EXISTS**)</span></span>
-   <span data-ttu-id="1b0cc-130">такой объект отсутствует (**LDAP \_ отсутствует \_ \_**)</span><span class="sxs-lookup"><span data-stu-id="1b0cc-130">no such object (**LDAP\_NO\_SUCH\_OBJECT**)</span></span>

<span data-ttu-id="1b0cc-131">Следующие чанжетипес предназначены специально для операций обновления схемы.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-131">The following changetypes are designed specifically for schema upgrade operations.</span></span>



| <span data-ttu-id="1b0cc-132">ChangeType</span><span class="sxs-lookup"><span data-stu-id="1b0cc-132">Changetype</span></span>                      | <span data-ttu-id="1b0cc-133">Описание</span><span class="sxs-lookup"><span data-stu-id="1b0cc-133">Description</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b0cc-134">**нтдссчемаадд**</span><span class="sxs-lookup"><span data-stu-id="1b0cc-134">**ntdsSchemaAdd**</span></span><br/>    | <span data-ttu-id="1b0cc-135">**нтдссчемаадд** соответствует **Add** в LDIF-файле.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-135">**ntdsSchemaAdd** corresponds to **add** in an LDIF file.</span></span> <span data-ttu-id="1b0cc-136">Единственное отличие заключается в том, что **нтдссчемаадд** может привести к тому, что ldifde будет пропускать операцию **добавления** , если объект уже существует в схеме.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-136">The only difference is that **ntdsSchemaAdd** would cause ldifde to skip an **add** operation if the object already exists in the schema.</span></span> <span data-ttu-id="1b0cc-137">(**Протокол LDAP \_ уже \_ существует** .)</span><span class="sxs-lookup"><span data-stu-id="1b0cc-137">(**LDAP\_ALREADY\_EXISTS** is ignored.)</span></span><br/>                                   |
| <span data-ttu-id="1b0cc-138">**нтдссчемамодифи**</span><span class="sxs-lookup"><span data-stu-id="1b0cc-138">**ntdsSchemaModify**</span></span><br/> | <span data-ttu-id="1b0cc-139">**нтдссчемамодифи** соответствует **ИЗМЕНЕНию** в LDIF-файле.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-139">**ntdsSchemaModify** corresponds to **modify** in an LDIF file.</span></span> <span data-ttu-id="1b0cc-140">Единственное отличие заключается в том, что **нтдссчемамодифи** может привести к тому, что ldifde будет пропускать операцию **изменения** , если объект не найден в схеме.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-140">The only difference is that **ntdsSchemaModify** would cause ldifde to skip an **modify** operation if the object is not found in the schema.</span></span> <span data-ttu-id="1b0cc-141">(**LDAP \_ не \_ \_** пропускается.)</span><span class="sxs-lookup"><span data-stu-id="1b0cc-141">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="1b0cc-142">**нтдссчемаделете**</span><span class="sxs-lookup"><span data-stu-id="1b0cc-142">**ntdsSchemaDelete**</span></span><br/> | <span data-ttu-id="1b0cc-143">**нтдссчемаделете** соответствует **УДАЛЕНию** в LDIF-файле.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-143">**ntdsSchemaDelete** corresponds to **delete** in an LDIF file.</span></span> <span data-ttu-id="1b0cc-144">Единственное отличие заключается в том, что **нтдссчемаделете** будет вызывать LDIFDE для пропуска операции **удаления** , если объект не найден в схеме.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-144">The only difference is that **ntdsSchemaDelete** would cause ldifde to skip an **delete** operation if the object is not found in the schema.</span></span> <span data-ttu-id="1b0cc-145">(**LDAP \_ не \_ \_** пропускается.)</span><span class="sxs-lookup"><span data-stu-id="1b0cc-145">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="1b0cc-146">**нтдссчемамодрдн**</span><span class="sxs-lookup"><span data-stu-id="1b0cc-146">**ntdsSchemaModRdn**</span></span><br/> | <span data-ttu-id="1b0cc-147">**нтдссчемамодрдн** соответствует **модрдн** в LDIF-файле.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-147">**ntdsSchemaModRdn** corresponds to **modrdn** in an LDIF file.</span></span> <span data-ttu-id="1b0cc-148">Единственное отличие заключается в том, что **нтдссчемамодрдн** может привести к тому, что LDIFDE пропустит операцию изменения относительного различающегося имени, если объект не найден в схеме.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-148">The only difference is that **ntdsSchemaModRdn** would cause ldifde to skip a modify-relative-distinguished-name operation if the object is not found in the schema.</span></span> <span data-ttu-id="1b0cc-149">(**LDAP \_ не \_ \_** пропускается.)</span><span class="sxs-lookup"><span data-stu-id="1b0cc-149">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/> |



 

## <a name="example"></a><span data-ttu-id="1b0cc-150">Пример</span><span class="sxs-lookup"><span data-stu-id="1b0cc-150">Example</span></span>

<span data-ttu-id="1b0cc-151">Следующий пример кода включает:</span><span class="sxs-lookup"><span data-stu-id="1b0cc-151">The following code example includes:</span></span>

-   <span data-ttu-id="1b0cc-152">Мисчемаекст. ldf — это сценарий LDIF, содержащий новые атрибуты и классы.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-152">Myschemaext.ldf is an LDIF script that contains new attributes and classes.</span></span> <span data-ttu-id="1b0cc-153">Имейте в виду, что этот файл является измененной версией файла, созданного на основе Lgetattcls.vbs.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-153">Be aware that this file is a modified version of the file generated from Lgetattcls.vbs.</span></span> <span data-ttu-id="1b0cc-154">Также имейте в виду, что атрибут **My-Test-Attribute-DN-FL** был перемещен впереди **My-Test-Attribute-DN-BL** , так как ссылка назад (**My-Test-Attribute-DN-BL**) зависит от прямой ссылки (**My-Test-Attribute-DN-FL**).</span><span class="sxs-lookup"><span data-stu-id="1b0cc-154">Also be aware that the **My-Test-Attribute-DN-FL** attribute was moved ahead of **My-Test-Attribute-DN-BL** because the back link (**My-Test-Attribute-DN-BL**) is dependent on the forward link (**My-Test-Attribute-DN-FL**).</span></span> <span data-ttu-id="1b0cc-155">Более того, Рабочий атрибут **счемаупдатенов** задается в двух местах для активации обновлений кэша схемы, так что зависимые атрибуты и классы будут доступны для добавления двух классов в скрипте.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-155">Furthermore, the **schemaUpdateNow** operational attribute is set in two places to trigger updates of the schema cache so that dependent attributes and classes will be available for adding the two classes in the script.</span></span>
    > [!Note]  
    > <span data-ttu-id="1b0cc-156">Сведения об источнике идентификатора в инструкциях linkID: см. в разделе [Получение идентификатора ссылки](obtaining-a-link-id.md) .</span><span class="sxs-lookup"><span data-stu-id="1b0cc-156">See the topic [Obtaining a Link ID](obtaining-a-link-id.md) for information about the source of the ID in the linkID: statements.</span></span>

     

-   <span data-ttu-id="1b0cc-157">Lgetattcls.vbs — это файл VBScript, который создает скрипт LDIF, используемый в качестве начальной точки для Мисчемаекст. ldf.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-157">Lgetattcls.vbs is a VBScript file that generates the LDIF script used as the starting point for the Myschemaext.ldf.</span></span> <span data-ttu-id="1b0cc-158">Имейте в виду, что путь к текущей схеме заменяется CN = Schema, CN = Configuration, DC = мйорг, DC = com.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-158">Be aware that the current schema path is replaced by CN=Schema,CN=Configuration,DC=myorg,DC=com.</span></span> <span data-ttu-id="1b0cc-159">Вы можете заменить DC = мйорг, DC = com на отразить различающееся имя (DN) для публикации в скрипте LDIF, чтобы в LSETATTCLS.VBS отражалось изменение в его **сфромдн** , чтобы при применении сценария LDIF заменялись правильные DN.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-159">You can replace DC=myorg,DC=com to reflect the distinguished name (DN) to publish in the LDIF script  ensure that LSETATTCLS.VBS reflects the change in its **sFromDN** so that the correct DN is replaced when the LDIF script is applied.</span></span> <span data-ttu-id="1b0cc-160">Также имейте в виду, что скрипт использует префикс для поиска классов и атрибутов, которые также необходимо определить, и использовать префикс для всех классов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-160">Also be aware that the script uses a prefix to find the classes and attributes you should also define and use a prefix for all your classes and attributes.</span></span> <span data-ttu-id="1b0cc-161">Дополнительные сведения см. в разделе [именование атрибутов и классов](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1b0cc-161">For more information, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span> <span data-ttu-id="1b0cc-162">Кроме того, сценарий выводит в LDIF-файл только необходимые атрибуты для объектов **attributeSchema** и **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="1b0cc-162">In addition, the script outputs only the necessary attributes for the **attributeSchema** and **classSchema** objects to the LDIF file.</span></span>
-   <span data-ttu-id="1b0cc-163">Lsetattcls.vbs — это файл VBScript, который использует скрипт Мисчемаекст. LDF для добавления новых атрибутов и классов в скрипт.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-163">Lsetattcls.vbs is a VBScript file that uses the Myschemaext.ldf script to add the new attributes and classes in the script.</span></span> <span data-ttu-id="1b0cc-164">Перед выполнением скрипта убедитесь, что хозяин схемы может быть записан в.</span><span class="sxs-lookup"><span data-stu-id="1b0cc-164">Ensure that the schema master is able to be written to before running the script.</span></span>

## <a name="myschemaextldf"></a><span data-ttu-id="1b0cc-165">МИСЧЕМАЕКСТ. LDF</span><span class="sxs-lookup"><span data-stu-id="1b0cc-165">MYSCHEMAEXT.LDF</span></span>

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a><span data-ttu-id="1b0cc-166">LGETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="1b0cc-166">LGETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a><span data-ttu-id="1b0cc-167">LSETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="1b0cc-167">LSETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





