---
title: Метод Инапсистемхеалсаженткаллбакк Нотифисистемисолатионстатечанже (Напсистемхеалсажент. h)
description: Вызывается Напажент для указания на то, что состояние изоляции системы или время окончания надзора изменилось.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- Метод Нотифисистемисолатионстатечанже NAP
- Метод Нотифисистемисолатионстатечанже NAP, интерфейс Инапсистемхеалсаженткаллбакк
- Инапсистемхеалсаженткаллбакк интерфейса NAP, метод Нотифисистемисолатионстатечанже
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802615"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a><span data-ttu-id="dec90-106">Метод Инапсистемхеалсаженткаллбакк:: Нотифисистемисолатионстатечанже</span><span class="sxs-lookup"><span data-stu-id="dec90-106">INapSystemHealthAgentCallback::NotifySystemIsolationStateChange method</span></span>

> [!Note]  
> <span data-ttu-id="dec90-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="dec90-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dec90-108">Метод **инапсистемхеалсаженткаллбакк:: нотифисистемисолатионстатечанже** вызывается напажент, чтобы указать, что состояние изоляции системы или время окончания надзора изменилось.</span><span class="sxs-lookup"><span data-stu-id="dec90-108">The **INapSystemHealthAgentCallback::NotifySystemIsolationStateChange** method is called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec90-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dec90-109">Syntax</span></span>


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a><span data-ttu-id="dec90-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dec90-110">Parameters</span></span>

<span data-ttu-id="dec90-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="dec90-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dec90-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dec90-112">Return value</span></span>

<span data-ttu-id="dec90-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="dec90-113">This method can return one of these values.</span></span>



| <span data-ttu-id="dec90-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dec90-114">Return code</span></span>                                                                          | <span data-ttu-id="dec90-115">Описание</span><span class="sxs-lookup"><span data-stu-id="dec90-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="dec90-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dec90-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dec90-117">Указывает на успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="dec90-117">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dec90-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dec90-118">Remarks</span></span>

<span data-ttu-id="dec90-119">Этот метод обратного вызова объявляется системой защиты доступа к сети и реализуется модулем записи SHA.</span><span class="sxs-lookup"><span data-stu-id="dec90-119">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="dec90-120">Агент работоспособности может запрашивать состояние NAP системы с помощью [**инапсистемхеалсажентбиндинг:: жетсистемисолатионинфо**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="dec90-120">The health agent can query the system NAP state using the [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dec90-121">Требования</span><span class="sxs-lookup"><span data-stu-id="dec90-121">Requirements</span></span>



| <span data-ttu-id="dec90-122">Требование</span><span class="sxs-lookup"><span data-stu-id="dec90-122">Requirement</span></span> | <span data-ttu-id="dec90-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dec90-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec90-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dec90-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dec90-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dec90-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dec90-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dec90-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dec90-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dec90-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dec90-128">Header</span><span class="sxs-lookup"><span data-stu-id="dec90-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec90-129"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="dec90-129"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="dec90-130">IDL</span><span class="sxs-lookup"><span data-stu-id="dec90-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dec90-131"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dec90-131"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dec90-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dec90-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec90-133">**инапсистемхеалсаженткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="dec90-133">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





