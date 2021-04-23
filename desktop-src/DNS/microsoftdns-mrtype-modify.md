---
title: Метод Modify класса MicrosoftDNS_MRType
description: Метод Modify обновляет запись ресурса переименования почтового ящика (MR).
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MRType класс
- MicrosoftDNS_MRType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490485"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="56fe4-106">Метод Modify \_ класса микрософтднс мртипе</span><span class="sxs-lookup"><span data-stu-id="56fe4-106">Modify method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="56fe4-107">Метод **Modify** обновляет запись ресурса переименования почтового ящика (MR).</span><span class="sxs-lookup"><span data-stu-id="56fe4-107">The **Modify** method updates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="56fe4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56fe4-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="56fe4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="56fe4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56fe4-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="56fe4-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="56fe4-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="56fe4-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="56fe4-112">*Мрмаилбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56fe4-112">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56fe4-113">Полное доменное имя, указывающее почтовый ящик, который является правильным именем почтового ящика, указанного в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="56fe4-113">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="56fe4-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="56fe4-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="56fe4-115">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="56fe4-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56fe4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56fe4-116">Return value</span></span>

<span data-ttu-id="56fe4-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="56fe4-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56fe4-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56fe4-118">Remarks</span></span>

<span data-ttu-id="56fe4-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="56fe4-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="56fe4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="56fe4-120">Requirements</span></span>



| <span data-ttu-id="56fe4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="56fe4-121">Requirement</span></span> | <span data-ttu-id="56fe4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="56fe4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56fe4-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56fe4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="56fe4-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="56fe4-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="56fe4-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56fe4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="56fe4-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="56fe4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="56fe4-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="56fe4-127">Namespace</span></span><br/>                | <span data-ttu-id="56fe4-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="56fe4-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="56fe4-129">MOF</span><span class="sxs-lookup"><span data-stu-id="56fe4-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56fe4-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56fe4-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56fe4-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56fe4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56fe4-132">**Микрософтднс \_ мртипе**</span><span class="sxs-lookup"><span data-stu-id="56fe4-132">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="56fe4-133">**Метод Креатеинстанцефромпропертидата \_ класса Мртипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="56fe4-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="56fe4-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="56fe4-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





