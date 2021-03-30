---
title: Метод Modify класса MicrosoftDNS_HINFOType
description: Метод Modify обновляет запись ресурса сведения об узле (HINFO).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_HINFOType класс
- MicrosoftDNS_HINFOType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802309"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="f7509-106">Метод Modify \_ класса микрософтднс хинфотипе</span><span class="sxs-lookup"><span data-stu-id="f7509-106">Modify method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="f7509-107">Метод **Modify** обновляет запись ресурса сведения об узле (HINFO).</span><span class="sxs-lookup"><span data-stu-id="f7509-107">The **Modify** method updates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7509-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7509-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f7509-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7509-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7509-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f7509-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7509-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="f7509-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f7509-112">*ЦП* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f7509-112">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7509-113">Тип ЦП владельца записи.</span><span class="sxs-lookup"><span data-stu-id="f7509-113">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="f7509-114">*Операционная система* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f7509-114">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7509-115">Операционная система владельца записи.</span><span class="sxs-lookup"><span data-stu-id="f7509-115">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="f7509-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="f7509-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f7509-117">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="f7509-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7509-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7509-118">Return value</span></span>

<span data-ttu-id="f7509-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f7509-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7509-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7509-120">Remarks</span></span>

<span data-ttu-id="f7509-121">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="f7509-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7509-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f7509-122">Requirements</span></span>



| <span data-ttu-id="f7509-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f7509-123">Requirement</span></span> | <span data-ttu-id="f7509-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f7509-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7509-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7509-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f7509-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f7509-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f7509-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7509-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f7509-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f7509-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f7509-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7509-129">Namespace</span></span><br/>                | <span data-ttu-id="f7509-130">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="f7509-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f7509-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f7509-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7509-132"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7509-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7509-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7509-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7509-134">**Микрософтднс \_ хинфотипе**</span><span class="sxs-lookup"><span data-stu-id="f7509-134">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="f7509-135">**Метод Креатеинстанцефромпропертидата \_ класса Хинфотипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="f7509-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f7509-136">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="f7509-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





