---
description: Следующие константы могут возвращаться как ошибки.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: Константы RND_ (Рндерр. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685430"
---
# <a name="rnd_-constants"></a><span data-ttu-id="d9529-103">\_Константы Rnd</span><span class="sxs-lookup"><span data-stu-id="d9529-103">RND\_ Constants</span></span>

<span data-ttu-id="d9529-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="d9529-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d9529-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="d9529-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d9529-106">Следующие константы могут возвращаться как ошибки.</span><span class="sxs-lookup"><span data-stu-id="d9529-106">The following constants may be returned as errors.</span></span>

<dl> <dt>

<span data-ttu-id="d9529-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**\_недопустимое \_ время Rnd**</span><span class="sxs-lookup"><span data-stu-id="d9529-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d9529-108">0xe0000200</span><span class="sxs-lookup"><span data-stu-id="d9529-108">0xe0000200</span></span>
</dt> <dt>



<span data-ttu-id="d9529-109">Указано недопустимое значение времени.</span><span class="sxs-lookup"><span data-stu-id="d9529-109">The time value entered is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9529-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**\_имя неопределенного \_ сервера \_**</span><span class="sxs-lookup"><span data-stu-id="d9529-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND\_NULL\_SERVER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d9529-111">0xe0000201</span><span class="sxs-lookup"><span data-stu-id="d9529-111">0xe0000201</span></span>
</dt> <dt>



<span data-ttu-id="d9529-112">Имя сервера равно **null**, возможно, из-за того, что [**Итконференцеблоб:: init**](itconferenceblob-init.md) не был запущен или завершился неудачно.</span><span class="sxs-lookup"><span data-stu-id="d9529-112">The server name is **NULL**, probably because [**ITConferenceBlob::Init**](itconferenceblob-init.md) has not been run or did not succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9529-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**Функция RND \_ уже \_ подключена**</span><span class="sxs-lookup"><span data-stu-id="d9529-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d9529-114">0xe0000202</span><span class="sxs-lookup"><span data-stu-id="d9529-114">0xe0000202</span></span>
</dt> <dt>



<span data-ttu-id="d9529-115">Был вызван метод [**итдиректори:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) , но соединение уже существует.</span><span class="sxs-lookup"><span data-stu-id="d9529-115">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method was called, but a connection already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9529-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ не \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="d9529-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d9529-117">0xe0000203</span><span class="sxs-lookup"><span data-stu-id="d9529-117">0xe0000203</span></span>
</dt> <dt>



<span data-ttu-id="d9529-118">Метод [**итдиректори:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) не был вызван или завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d9529-118">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method has not been called, or failed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9529-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d9529-119">Requirements</span></span>



| <span data-ttu-id="d9529-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d9529-120">Requirement</span></span> | <span data-ttu-id="d9529-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d9529-121">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d9529-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="d9529-122">TAPI version</span></span><br/> | <span data-ttu-id="d9529-123">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d9529-123">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="d9529-124">Header</span><span class="sxs-lookup"><span data-stu-id="d9529-124">Header</span></span><br/>       | <dl> <span data-ttu-id="d9529-125"><dt>Рндерр. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9529-125"><dt>Rnderr.h</dt></span></span> </dl> |



 

 




