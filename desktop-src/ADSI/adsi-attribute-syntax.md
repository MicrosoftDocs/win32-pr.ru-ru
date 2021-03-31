---
title: Синтаксис атрибутов ADSI
description: С каждым атрибутом в каталоге связан синтаксис. Например, целое число, строка, число и т. д. ADSI определяет собственный синтаксис, соответствующий синтаксису собственного каталога. В этом разделе описываются типы синтаксиса атрибутов в ADSI.
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- атрибуты ADSI, синтаксис
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23d58b48b27fa88077f388b47535afd1dbd0a4f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793812"
---
# <a name="adsi-attribute-syntax"></a><span data-ttu-id="6b5ac-107">Синтаксис атрибутов ADSI</span><span class="sxs-lookup"><span data-stu-id="6b5ac-107">ADSI Attribute Syntax</span></span>

<span data-ttu-id="6b5ac-108">С каждым атрибутом в каталоге связан синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-108">Each attribute in the directory has an associated syntax.</span></span> <span data-ttu-id="6b5ac-109">Например, целое число, строка, число и т. д.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-109">For example, integer, string, numeric, and so on.</span></span> <span data-ttu-id="6b5ac-110">ADSI определяет собственный синтаксис, соответствующий синтаксису собственного каталога.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-110">ADSI defines its own syntax that maps to the native directory syntax.</span></span> <span data-ttu-id="6b5ac-111">В этом разделе описываются типы синтаксиса атрибутов в ADSI.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-111">This section describes the types of attribute syntaxes in ADSI.</span></span>

## <a name="distinguished-name-string"></a><span data-ttu-id="6b5ac-112">Строка различающегося имени</span><span class="sxs-lookup"><span data-stu-id="6b5ac-112">Distinguished Name String</span></span>


```VB
Syntax Type: ADSTYPE_DN_STRING
```



<span data-ttu-id="6b5ac-113">Различающееся имя удобно использовать для связи между двумя объектами.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-113">The distinguished name is useful for linking two objects together.</span></span> <span data-ttu-id="6b5ac-114">Например, он может создать ссылку, которая делает объект Алисы диспетчером объекта Bob.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-114">For example, it can create a link that makes the Alice object a manager of the Bob object.</span></span> <span data-ttu-id="6b5ac-115">Если объект Алисы перемещается в другое место, ссылка на диспетчер между Алисой и Бобом обновляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-115">If the Alice object moves to different place, the manager link between Alice and Bob is updated automatically.</span></span>

<span data-ttu-id="6b5ac-116">Различающееся имя должно содержать допустимый объект различающегося имени.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-116">The distinguished name must contain a valid distinguished name object.</span></span> <span data-ttu-id="6b5ac-117">Если различающееся имя не соответствует допустимому существующему объекту, большинство серверов отклоняет запрос и возвращает ошибку нарушения ограничения.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-117">If the distinguished name does not correspond to a valid existing object, most servers reject the request and return a constraint violation error.</span></span>

<span data-ttu-id="6b5ac-118">Примеры:</span><span class="sxs-lookup"><span data-stu-id="6b5ac-118">Examples:</span></span>


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a><span data-ttu-id="6b5ac-119">Строка с точным регистром и регистром символов</span><span class="sxs-lookup"><span data-stu-id="6b5ac-119">Case Exact String and Case Ignore String</span></span>


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



<span data-ttu-id="6b5ac-120">Точная строка Case учитывает регистр, а строка без учета регистра не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-120">Case Exact String is a case-sensitive string while Case Ignore String is a case-insensitive string.</span></span> <span data-ttu-id="6b5ac-121">Этот синтаксис используется в больших процентах атрибутов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-121">A large percentage of attributes in the directory use this syntax.</span></span>

> [!Note]  
> <span data-ttu-id="6b5ac-122">Каталог может или не может хранить его как строку в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-122">The directory may or may not store this as a Unicode string.</span></span> <span data-ttu-id="6b5ac-123">Однако ADSI принимает и возвращает строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-123">However, ADSI accepts and returns Unicode strings.</span></span>

 

<span data-ttu-id="6b5ac-124">Пример.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-124">Example:</span></span>


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a><span data-ttu-id="6b5ac-125">Печатная строка</span><span class="sxs-lookup"><span data-stu-id="6b5ac-125">Printable String</span></span>


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



<span data-ttu-id="6b5ac-126">Этот синтаксис используется для атрибутов со строковыми значениями, где прописные и строчные буквы считаются неравными для сравнений, например, "FABRIKAM" и "Fabrikam" не совпадают.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-126">This syntax is used for attributes with string values where uppercase and lowercase are considered unequal for comparisons, for example, "FABRIKAM" and "Fabrikam" do not match.</span></span> <span data-ttu-id="6b5ac-127">ADSI принимает любое содержимое для печатной строки; Он не пытается проверить, действительно ли они доступны для печати.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-127">ADSI accepts any contents for a Printable-String; it does not attempt to verify that they are indeed printable.</span></span>

## <a name="numeric-string"></a><span data-ttu-id="6b5ac-128">Числовая строка</span><span class="sxs-lookup"><span data-stu-id="6b5ac-128">Numeric String</span></span>


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



<span data-ttu-id="6b5ac-129">В этом синтаксисе строки совпадают, как в печатной строке, за исключением того, что все символы пробела игнорируются в сравнениях.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-129">In this syntax, strings match as in Printable String, except that all space characters are ignored in comparisons.</span></span> <span data-ttu-id="6b5ac-130">ADSI не выполняет проверку значений, чтобы убедиться в том, что в значениях этого синтаксиса отображаются только цифры и пробелы.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-130">ADSI does not perform value checking to ensure that only numerals and spaces appear in values of this syntax.</span></span> <span data-ttu-id="6b5ac-131">Active Directory принимает любое содержимое для числовой строки; Он не проверяет, являются ли символы числовыми.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-131">Active Directory accepts any content for a numeric string; it does not verify that the characters are numeric.</span></span>

## <a name="utc-time"></a><span data-ttu-id="6b5ac-132">Время в формате UTC</span><span class="sxs-lookup"><span data-stu-id="6b5ac-132">UTC Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="6b5ac-133">Этот синтаксис сохраняет дату и время в одной строке.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-133">This syntax stores the date and time in a single string.</span></span> <span data-ttu-id="6b5ac-134">Строковый формат состоит из трех Объединенных частей: (1) YYMMDD; (2) ЧЧММ или ЧЧММСС (оба допустимы); и (3) "Z", чтобы указать, что заданное время является временем по Гринвичу (GMT), или "+/-ХХММ", чтобы указать, что указанное время является местным временем с заданной разностной копией по ГРИНВИЧу.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-134">The string format consists of three concatenated parts: (1) YYMMDD; (2) HHMM or HHMMSS (both are acceptable); and (3) "Z" to indicate that the time given is Greenwich Mean Time (GMT), or "+/-HHMM" to indicate that the time given is local time with the given differential from GMT.</span></span> <span data-ttu-id="6b5ac-135">Разностное резервное копирование основано на формуле: GMT = Local + DIFFERENTIAL.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-135">The differential is based on the formula: GMT=Local+differential.</span></span>

> [!Note]  
> <span data-ttu-id="6b5ac-136">Первые две цифры года не хранятся в этой строке.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-136">The first two digits of the year are not stored in this string.</span></span>

 

<span data-ttu-id="6b5ac-137">Примерами допустимых значений являются "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503 + 0130".</span><span class="sxs-lookup"><span data-stu-id="6b5ac-137">Some examples of legal values are "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503+0130".</span></span> <span data-ttu-id="6b5ac-138">Эта строка хранится в виде однобайтовых символов ASCII, и с ней не хранится номер кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-138">This string is stored as single-byte ASCII characters, and no code page number is stored with it.</span></span>

<span data-ttu-id="6b5ac-139">Хотя сортировка поддерживается, она выполняется только в виде строки, учитывающей регистр символов ASCII, а не с помощью правильного интерпретации значения строк.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-139">Although ordering is supported, it is done only as an ASCII case-insensitive string sort, not by properly interpreting the meaning of the strings.</span></span>

<span data-ttu-id="6b5ac-140">Принимается любое допустимое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-140">Any valid string value is accepted.</span></span> <span data-ttu-id="6b5ac-141">Не предпринимается попытка убедиться, что строка содержит допустимую строку времени.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-141">No attempt is made to ensure that the string contains a valid time string.</span></span>

## <a name="generalized-time"></a><span data-ttu-id="6b5ac-142">Обобщенное время</span><span class="sxs-lookup"><span data-stu-id="6b5ac-142">Generalized Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="6b5ac-143">Если определен новый атрибут для хранения значений времени, следует использовать синтаксис Женерализедтиме.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-143">If a new attribute to store time values is being defined, the GeneralizedTime syntax should be used.</span></span> <span data-ttu-id="6b5ac-144">Синтаксис Женерализедтиме использует четыре символа для представления года вместо двух, как в Утктиме.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-144">GeneralizedTime syntax uses four characters to represent the year instead of two as with UTCTime.</span></span>

<span data-ttu-id="6b5ac-145">Формат синтаксиса Женерализедтиме — "YYYYMMDDHHMMSS. 0Z".</span><span class="sxs-lookup"><span data-stu-id="6b5ac-145">The format for the GeneralizedTime syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="6b5ac-146">Примером допустимого значения является "20010928060000.0 Z".</span><span class="sxs-lookup"><span data-stu-id="6b5ac-146">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="6b5ac-147">"Z" обозначает отсутствие разностного времени.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-147">The "Z" indicates no time differential.</span></span> <span data-ttu-id="6b5ac-148">Active Directory сохраняет дату и время как среднее время по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="6b5ac-148">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="6b5ac-149">Если значение времени не указано, по умолчанию используется значение GMT.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-149">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="6b5ac-150">Если время указано в часовом поясе, отличном от GMT, то разностное соединение между часовым поясом и GMT добавляется к строке вместо «Z» в формате «YYYYMMDDHHMMSS. 0 \[ +/- \] ЧЧММ».</span><span class="sxs-lookup"><span data-stu-id="6b5ac-150">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="6b5ac-151">Пример допустимого значения: "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="6b5ac-151">An example of an acceptable value is "20010928060000.0+0200".</span></span>

<span data-ttu-id="6b5ac-152">Разностное резервное копирование основано на формуле: GMT = Local + DIFFERENTIAL.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-152">The differential is based on the formula: GMT=Local+differential.</span></span>

## <a name="boolean"></a><span data-ttu-id="6b5ac-153">Логическое</span><span class="sxs-lookup"><span data-stu-id="6b5ac-153">Boolean</span></span>


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



<span data-ttu-id="6b5ac-154">Active Directory принимает для этого синтаксиса только 32-разрядное значение со знаком.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-154">Active Directory accepts only a signed 32-bit value for this syntax.</span></span> <span data-ttu-id="6b5ac-155">Он обрабатывает нуль как **false** и все ненулевые значения как **true**.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-155">It handles zero as **FALSE** and all nonzero values as **TRUE**.</span></span>

## <a name="integer"></a><span data-ttu-id="6b5ac-156">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="6b5ac-156">Integer</span></span>


```VB
Syntax Type: ADSTYPE_INTEGER
```



<span data-ttu-id="6b5ac-157">32-разрядное числовое значение со знаком.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-157">A 32-bit signed numeric value.</span></span>

## <a name="large-integer"></a><span data-ttu-id="6b5ac-158">Большое целое число</span><span class="sxs-lookup"><span data-stu-id="6b5ac-158">Large Integer</span></span>


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



<span data-ttu-id="6b5ac-159">64-разрядное числовое значение со знаком.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-159">A 64-bit signed numeric value.</span></span> <span data-ttu-id="6b5ac-160">Большие целые числа фактически реализуются как COM-объекты в интерфейсе [**иадсларжеинтежер**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) .</span><span class="sxs-lookup"><span data-stu-id="6b5ac-160">Large integers are actually implemented as COM objects on the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface.</span></span> <span data-ttu-id="6b5ac-161">Методы **хигхпарт** и **ловпарт** используются для доступа к 2 32-разрядным половинам длинного целочисленного значения.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-161">The **HighPart** and **LowPart** methods are used to access the two 32-bit halves of the large integer value.</span></span>

<span data-ttu-id="6b5ac-162">Пример.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-162">Example:</span></span>


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a><span data-ttu-id="6b5ac-163">Строка октета</span><span class="sxs-lookup"><span data-stu-id="6b5ac-163">Octet String</span></span>


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



<span data-ttu-id="6b5ac-164">Строка октета возвращается в виде массива вариантов байтов.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-164">An octet string is returned as a variant array of bytes.</span></span> <span data-ttu-id="6b5ac-165">Это количество октетов, за которыми следует ряд октетов.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-165">This consists of a size count (number of octets) followed by a series of octets.</span></span> <span data-ttu-id="6b5ac-166">Октет — это 8-разрядный байт, поэтому последовательность октетов представляет собой строку двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-166">An octet is an 8-bit byte, so a series of octets is a string of binary data.</span></span>

## <a name="object-class"></a><span data-ttu-id="6b5ac-167">Класс объекта</span><span class="sxs-lookup"><span data-stu-id="6b5ac-167">Object Class</span></span>


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



<span data-ttu-id="6b5ac-168">Класс объекта является уникальным идентификатором объекта для данного класса схемы.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-168">Object Class is a unique object identifier for a given schema class.</span></span> <span data-ttu-id="6b5ac-169">Класс каждого экземпляра объекта определяется атрибутом **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="6b5ac-169">The class of each object instance is identified by the **objectClass** attribute.</span></span> <span data-ttu-id="6b5ac-170">При создании можно никогда не изменять класс объекта.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-170">When created, you can never change an object class.</span></span> <span data-ttu-id="6b5ac-171">**objectClass** является многозначным атрибутом.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-171">**objectClass** is a multiple valued attribute.</span></span> <span data-ttu-id="6b5ac-172">Он перечисляет конкретный класс объекта и классы всех структурных или абстрактных классов, из которых был получен конкретный класс.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-172">It lists the specific class of the object, and the classes of all structural or abstract classes from which the specific class was derived.</span></span> <span data-ttu-id="6b5ac-173">Сюда входит Top, класс, из которого все остальные классы в конечном итоге являются производными.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-173">This includes Top, the class from which all other classes are ultimately derived.</span></span> <span data-ttu-id="6b5ac-174">В Active Directory не перечислены вспомогательные классы в атрибуте **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="6b5ac-174">Active Directory does not list auxiliary classes in the **objectClass** attribute.</span></span>

## <a name="security-descriptor"></a><span data-ttu-id="6b5ac-175">Дескриптор безопасности</span><span class="sxs-lookup"><span data-stu-id="6b5ac-175">Security Descriptor</span></span>


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



<span data-ttu-id="6b5ac-176">Права доступа определяют, какие возможности имеет субъект безопасности при попытке выполнить операцию с объектом Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-176">Access rights define what abilities a security principal has when it attempts to perform an operation on an Active Directory object.</span></span> <span data-ttu-id="6b5ac-177">Дескриптор безопасности описывает сведения об управлении доступом, связанные с объектом.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-177">A security descriptor describes the access control information associated with an object.</span></span>

<span data-ttu-id="6b5ac-178">Дескриптор безопасности хранится как свойство объекта каталога в свойстве **нтсекуритидескриптор** .</span><span class="sxs-lookup"><span data-stu-id="6b5ac-178">The security descriptor is stored as a property of a directory object in the **nTSecurityDescriptor** property.</span></span> <span data-ttu-id="6b5ac-179">Когда прошедший проверку подлинности пользователь пытается получить доступ к объекту каталога, сервер каталогов определяет предоставленный или запрещенный ему доступ на основе дескриптора безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-179">When an authenticated user attempts to access a directory object, the directory server determines the access granted or denied to the user based on the object security descriptor.</span></span>

<span data-ttu-id="6b5ac-180">Перечисление [**\_ \_ элементов \_ управления SD в ADS**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) определяет флаги управления для дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-180">The [**ADS\_SD\_CONTROL\_ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) enumeration specifies control flags for a security descriptor.</span></span>

<span data-ttu-id="6b5ac-181">В следующем примере кода показано, как получить дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="6b5ac-181">The following code example shows how to obtain a security descriptor.</span></span>


```VB
' Obtain a security descriptor.
Dim x as IADs
Dim sd as IADsSecurityDescriptor
Dim acl as IADsAccessControlList
 
Set x = GetObject("LDAP://DC=Fabrikam, DC=com")
Set sd = x.Get("nTSecurityDescriptor")
 
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
 
Set acl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
```



## <a name="related-topics"></a><span data-ttu-id="6b5ac-182">См. также</span><span class="sxs-lookup"><span data-stu-id="6b5ac-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b5ac-183">Синтаксис для атрибутов Active Directory</span><span class="sxs-lookup"><span data-stu-id="6b5ac-183">Syntaxes for Active Directory Attributes</span></span>](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[<span data-ttu-id="6b5ac-184">Выбор синтаксиса</span><span class="sxs-lookup"><span data-stu-id="6b5ac-184">Choosing a Syntax</span></span>](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[<span data-ttu-id="6b5ac-185">Как указать значения для сравнения</span><span class="sxs-lookup"><span data-stu-id="6b5ac-185">How to Specify Comparison Values</span></span>](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 