---
title: Метод Modify класса MicrosoftDNS_MBType
description: Метод Modify обновляет запись ресурса почтового ящика (MB).
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MBType класс
- MicrosoftDNS_MBType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d6f0fcb0faf5c1e8da152798863c8cecc8641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802644"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="85366-106">Метод Modify \_ класса микрософтднс мбтипе</span><span class="sxs-lookup"><span data-stu-id="85366-106">Modify method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="85366-107">Метод **Modify** обновляет запись ресурса почтового ящика (MB).</span><span class="sxs-lookup"><span data-stu-id="85366-107">The **Modify** method updates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="85366-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85366-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="85366-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="85366-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85366-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="85366-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85366-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="85366-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="85366-112">*Мбхост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85366-112">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85366-113">Строка, представляющая имя узла почтового ящика для записи в МБ.</span><span class="sxs-lookup"><span data-stu-id="85366-113">String representing the mailbox host name for the MB record.</span></span>

</dd> <dt>

<span data-ttu-id="85366-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="85366-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="85366-115">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="85366-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85366-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85366-116">Return value</span></span>

<span data-ttu-id="85366-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="85366-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85366-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85366-118">Remarks</span></span>

<span data-ttu-id="85366-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="85366-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="85366-120">Требования</span><span class="sxs-lookup"><span data-stu-id="85366-120">Requirements</span></span>



| <span data-ttu-id="85366-121">Требование</span><span class="sxs-lookup"><span data-stu-id="85366-121">Requirement</span></span> | <span data-ttu-id="85366-122">Значение</span><span class="sxs-lookup"><span data-stu-id="85366-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85366-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85366-123">Minimum supported client</span></span><br/> | <span data-ttu-id="85366-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="85366-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="85366-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85366-125">Minimum supported server</span></span><br/> | <span data-ttu-id="85366-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="85366-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="85366-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="85366-127">Namespace</span></span><br/>                | <span data-ttu-id="85366-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="85366-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="85366-129">MOF</span><span class="sxs-lookup"><span data-stu-id="85366-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85366-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85366-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85366-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85366-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85366-132">**Микрософтднс \_ мбтипе**</span><span class="sxs-lookup"><span data-stu-id="85366-132">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="85366-133">**Метод Креатеинстанцефромпропертидата \_ класса Мбтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="85366-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="85366-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="85366-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





