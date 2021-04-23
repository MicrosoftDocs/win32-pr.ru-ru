---
title: Метод Modify класса MicrosoftDNS_MDType
description: Метод Modify обновляет запись ресурса почтового агента для домена (MD).
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MDType класс
- MicrosoftDNS_MDType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ed5e3a8d7f819447d256ba3bce31f4eaa6986a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135843"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a><span data-ttu-id="f1f25-106">Метод Modify \_ класса микрософтднс мдтипе</span><span class="sxs-lookup"><span data-stu-id="f1f25-106">Modify method of the MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="f1f25-107">Метод **Modify** обновляет запись ресурса почтового агента для домена (MD).</span><span class="sxs-lookup"><span data-stu-id="f1f25-107">The **Modify** method updates a Mail Agent for Domain (MD) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f25-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1f25-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f1f25-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1f25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f25-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f1f25-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f25-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="f1f25-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f1f25-112">*Мдхост* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f1f25-112">*MDHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f25-113">Строка, представляющая узел доставки почты.</span><span class="sxs-lookup"><span data-stu-id="f1f25-113">String representing the mail delivery host.</span></span>

</dd> <dt>

<span data-ttu-id="f1f25-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="f1f25-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f25-115">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="f1f25-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f25-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1f25-116">Return value</span></span>

<span data-ttu-id="f1f25-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f1f25-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1f25-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1f25-118">Remarks</span></span>

<span data-ttu-id="f1f25-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="f1f25-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f25-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f1f25-120">Requirements</span></span>



| <span data-ttu-id="f1f25-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f1f25-121">Requirement</span></span> | <span data-ttu-id="f1f25-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f1f25-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f25-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1f25-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f1f25-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f1f25-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f1f25-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1f25-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f1f25-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f1f25-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f1f25-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f1f25-127">Namespace</span></span><br/>                | <span data-ttu-id="f1f25-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="f1f25-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f1f25-129">MOF</span><span class="sxs-lookup"><span data-stu-id="f1f25-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1f25-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1f25-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1f25-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1f25-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f25-132">**Микрософтднс \_ мдтипе**</span><span class="sxs-lookup"><span data-stu-id="f1f25-132">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)
</dt> <dt>

[<span data-ttu-id="f1f25-133">**Метод Креатеинстанцефромпропертидата \_ класса Мдтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="f1f25-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f1f25-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="f1f25-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





