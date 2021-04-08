---
title: Класс MicrosoftDNS_KEYType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись ресурса ключа.
ms.assetid: d3fa1f35-fa0a-47ee-b2be-4464b9b21d80
keywords:
- DNS класса MicrosoftDNS_KEYType
- DNS-MicrosoftDNS_KEYType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
- MicrosoftDNS_KEYType.Modify
- MicrosoftDNS_KEYType.Flags
- MicrosoftDNS_KEYType.Protocol
- MicrosoftDNS_KEYType.Algorithm
- MicrosoftDNS_KEYType.PublicKey
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e814af1d22820f1722e5812dd314dd1c7f6e0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892126"
---
# <a name="microsoftdns_keytype-class"></a><span data-ttu-id="1d381-105">\_Класс KEYType микрософтднс</span><span class="sxs-lookup"><span data-stu-id="1d381-105">MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="1d381-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись ресурса ключа.</span><span class="sxs-lookup"><span data-stu-id="1d381-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a KEY Resource Record.</span></span>

<span data-ttu-id="1d381-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="1d381-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d381-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d381-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_KEYType : MicrosoftDNS_ResourceRecord
{
  uint16 Flags;
  uint16 Protocol;
  uint16 Algorithm;
  string PublicKey;
};
```

## <a name="members"></a><span data-ttu-id="1d381-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1d381-109">Members</span></span>

<span data-ttu-id="1d381-110">Класс **\_ KEYType микрософтднс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1d381-110">The **MicrosoftDNS\_KEYType** class has these types of members:</span></span>

-   [<span data-ttu-id="1d381-111">Методы</span><span class="sxs-lookup"><span data-stu-id="1d381-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d381-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d381-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d381-113">Методы</span><span class="sxs-lookup"><span data-stu-id="1d381-113">Methods</span></span>

<span data-ttu-id="1d381-114">Класс **\_ KEYType микрософтднс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1d381-114">The **MicrosoftDNS\_KEYType** class has these methods.</span></span>



| <span data-ttu-id="1d381-115">Метод</span><span class="sxs-lookup"><span data-stu-id="1d381-115">Method</span></span>                             | <span data-ttu-id="1d381-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1d381-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d381-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="1d381-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="1d381-118">Создает экземпляр записи КЛЮЧЕВого ресурса на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — в), значение срока жизни и флаг сопоставления WINS, время ожидания для отмены просмотра, время ожидания кэша WINS и имя домена для добавления.</span><span class="sxs-lookup"><span data-stu-id="1d381-118">Instantiates a KEY Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="1d381-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="1d381-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="1d381-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="1d381-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="1d381-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="1d381-121">**Modify**</span></span>                         | <span data-ttu-id="1d381-122">Обновляет значения TTL, флаг сопоставления, время ожидания, время ожидания кэша и домен результата, до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="1d381-122">Updates the TTL, mapping flag, look-up time out, cache time out, and result domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="1d381-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="1d381-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="1d381-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="1d381-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="1d381-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="1d381-125">Qualifiers: Implemented</span></span><br/>                          |



 

### <a name="properties"></a><span data-ttu-id="1d381-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d381-126">Properties</span></span>

<span data-ttu-id="1d381-127">Класс **\_ KEYType микрософтднс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1d381-127">The **MicrosoftDNS\_KEYType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d381-128">**Алгоритм**</span><span class="sxs-lookup"><span data-stu-id="1d381-128">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d381-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d381-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d381-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d381-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d381-131">Алгоритм, используемый с ключом, указанным в записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="1d381-131">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="1d381-132">Назначенные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1d381-132">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="1d381-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1d381-133">Value</span></span>                                                                                                | <span data-ttu-id="1d381-134">Значение</span><span class="sxs-lookup"><span data-stu-id="1d381-134">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="1d381-135"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-135"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1d381-136">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="1d381-136">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="1d381-137"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-137"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1d381-138">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="1d381-138">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="1d381-139"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-139"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="1d381-140">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="1d381-140">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="1d381-141"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-141"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="1d381-142">Шифрование на основе эллиптических кривых</span><span class="sxs-lookup"><span data-stu-id="1d381-142">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1d381-143">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="1d381-143">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d381-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d381-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d381-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d381-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d381-146">Флаги, используемые для определения сопоставления, как описано в документе IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="1d381-146">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="1d381-147">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="1d381-147">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d381-148">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d381-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d381-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d381-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d381-150">Протокол, для которого можно использовать ключ, указанный в записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="1d381-150">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="1d381-151">Назначенные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1d381-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="1d381-152">Значение</span><span class="sxs-lookup"><span data-stu-id="1d381-152">Value</span></span>                                                                                                    | <span data-ttu-id="1d381-153">Значение</span><span class="sxs-lookup"><span data-stu-id="1d381-153">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="1d381-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-154"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="1d381-155">TLS</span><span class="sxs-lookup"><span data-stu-id="1d381-155">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="1d381-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-156"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="1d381-157">E-Mail</span><span class="sxs-lookup"><span data-stu-id="1d381-157">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="1d381-158"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-158"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="1d381-159">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="1d381-159">DNSSEC</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="1d381-160"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-160"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="1d381-161">IPsec</span><span class="sxs-lookup"><span data-stu-id="1d381-161">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="1d381-162"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-162"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="1d381-163">Все протоколы</span><span class="sxs-lookup"><span data-stu-id="1d381-163">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1d381-164">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="1d381-164">**PublicKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d381-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d381-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d381-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d381-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d381-167">Открытый ключ, представленный в базовом 64, как описано в приложении A из RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="1d381-167">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d381-168">Требования</span><span class="sxs-lookup"><span data-stu-id="1d381-168">Requirements</span></span>



| <span data-ttu-id="1d381-169">Требование</span><span class="sxs-lookup"><span data-stu-id="1d381-169">Requirement</span></span> | <span data-ttu-id="1d381-170">Значение</span><span class="sxs-lookup"><span data-stu-id="1d381-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d381-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d381-171">Minimum supported client</span></span><br/> | <span data-ttu-id="1d381-172">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1d381-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1d381-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d381-173">Minimum supported server</span></span><br/> | <span data-ttu-id="1d381-174">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1d381-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1d381-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1d381-175">Namespace</span></span><br/>                | <span data-ttu-id="1d381-176">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="1d381-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="1d381-177">MOF</span><span class="sxs-lookup"><span data-stu-id="1d381-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d381-178"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d381-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d381-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d381-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d381-180">**Метод Креатеинстанцефромпропертидата \_ класса KEYType микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="1d381-180">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="1d381-181">**Метод Modify \_ класса микрософтднс KEYType**</span><span class="sxs-lookup"><span data-stu-id="1d381-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="1d381-182">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="1d381-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





