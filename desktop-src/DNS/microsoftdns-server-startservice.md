---
title: Метод StartService класса MicrosoftDNS_Server
description: Метод StartService запускает DNS-сервер.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- DNS-метод StartService
- Метод StartService DNS, MicrosoftDNS_Server класс
- DNS класса MicrosoftDNS_Server, метод StartService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654537"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="bd9c5-106">Метод StartService \_ класса микрософтднс Server</span><span class="sxs-lookup"><span data-stu-id="bd9c5-106">StartService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="bd9c5-107">Метод **StartService** запускает DNS-сервер.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-107">The **StartService** method starts the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd9c5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd9c5-108">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="bd9c5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd9c5-109">Parameters</span></span>

<span data-ttu-id="bd9c5-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd9c5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd9c5-111">Return value</span></span>

<span data-ttu-id="bd9c5-112">Ошибка \_ указывает на то, что служба успешно запущена.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-112">ERROR\_SUCCESS indicates the service was successfully started.</span></span> <span data-ttu-id="bd9c5-113">Любое другое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd9c5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bd9c5-114">Requirements</span></span>



| <span data-ttu-id="bd9c5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bd9c5-115">Requirement</span></span> | <span data-ttu-id="bd9c5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bd9c5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd9c5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd9c5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bd9c5-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bd9c5-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bd9c5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd9c5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bd9c5-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bd9c5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bd9c5-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bd9c5-121">Namespace</span></span><br/>                | <span data-ttu-id="bd9c5-122">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="bd9c5-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="bd9c5-123">MOF</span><span class="sxs-lookup"><span data-stu-id="bd9c5-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd9c5-124"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd9c5-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd9c5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd9c5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd9c5-126">**\_Сервер микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="bd9c5-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="bd9c5-127">**Метод работы \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="bd9c5-127">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="bd9c5-128">**Метод Стартскавенгинг \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="bd9c5-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="bd9c5-129">**Метод Жетдистингуишеднаме \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="bd9c5-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





