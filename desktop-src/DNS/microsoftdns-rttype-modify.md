---
title: Метод Modify класса MicrosoftDNS_RTType
description: Метод Modify обновляет запись ресурса маршрута (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_RTType класс
- MicrosoftDNS_RTType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534325"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="14e9c-106">Метод Modify \_ класса микрософтднс рттипе</span><span class="sxs-lookup"><span data-stu-id="14e9c-106">Modify method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="14e9c-107">Метод **Modify** обновляет запись ресурса маршрута (RT).</span><span class="sxs-lookup"><span data-stu-id="14e9c-107">The **Modify** method updates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e9c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14e9c-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="14e9c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="14e9c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e9c-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="14e9c-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e9c-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="14e9c-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="14e9c-112">*Настройка* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="14e9c-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e9c-113">Предпочтение данной записи ресурса между другими пользователями того же владельца.</span><span class="sxs-lookup"><span data-stu-id="14e9c-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="14e9c-114">Более низкие значения являются предпочтительными.</span><span class="sxs-lookup"><span data-stu-id="14e9c-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="14e9c-115">*Интермедиатехост* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="14e9c-115">*IntermediateHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e9c-116">Полное доменное имя, указывающее узел, который будет выступать в качестве промежуточного в достижение узла, указанного владельцем.</span><span class="sxs-lookup"><span data-stu-id="14e9c-116">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="14e9c-117">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="14e9c-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="14e9c-118">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="14e9c-118">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e9c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14e9c-119">Return value</span></span>

<span data-ttu-id="14e9c-120">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="14e9c-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14e9c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14e9c-121">Remarks</span></span>

<span data-ttu-id="14e9c-122">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="14e9c-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e9c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="14e9c-123">Requirements</span></span>



| <span data-ttu-id="14e9c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="14e9c-124">Requirement</span></span> | <span data-ttu-id="14e9c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="14e9c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14e9c-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14e9c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="14e9c-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="14e9c-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="14e9c-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14e9c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="14e9c-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14e9c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14e9c-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="14e9c-130">Namespace</span></span><br/>                | <span data-ttu-id="14e9c-131">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="14e9c-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="14e9c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="14e9c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14e9c-133"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14e9c-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14e9c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14e9c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e9c-135">**Микрософтднс \_ рттипе**</span><span class="sxs-lookup"><span data-stu-id="14e9c-135">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="14e9c-136">**Метод Креатеинстанцефромпропертидата \_ класса Рттипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="14e9c-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="14e9c-137">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="14e9c-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





