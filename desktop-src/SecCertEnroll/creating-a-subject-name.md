---
description: Для создания имени субъекта из строки различающегося имени можно использовать интерфейс IX500DistinguishedName.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Создание имени субъекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540154"
---
# <a name="creating-a-subject-name"></a><span data-ttu-id="dbca6-103">Создание имени субъекта</span><span class="sxs-lookup"><span data-stu-id="dbca6-103">Creating a Subject Name</span></span>

<span data-ttu-id="dbca6-104">Для создания имени субъекта из строки различающегося имени можно использовать интерфейс [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .</span><span class="sxs-lookup"><span data-stu-id="dbca6-104">You can use the [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) interface to create a subject name from a distinguished name string.</span></span> <span data-ttu-id="dbca6-105">Строка состоит из сцепленных относительных различающихся имен (Рднс).</span><span class="sxs-lookup"><span data-stu-id="dbca6-105">The string consists of concatenated relative distinguished names (RDNs).</span></span> <span data-ttu-id="dbca6-106">API регистрации сертификатов поддерживает следующие ключи RDN.</span><span class="sxs-lookup"><span data-stu-id="dbca6-106">The following RDN keys are supported by the Certificate Enrollment API.</span></span>

| <span data-ttu-id="dbca6-107">Ключ</span><span class="sxs-lookup"><span data-stu-id="dbca6-107">Key</span></span>                               | <span data-ttu-id="dbca6-108">OID</span><span class="sxs-lookup"><span data-stu-id="dbca6-108">OID</span></span>                                             | <span data-ttu-id="dbca6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dbca6-109">Description</span></span>                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbca6-110">C</span><span class="sxs-lookup"><span data-stu-id="dbca6-110">C</span></span><br/>                      | <span data-ttu-id="dbca6-111">\_ \_ имя страны кскн \_ OID</span><span class="sxs-lookup"><span data-stu-id="dbca6-111">XCN\_OID\_COUNTRY\_NAME</span></span><br/>              | <span data-ttu-id="dbca6-112">Содержит двухбуквенный код страны ISO 3166 или регион.</span><span class="sxs-lookup"><span data-stu-id="dbca6-112">Contains a two-letter ISO 3166 country or region code.</span></span><br/>                                  |
| <span data-ttu-id="dbca6-113">CN</span><span class="sxs-lookup"><span data-stu-id="dbca6-113">CN</span></span><br/>                     | <span data-ttu-id="dbca6-114">\_ \_ Общее имя OID \_ кскн</span><span class="sxs-lookup"><span data-stu-id="dbca6-114">XCN\_OID\_COMMON\_NAME</span></span><br/>               | <span data-ttu-id="dbca6-115">Содержит общее имя.</span><span class="sxs-lookup"><span data-stu-id="dbca6-115">Contains a common name.</span></span><br/>                                                                 |
| <span data-ttu-id="dbca6-116">E</span><span class="sxs-lookup"><span data-stu-id="dbca6-116">E</span></span><br/> <span data-ttu-id="dbca6-117">Отправить по электронной почте</span><span class="sxs-lookup"><span data-stu-id="dbca6-117">EMAIL</span></span><br/>     | <span data-ttu-id="dbca6-118">КСКН \_ OID \_ RSA \_ емаиладдр</span><span class="sxs-lookup"><span data-stu-id="dbca6-118">XCN\_OID\_RSA\_emailAddr</span></span><br/>             | <span data-ttu-id="dbca6-119">Содержит адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="dbca6-119">Contains an email address.</span></span><br/>                                                              |
| <span data-ttu-id="dbca6-120">DC</span><span class="sxs-lookup"><span data-stu-id="dbca6-120">DC</span></span><br/>                     | <span data-ttu-id="dbca6-121">\_ \_ Компонент домена кскн \_ OID</span><span class="sxs-lookup"><span data-stu-id="dbca6-121">XCN\_OID\_DOMAIN\_COMPONENT</span></span><br/>          | <span data-ttu-id="dbca6-122">Содержит одну часть имени системы доменных имен (DNS).</span><span class="sxs-lookup"><span data-stu-id="dbca6-122">Contains one part of a Domain Name System (DNS) name.</span></span><br/>                                   |
| <span data-ttu-id="dbca6-123">G</span><span class="sxs-lookup"><span data-stu-id="dbca6-123">G</span></span><br/> <span data-ttu-id="dbca6-124">GivenName</span><span class="sxs-lookup"><span data-stu-id="dbca6-124">GivenName</span></span><br/> | <span data-ttu-id="dbca6-125">\_заданное \_ \_ имя OID кскн</span><span class="sxs-lookup"><span data-stu-id="dbca6-125">XCN\_OID\_GIVEN\_NAME</span></span><br/>                | <span data-ttu-id="dbca6-126">Содержит часть имени человека, которая не является фамилией.</span><span class="sxs-lookup"><span data-stu-id="dbca6-126">Contains the part of a person's name that is not a surname.</span></span><br/>                             |
| <span data-ttu-id="dbca6-127">I</span><span class="sxs-lookup"><span data-stu-id="dbca6-127">I</span></span><br/>                      | <span data-ttu-id="dbca6-128">\_ \_ инициалы OID кскн</span><span class="sxs-lookup"><span data-stu-id="dbca6-128">XCN\_OID\_INITIALS</span></span><br/>                   | <span data-ttu-id="dbca6-129">Содержит инициалы пользователя.</span><span class="sxs-lookup"><span data-stu-id="dbca6-129">Contains a person's initials.</span></span><br/>                                                           |
| <span data-ttu-id="dbca6-130">L</span><span class="sxs-lookup"><span data-stu-id="dbca6-130">L</span></span><br/>                      | <span data-ttu-id="dbca6-131">\_ \_ имя локальной OID кскн \_</span><span class="sxs-lookup"><span data-stu-id="dbca6-131">XCN\_OID\_LOCALITY\_NAME</span></span><br/>             | <span data-ttu-id="dbca6-132">Содержит имя, определяющее город, страну или другой географический регион.</span><span class="sxs-lookup"><span data-stu-id="dbca6-132">Contains the locality name that identifies a city, country, or other geographic region.</span></span><br/> |
| <span data-ttu-id="dbca6-133">O</span><span class="sxs-lookup"><span data-stu-id="dbca6-133">O</span></span><br/>                      | <span data-ttu-id="dbca6-134">\_имя кскн OID \_ организации \_</span><span class="sxs-lookup"><span data-stu-id="dbca6-134">XCN\_OID\_ORGANIZATION\_NAME</span></span><br/>         | <span data-ttu-id="dbca6-135">Содержит имя Организации.</span><span class="sxs-lookup"><span data-stu-id="dbca6-135">Contains the name of an organization.</span></span><br/>                                                   |
| <span data-ttu-id="dbca6-136">OU</span><span class="sxs-lookup"><span data-stu-id="dbca6-136">OU</span></span><br/>                     | <span data-ttu-id="dbca6-137">\_ \_ имя подразделения OID \_ кскн \_</span><span class="sxs-lookup"><span data-stu-id="dbca6-137">XCN\_OID\_ORGANIZATIONAL\_UNIT\_NAME</span></span><br/> | <span data-ttu-id="dbca6-138">Содержит имя подразделений единиц в пределах организации.</span><span class="sxs-lookup"><span data-stu-id="dbca6-138">Contains the name of a unit subdivision within an organization.</span></span><br/>                         |
| <span data-ttu-id="dbca6-139">S</span><span class="sxs-lookup"><span data-stu-id="dbca6-139">S</span></span><br/> <span data-ttu-id="dbca6-140">ST</span><span class="sxs-lookup"><span data-stu-id="dbca6-140">ST</span></span><br/>        | <span data-ttu-id="dbca6-141">\_ \_ \_ \_ имя или Республика \_ кскн OID</span><span class="sxs-lookup"><span data-stu-id="dbca6-141">XCN\_OID\_STATE\_OR\_PROVINCE\_NAME</span></span><br/>  | <span data-ttu-id="dbca6-142">Содержит полное имя штата или Республики.</span><span class="sxs-lookup"><span data-stu-id="dbca6-142">Contains the full name of a state or province.</span></span><br/>                                          |
| <span data-ttu-id="dbca6-143">STREET</span><span class="sxs-lookup"><span data-stu-id="dbca6-143">STREET</span></span><br/>                 | <span data-ttu-id="dbca6-144">\_ \_ почтовый адрес OID \_ кскн</span><span class="sxs-lookup"><span data-stu-id="dbca6-144">XCN\_OID\_STREET\_ADDRESS</span></span><br/>            | <span data-ttu-id="dbca6-145">Содержит физический адрес.</span><span class="sxs-lookup"><span data-stu-id="dbca6-145">Contains the physical address.</span></span><br/>                                                          |
| <span data-ttu-id="dbca6-146">SN</span><span class="sxs-lookup"><span data-stu-id="dbca6-146">SN</span></span><br/>                     | <span data-ttu-id="dbca6-147">\_ \_ имя Sur OID \_ кскн</span><span class="sxs-lookup"><span data-stu-id="dbca6-147">XCN\_OID\_SUR\_NAME</span></span><br/>                  | <span data-ttu-id="dbca6-148">Содержит имя семейства человека.</span><span class="sxs-lookup"><span data-stu-id="dbca6-148">Contains the family name of a person.</span></span><br/>                                                   |
| <span data-ttu-id="dbca6-149">T</span><span class="sxs-lookup"><span data-stu-id="dbca6-149">T</span></span><br/> <span data-ttu-id="dbca6-150">TITLE</span><span class="sxs-lookup"><span data-stu-id="dbca6-150">TITLE</span></span><br/>     | <span data-ttu-id="dbca6-151">\_заголовок OID \_ кскн</span><span class="sxs-lookup"><span data-stu-id="dbca6-151">XCN\_OID\_TITLE</span></span><br/>                      | <span data-ttu-id="dbca6-152">Содержит название сотрудника в Организации.</span><span class="sxs-lookup"><span data-stu-id="dbca6-152">Contains the title of a person in the organization.</span></span><br/>                                     |



 

<span data-ttu-id="dbca6-153">При инициализации объекта [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) можно определить формат различающегося имени, указав значение из типа перечисления [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) .</span><span class="sxs-lookup"><span data-stu-id="dbca6-153">When you initialize an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, you can identify the format of the distinguished name by specifying a value from the [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) enumeration type.</span></span> <span data-ttu-id="dbca6-154">Например, предположим, что различающееся имя субъекта состоит из следующих Рднс:</span><span class="sxs-lookup"><span data-stu-id="dbca6-154">For example, assume that the subject distinguished name consists of the following RDNs:</span></span><dl> <span data-ttu-id="dbca6-155">CN = администратор</span><span class="sxs-lookup"><span data-stu-id="dbca6-155">CN=Administrator</span></span>  
<span data-ttu-id="dbca6-156">CN = пользователи</span><span class="sxs-lookup"><span data-stu-id="dbca6-156">CN=Users</span></span>  
<span data-ttu-id="dbca6-157">DC = ждомкск</span><span class="sxs-lookup"><span data-stu-id="dbca6-157">DC=jdomcsc</span></span>  
<span data-ttu-id="dbca6-158">DC = нттест</span><span class="sxs-lookup"><span data-stu-id="dbca6-158">DC=nttest</span></span>  
<span data-ttu-id="dbca6-159">DC = Microsoft</span><span class="sxs-lookup"><span data-stu-id="dbca6-159">DC=microsoft</span></span>  
<span data-ttu-id="dbca6-160">DC = com</span><span class="sxs-lookup"><span data-stu-id="dbca6-160">DC=com</span></span>  
</dl>

<span data-ttu-id="dbca6-161">При объединении этих Рднс в следующую строку различающегося имени с разделителями-запятыми можно указать значение **\_ \_ \_ \_ \_ флага кскн для имени сертификата str** при инициализации объекта [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .</span><span class="sxs-lookup"><span data-stu-id="dbca6-161">If you concatenate these RDNs into the following comma-delimited distinguished name string, you can specify the **XCN\_CERT\_NAME\_STR\_COMMA\_FLAG** value when initializing an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object.</span></span>

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a><span data-ttu-id="dbca6-162">См. также</span><span class="sxs-lookup"><span data-stu-id="dbca6-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbca6-163">Кодирование имени субъекта</span><span class="sxs-lookup"><span data-stu-id="dbca6-163">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)
</dt> <dt>

[<span data-ttu-id="dbca6-164">Имена субъектов</span><span class="sxs-lookup"><span data-stu-id="dbca6-164">Subject Names</span></span>](subject-names.md)
</dt> </dl>

 

 




