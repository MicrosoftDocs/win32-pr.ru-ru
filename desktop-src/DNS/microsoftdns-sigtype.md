---
title: Класс MicrosoftDNS_SIGType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись ресурса сигнатуры (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- DNS класса MicrosoftDNS_SIGType
- DNS-MicrosoftDNS_SIGType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801348"
---
# <a name="microsoftdns_sigtype-class"></a><span data-ttu-id="13d5e-105">\_Класс микрософтднс сигтипе</span><span class="sxs-lookup"><span data-stu-id="13d5e-105">MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="13d5e-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись ресурса сигнатуры (SIG).</span><span class="sxs-lookup"><span data-stu-id="13d5e-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Signature (SIG) Resource Record.</span></span>

<span data-ttu-id="13d5e-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="13d5e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d5e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13d5e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a><span data-ttu-id="13d5e-109">Члены</span><span class="sxs-lookup"><span data-stu-id="13d5e-109">Members</span></span>

<span data-ttu-id="13d5e-110">Класс **микрософтднс \_ сигтипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="13d5e-110">The **MicrosoftDNS\_SIGType** class has these types of members:</span></span>

-   [<span data-ttu-id="13d5e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="13d5e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="13d5e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="13d5e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="13d5e-113">Методы</span><span class="sxs-lookup"><span data-stu-id="13d5e-113">Methods</span></span>

<span data-ttu-id="13d5e-114">Класс **микрософтднс \_ сигтипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="13d5e-114">The **MicrosoftDNS\_SIGType** class has these methods.</span></span>



| <span data-ttu-id="13d5e-115">Метод</span><span class="sxs-lookup"><span data-stu-id="13d5e-115">Method</span></span>                             | <span data-ttu-id="13d5e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="13d5e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d5e-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="13d5e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="13d5e-118">Создает объект RR SIG на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и флаг сопоставления WINS, время ожидания для отмены просмотра, время ожидания кэша WINS и имя домена для добавления.</span><span class="sxs-lookup"><span data-stu-id="13d5e-118">Instantiates an SIG RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="13d5e-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="13d5e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="13d5e-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="13d5e-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="13d5e-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="13d5e-121">**Modify**</span></span>                         | <span data-ttu-id="13d5e-122">Обновляет значения TTL, флага сопоставления, времени ожидания при поиске, истечения времени ожидания кэша и домена результата до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="13d5e-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="13d5e-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="13d5e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="13d5e-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="13d5e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="13d5e-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="13d5e-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="13d5e-126">**Windows Server 2003:** Этот метод также обновляет значения Типековеред, algorithm, labels, Оригиналттл, Сигнатурикспиратион, Сигнатуреинцептион, Кэйтаг, Сигнернаме и Signature до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="13d5e-126">**Windows Server 2003:** This method also updates the TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName and Signature to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="13d5e-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="13d5e-127">Properties</span></span>

<span data-ttu-id="13d5e-128">Класс **микрософтднс \_ сигтипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="13d5e-128">The **MicrosoftDNS\_SIGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13d5e-129">**Алгоритм**</span><span class="sxs-lookup"><span data-stu-id="13d5e-129">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d5e-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13d5e-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13d5e-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13d5e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d5e-132">Алгоритм, используемый с ключом, указанным в записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="13d5e-132">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="13d5e-133">Назначенные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="13d5e-133">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="13d5e-134">Значение</span><span class="sxs-lookup"><span data-stu-id="13d5e-134">Value</span></span>                                                                                                | <span data-ttu-id="13d5e-135">Значение</span><span class="sxs-lookup"><span data-stu-id="13d5e-135">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="13d5e-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="13d5e-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="13d5e-137">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="13d5e-137">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="13d5e-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="13d5e-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="13d5e-139">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="13d5e-139">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="13d5e-140"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="13d5e-140"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="13d5e-141">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="13d5e-141">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="13d5e-142"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="13d5e-142"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="13d5e-143">Шифрование на основе эллиптических кривых</span><span class="sxs-lookup"><span data-stu-id="13d5e-143">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="13d5e-144">**кэйтаг**</span><span class="sxs-lookup"><span data-stu-id="13d5e-144">**KeyTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d5e-145">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13d5e-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13d5e-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13d5e-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d5e-147">Метод, используемый для выбора ключа, который проверяет подпись.</span><span class="sxs-lookup"><span data-stu-id="13d5e-147">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="13d5e-148">Метод, используемый для вычисления Кэйтаг, см. в документе RFC 2535 в приложении C.</span><span class="sxs-lookup"><span data-stu-id="13d5e-148">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="13d5e-149">**Метки**</span><span class="sxs-lookup"><span data-stu-id="13d5e-149">**Labels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d5e-150">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13d5e-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13d5e-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13d5e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d5e-152">Число меток без знака в исходном имени владельца RR.</span><span class="sxs-lookup"><span data-stu-id="13d5e-152">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="13d5e-153">Число не включает метку NULL для корня или любые начальные подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="13d5e-153">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="13d5e-154">**оригиналттл**</span><span class="sxs-lookup"><span data-stu-id="13d5e-154">**OriginalTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d5e-155">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13d5e-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13d5e-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13d5e-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d5e-157">Срок жизни набора записей RR, подписанный SIG.</span><span class="sxs-lookup"><span data-stu-id="13d5e-157">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="13d5e-158">**Образец**</span><span class="sxs-lookup"><span data-stu-id="13d5e-158">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d5e-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13d5e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d5e-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13d5e-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d5e-161">Сигнатура, представленная в базовом 64, в формате, определенном в RFC 2535, приложение а.</span><span class="sxs-lookup"><span data-stu-id="13d5e-161">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="13d5e-162">**сигнатурикспиратион**</span><span class="sxs-lookup"><span data-stu-id="13d5e-162">**SignatureExpiration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d5e-163">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13d5e-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13d5e-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13d5e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d5e-165">Дата окончания срока действия подписи, выраженная в секундах с начала 1 января 1970 г., время по Гринвичу (GMT), за исключением високосных секунд.</span><span class="sxs-lookup"><span data-stu-id="13d5e-165">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="13d5e-166">**сигнатуреинцептион**</span><span class="sxs-lookup"><span data-stu-id="13d5e-166">**SignatureInception**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d5e-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13d5e-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13d5e-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13d5e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d5e-169">Дата и время, когда подпись действительна, выраженная в секундах с начала 1 января 1970 г., время по Гринвичу (GMT), за исключением високосных секунд.</span><span class="sxs-lookup"><span data-stu-id="13d5e-169">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="13d5e-170">**сигнернаме**</span><span class="sxs-lookup"><span data-stu-id="13d5e-170">**SignerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d5e-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13d5e-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d5e-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13d5e-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d5e-173">Доменное имя подписывающий, создавшего RR SIG.</span><span class="sxs-lookup"><span data-stu-id="13d5e-173">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="13d5e-174">**типековеред**</span><span class="sxs-lookup"><span data-stu-id="13d5e-174">**TypeCovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d5e-175">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13d5e-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13d5e-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13d5e-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d5e-177">Тип записи ресурса, охватываемый этой ПОДПИСЬю.</span><span class="sxs-lookup"><span data-stu-id="13d5e-177">Type of RR covered by this SIG.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13d5e-178">Требования</span><span class="sxs-lookup"><span data-stu-id="13d5e-178">Requirements</span></span>



| <span data-ttu-id="13d5e-179">Требование</span><span class="sxs-lookup"><span data-stu-id="13d5e-179">Requirement</span></span> | <span data-ttu-id="13d5e-180">Значение</span><span class="sxs-lookup"><span data-stu-id="13d5e-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13d5e-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13d5e-181">Minimum supported client</span></span><br/> | <span data-ttu-id="13d5e-182">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="13d5e-182">None supported</span></span><br/>                                                              |
| <span data-ttu-id="13d5e-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13d5e-183">Minimum supported server</span></span><br/> | <span data-ttu-id="13d5e-184">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="13d5e-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13d5e-185">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="13d5e-185">Namespace</span></span><br/>                | <span data-ttu-id="13d5e-186">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="13d5e-186">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="13d5e-187">MOF</span><span class="sxs-lookup"><span data-stu-id="13d5e-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13d5e-188"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13d5e-188"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d5e-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13d5e-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d5e-190">**Метод Креатеинстанцефромпропертидата \_ класса Сигтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="13d5e-190">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="13d5e-191">**Метод Modify \_ класса микрософтднс сигтипе**</span><span class="sxs-lookup"><span data-stu-id="13d5e-191">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="13d5e-192">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="13d5e-192">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





