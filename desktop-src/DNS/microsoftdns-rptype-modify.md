---
title: Метод Modify класса MicrosoftDNS_RPType
description: Метод Modify обновляет запись ресурса ответственного лица (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_RPType класс
- MicrosoftDNS_RPType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892118"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="f135c-106">Метод Modify \_ класса микрософтднс рптипе</span><span class="sxs-lookup"><span data-stu-id="f135c-106">Modify method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="f135c-107">Метод **Modify** обновляет запись ресурса ответственного лица (RP).</span><span class="sxs-lookup"><span data-stu-id="f135c-107">The **Modify** method updates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f135c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f135c-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f135c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f135c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f135c-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f135c-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f135c-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="f135c-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f135c-112">*Рпмаилбокс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f135c-112">*RPMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f135c-113">Полное доменное имя, указывающее почтовый ящик ответственного лица.</span><span class="sxs-lookup"><span data-stu-id="f135c-113">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="f135c-114">*Ткстдомаиннаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f135c-114">*TXTDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f135c-115">Полное доменное имя, для которого существуют записи ресурсов TXT.</span><span class="sxs-lookup"><span data-stu-id="f135c-115">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="f135c-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="f135c-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f135c-117">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="f135c-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f135c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f135c-118">Return value</span></span>

<span data-ttu-id="f135c-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f135c-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f135c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f135c-120">Remarks</span></span>

<span data-ttu-id="f135c-121">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="f135c-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="f135c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f135c-122">Requirements</span></span>



| <span data-ttu-id="f135c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f135c-123">Requirement</span></span> | <span data-ttu-id="f135c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f135c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f135c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f135c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f135c-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f135c-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f135c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f135c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f135c-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f135c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f135c-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f135c-129">Namespace</span></span><br/>                | <span data-ttu-id="f135c-130">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="f135c-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f135c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f135c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f135c-132"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f135c-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f135c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f135c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f135c-134">**Микрософтднс \_ рптипе**</span><span class="sxs-lookup"><span data-stu-id="f135c-134">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="f135c-135">**Метод Креатеинстанцефромпропертидата \_ класса Рптипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="f135c-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f135c-136">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="f135c-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





