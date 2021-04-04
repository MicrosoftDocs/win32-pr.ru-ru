---
title: Метод Modify класса MicrosoftDNS_MXType
description: Метод Modify обновляет запись ресурса почтового обменника (MR).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MXType класс
- MicrosoftDNS_MXType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989330"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="845f8-106">Метод Modify \_ класса микрософтднс мкстипе</span><span class="sxs-lookup"><span data-stu-id="845f8-106">Modify method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="845f8-107">Метод **Modify** обновляет запись ресурса почтового обменника (MR).</span><span class="sxs-lookup"><span data-stu-id="845f8-107">The **Modify** method updates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="845f8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="845f8-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="845f8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="845f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="845f8-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="845f8-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="845f8-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="845f8-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="845f8-112">*Настройка* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="845f8-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="845f8-113">Предпочтение данной записи ресурса между другими пользователями того же владельца.</span><span class="sxs-lookup"><span data-stu-id="845f8-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="845f8-114">Более низкие значения являются предпочтительными.</span><span class="sxs-lookup"><span data-stu-id="845f8-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="845f8-115">*Маилексчанже* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="845f8-115">*MailExchange* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="845f8-116">Полное доменное имя с указанием узла, который будет использоваться в качестве почтового обмена для имени владельца.</span><span class="sxs-lookup"><span data-stu-id="845f8-116">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="845f8-117">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="845f8-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="845f8-118">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="845f8-118">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="845f8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="845f8-119">Return value</span></span>

<span data-ttu-id="845f8-120">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="845f8-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="845f8-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="845f8-121">Remarks</span></span>

<span data-ttu-id="845f8-122">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="845f8-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="845f8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="845f8-123">Requirements</span></span>



| <span data-ttu-id="845f8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="845f8-124">Requirement</span></span> | <span data-ttu-id="845f8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="845f8-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="845f8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="845f8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="845f8-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="845f8-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="845f8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="845f8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="845f8-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="845f8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="845f8-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="845f8-130">Namespace</span></span><br/>                | <span data-ttu-id="845f8-131">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="845f8-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="845f8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="845f8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="845f8-133"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="845f8-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="845f8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="845f8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="845f8-135">**Микрософтднс \_ мкстипе**</span><span class="sxs-lookup"><span data-stu-id="845f8-135">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="845f8-136">**Метод Креатеинстанцефромпропертидата \_ класса Мкстипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="845f8-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="845f8-137">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="845f8-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





