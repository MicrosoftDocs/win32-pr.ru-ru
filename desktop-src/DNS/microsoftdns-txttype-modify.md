---
title: Метод Modify класса MicrosoftDNS_TXTType
description: Метод Modify обновляет запись ресурса Text (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_TXTType класс
- MicrosoftDNS_TXTType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285dfb6d5323ca3775f981aecbf5a0170392cd3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135287"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="089b3-106">Метод Modify \_ класса микрософтднс тксттипе</span><span class="sxs-lookup"><span data-stu-id="089b3-106">Modify method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="089b3-107">Метод **Modify** обновляет запись ресурса Text (txt).</span><span class="sxs-lookup"><span data-stu-id="089b3-107">The **Modify** method updates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="089b3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="089b3-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="089b3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="089b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="089b3-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="089b3-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="089b3-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="089b3-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="089b3-112">*Дескриптиветекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="089b3-112">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="089b3-113">Описательный текст, семантика которого зависит от домена владельца.</span><span class="sxs-lookup"><span data-stu-id="089b3-113">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="089b3-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="089b3-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="089b3-115">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="089b3-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="089b3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="089b3-116">Return value</span></span>

<span data-ttu-id="089b3-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="089b3-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="089b3-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="089b3-118">Remarks</span></span>

<span data-ttu-id="089b3-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="089b3-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="089b3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="089b3-120">Requirements</span></span>



| <span data-ttu-id="089b3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="089b3-121">Requirement</span></span> | <span data-ttu-id="089b3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="089b3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="089b3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="089b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="089b3-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="089b3-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="089b3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="089b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="089b3-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="089b3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="089b3-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="089b3-127">Namespace</span></span><br/>                | <span data-ttu-id="089b3-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="089b3-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="089b3-129">MOF</span><span class="sxs-lookup"><span data-stu-id="089b3-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="089b3-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="089b3-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="089b3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="089b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089b3-132">**Микрософтднс \_ тксттипе**</span><span class="sxs-lookup"><span data-stu-id="089b3-132">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="089b3-133">**Метод Креатеинстанцефромпропертидата \_ класса Тксттипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="089b3-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="089b3-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="089b3-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





