---
description: '\_Тип перечисления "CAPICOM Certificate \_ Find \_ Type" определяет тип условий поиска, используемый для поиска конкретных сертификатов. Этот тип перечисления появился в CAPICOM 2,0.'
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: Перечисление CAPICOM_CERTIFICATE_FIND_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665245"
---
# <a name="capicom_certificate_find_type-enumeration"></a><span data-ttu-id="081e3-104">\_ \_ Перечисление типов поиска для сертификата CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="081e3-104">CAPICOM\_CERTIFICATE\_FIND\_TYPE enumeration</span></span>

<span data-ttu-id="081e3-105">Тип перечисления " **CAPICOM \_ Certificate \_ Find \_ Type** " определяет тип условий поиска, используемый для поиска конкретных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="081e3-105">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type defines the type of search criteria used to find specific certificates.</span></span> <span data-ttu-id="081e3-106">Этот тип перечисления появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="081e3-106">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="081e3-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="081e3-107">Members</span></span>



| <span data-ttu-id="081e3-108">Член</span><span class="sxs-lookup"><span data-stu-id="081e3-108">Member</span></span>                                                | <span data-ttu-id="081e3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="081e3-109">Description</span></span>                                                                                                                                 | <span data-ttu-id="081e3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="081e3-110">Value</span></span> |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="081e3-111">**CAPICOM \_ Certificate \_ найти \_ \_ хэш SHA1**</span><span class="sxs-lookup"><span data-stu-id="081e3-111">**CAPICOM\_CERTIFICATE\_FIND\_SHA1\_HASH**</span></span>            | <span data-ttu-id="081e3-112">Возвращает сертификаты, соответствующие указанному хэшу SHA1.</span><span class="sxs-lookup"><span data-stu-id="081e3-112">Returns certificates matching a specified SHA1 hash.</span></span><br/>                                                                             | <span data-ttu-id="081e3-113">0</span><span class="sxs-lookup"><span data-stu-id="081e3-113">0</span></span>     |
| <span data-ttu-id="081e3-114">**CAPICOM \_ Certificate \_ найти \_ имя субъекта \_**</span><span class="sxs-lookup"><span data-stu-id="081e3-114">**CAPICOM\_CERTIFICATE\_FIND\_SUBJECT\_NAME**</span></span>         | <span data-ttu-id="081e3-115">Возвращает сертификаты, имена субъектов которых полностью или частично совпадают с указанным именем субъекта.</span><span class="sxs-lookup"><span data-stu-id="081e3-115">Returns certificates whose subject name exactly or partially matches a specified subject name.</span></span><br/>                                   | <span data-ttu-id="081e3-116">1</span><span class="sxs-lookup"><span data-stu-id="081e3-116">1</span></span>     |
| <span data-ttu-id="081e3-117">**CAPICOM \_ Certificate \_ найти \_ \_ имя издателя**</span><span class="sxs-lookup"><span data-stu-id="081e3-117">**CAPICOM\_CERTIFICATE\_FIND\_ISSUER\_NAME**</span></span>          | <span data-ttu-id="081e3-118">Возвращает сертификаты, имя издателя которых полностью или частично совпадает с указанным именем издателя.</span><span class="sxs-lookup"><span data-stu-id="081e3-118">Returns certificates whose issuer name exactly or partially matches a specified issuer name.</span></span><br/>                                     | <span data-ttu-id="081e3-119">2</span><span class="sxs-lookup"><span data-stu-id="081e3-119">2</span></span>     |
| <span data-ttu-id="081e3-120">**\_ \_ \_ имя корневого узла поиска CAPICOM Certificate \_**</span><span class="sxs-lookup"><span data-stu-id="081e3-120">**CAPICOM\_CERTIFICATE\_FIND\_ROOT\_NAME**</span></span>            | <span data-ttu-id="081e3-121">Возвращает сертификаты, имя корневого субъекта которых полностью или частично совпадает с указанным корневым именем субъекта.</span><span class="sxs-lookup"><span data-stu-id="081e3-121">Returns certificates whose root subject name exactly or partially matches a specified root subject name.</span></span><br/>                         | <span data-ttu-id="081e3-122">3</span><span class="sxs-lookup"><span data-stu-id="081e3-122">3</span></span>     |
| <span data-ttu-id="081e3-123">**\_ \_ \_ имя шаблона поиска CAPICOM \_ Certificate**</span><span class="sxs-lookup"><span data-stu-id="081e3-123">**CAPICOM\_CERTIFICATE\_FIND\_TEMPLATE\_NAME**</span></span>        | <span data-ttu-id="081e3-124">Возвращает сертификаты, имя шаблона которых соответствует указанному имени шаблона.</span><span class="sxs-lookup"><span data-stu-id="081e3-124">Returns certificates whose template name matches a specified template name.</span></span><br/>                                                      | <span data-ttu-id="081e3-125">4</span><span class="sxs-lookup"><span data-stu-id="081e3-125">4</span></span>     |
| <span data-ttu-id="081e3-126">**\_ \_ найти расширение CAPICOM \_ Certificate**</span><span class="sxs-lookup"><span data-stu-id="081e3-126">**CAPICOM\_CERTIFICATE\_FIND\_EXTENSION**</span></span>             | <span data-ttu-id="081e3-127">Возвращает сертификаты, имеющие расширение, соответствующее указанному расширению.</span><span class="sxs-lookup"><span data-stu-id="081e3-127">Returns certificates that have an extension that matches a specified extension.</span></span><br/>                                                  | <span data-ttu-id="081e3-128">5</span><span class="sxs-lookup"><span data-stu-id="081e3-128">5</span></span>     |
| <span data-ttu-id="081e3-129">**\_ \_ \_ Расширенное свойство поиска CAPICOM Certificate \_**</span><span class="sxs-lookup"><span data-stu-id="081e3-129">**CAPICOM\_CERTIFICATE\_FIND\_EXTENDED\_PROPERTY**</span></span>    | <span data-ttu-id="081e3-130">Возвращает сертификаты с расширенным свойством, идентификатор свойства которого соответствует указанному идентификатору свойства.</span><span class="sxs-lookup"><span data-stu-id="081e3-130">Returns certificates that have an extended property whose property identifier matches a specified property identifier.</span></span><br/>           | <span data-ttu-id="081e3-131">6</span><span class="sxs-lookup"><span data-stu-id="081e3-131">6</span></span>     |
| <span data-ttu-id="081e3-132">**CAPICOM \_ Certificate \_ найти \_ \_ политику приложения**</span><span class="sxs-lookup"><span data-stu-id="081e3-132">**CAPICOM\_CERTIFICATE\_FIND\_APPLICATION\_POLICY**</span></span>   | <span data-ttu-id="081e3-133">Возвращает сертификаты в хранилище, которые имеют расширение или свойство расширенного использования ключа, Объединенные с идентификатором использования.</span><span class="sxs-lookup"><span data-stu-id="081e3-133">Returns certificates in the store that have either an enhanced key usage extension or property combined with a usage identifier.</span></span><br/> | <span data-ttu-id="081e3-134">7</span><span class="sxs-lookup"><span data-stu-id="081e3-134">7</span></span>     |
| <span data-ttu-id="081e3-135">**CAPICOM \_ Certificate \_ Поиск \_ \_ политики сертификата**</span><span class="sxs-lookup"><span data-stu-id="081e3-135">**CAPICOM\_CERTIFICATE\_FIND\_CERTIFICATE\_POLICY**</span></span>   | <span data-ttu-id="081e3-136">Возвращает сертификаты, содержащие указанный OID политики.</span><span class="sxs-lookup"><span data-stu-id="081e3-136">Returns certificates containing a specified policy OID.</span></span><br/>                                                                          | <span data-ttu-id="081e3-137">8</span><span class="sxs-lookup"><span data-stu-id="081e3-137">8</span></span>     |
| <span data-ttu-id="081e3-138">**\_ \_ \_ допустимое время поиска CAPICOM Certificate \_**</span><span class="sxs-lookup"><span data-stu-id="081e3-138">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID**</span></span>           | <span data-ttu-id="081e3-139">Возвращает сертификаты, время которых допустимо.</span><span class="sxs-lookup"><span data-stu-id="081e3-139">Returns certificates whose time is valid.</span></span><br/>                                                                                        | <span data-ttu-id="081e3-140">9</span><span class="sxs-lookup"><span data-stu-id="081e3-140">9</span></span>     |
| <span data-ttu-id="081e3-141">**\_ \_ \_ недействительное время \_ \_ \_ поиска CAPICOM Certificate**</span><span class="sxs-lookup"><span data-stu-id="081e3-141">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID**</span></span> | <span data-ttu-id="081e3-142">Возвращает сертификаты, время которых еще не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="081e3-142">Returns certificates whose time is not yet valid.</span></span><br/>                                                                                | <span data-ttu-id="081e3-143">10</span><span class="sxs-lookup"><span data-stu-id="081e3-143">10</span></span>    |
| <span data-ttu-id="081e3-144">**\_время поиска CAPICOM Certificate истекло \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="081e3-144">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED**</span></span>         | <span data-ttu-id="081e3-145">Возвращает сертификаты, время которых истекло.</span><span class="sxs-lookup"><span data-stu-id="081e3-145">Returns certificates whose time has expired.</span></span><br/>                                                                                     | <span data-ttu-id="081e3-146">11</span><span class="sxs-lookup"><span data-stu-id="081e3-146">11</span></span>    |
| <span data-ttu-id="081e3-147">**\_Использование CAPICOM Certificate \_ Поиск \_ ключа \_**</span><span class="sxs-lookup"><span data-stu-id="081e3-147">**CAPICOM\_CERTIFICATE\_FIND\_KEY\_USAGE**</span></span>            | <span data-ttu-id="081e3-148">Возвращает сертификаты, содержащие ключ, который можно использовать указанным образом.</span><span class="sxs-lookup"><span data-stu-id="081e3-148">Returns certificates containing a key that can be used in the specified manner.</span></span><br/>                                                  | <span data-ttu-id="081e3-149">12</span><span class="sxs-lookup"><span data-stu-id="081e3-149">12</span></span>    |



## <a name="remarks"></a><span data-ttu-id="081e3-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="081e3-150">Remarks</span></span>

<span data-ttu-id="081e3-151">Тип перечисления **CAPICOM \_ Certificate \_ Find \_ Type** используется методом [**Certificates. Find**](certificates-find.md) .</span><span class="sxs-lookup"><span data-stu-id="081e3-151">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type is used by the [**Certificates.Find**](certificates-find.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="081e3-152">Требования</span><span class="sxs-lookup"><span data-stu-id="081e3-152">Requirements</span></span>



| <span data-ttu-id="081e3-153">Требование</span><span class="sxs-lookup"><span data-stu-id="081e3-153">Requirement</span></span> | <span data-ttu-id="081e3-154">Значение</span><span class="sxs-lookup"><span data-stu-id="081e3-154">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="081e3-155">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="081e3-155">Redistributable</span></span><br/> | <span data-ttu-id="081e3-156">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="081e3-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="081e3-157">Header</span><span class="sxs-lookup"><span data-stu-id="081e3-157">Header</span></span><br/>          | <dl> <span data-ttu-id="081e3-158"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="081e3-158"><dt>Capicom.h</dt></span></span> </dl> |



 

 




