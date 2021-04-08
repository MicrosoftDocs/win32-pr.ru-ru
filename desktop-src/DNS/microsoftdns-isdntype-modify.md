---
title: Метод Modify класса MicrosoftDNS_ISDNType
description: Метод Modify обновляет запись ресурса ISDN.
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_ISDNType класс
- MicrosoftDNS_ISDNType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c369a6650c834ff9f35af6389c346daec86a954
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988222"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="d144c-106">Метод Modify \_ класса микрософтднс исднтипе</span><span class="sxs-lookup"><span data-stu-id="d144c-106">Modify method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="d144c-107">Метод **Modify** обновляет запись ресурса ISDN.</span><span class="sxs-lookup"><span data-stu-id="d144c-107">The **Modify** method updates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d144c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d144c-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d144c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d144c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d144c-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d144c-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d144c-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="d144c-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d144c-112">*Исдннумбер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d144c-112">*ISDNNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d144c-113">Номер ISDN и DDI владельца записи.</span><span class="sxs-lookup"><span data-stu-id="d144c-113">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="d144c-114">*Подадрес* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d144c-114">*SubAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d144c-115">Подадрес владельца, если он определен.</span><span class="sxs-lookup"><span data-stu-id="d144c-115">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="d144c-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="d144c-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d144c-117">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="d144c-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d144c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d144c-118">Return value</span></span>

<span data-ttu-id="d144c-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d144c-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d144c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d144c-120">Remarks</span></span>

<span data-ttu-id="d144c-121">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="d144c-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="d144c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d144c-122">Requirements</span></span>



| <span data-ttu-id="d144c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d144c-123">Requirement</span></span> | <span data-ttu-id="d144c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d144c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d144c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d144c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d144c-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d144c-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d144c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d144c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d144c-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d144c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d144c-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d144c-129">Namespace</span></span><br/>                | <span data-ttu-id="d144c-130">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="d144c-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d144c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d144c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d144c-132"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d144c-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d144c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d144c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d144c-134">**Микрософтднс \_ исднтипе**</span><span class="sxs-lookup"><span data-stu-id="d144c-134">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="d144c-135">**Метод Креатеинстанцефромпропертидата \_ класса Исднтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d144c-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d144c-136">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="d144c-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





