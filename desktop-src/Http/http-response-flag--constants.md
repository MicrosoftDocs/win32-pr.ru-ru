---
title: Константы HTTP_RESPONSE_FLAG_ (HTTP. h)
description: Определите параметры для настройки ответов в API HTTP-сервера.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661865"
---
# <a name="http_response_flag_-constants"></a><span data-ttu-id="cc445-103">\_ \_ Константы флага HTTP-ответа \_</span><span class="sxs-lookup"><span data-stu-id="cc445-103">HTTP\_RESPONSE\_FLAG\_ Constants</span></span>

<span data-ttu-id="cc445-104">Константы **\_ \_ флага \_ http-ответа** определяют параметры для настройки ответов в API-интерфейсе сервера HTTP.</span><span class="sxs-lookup"><span data-stu-id="cc445-104">The **HTTP\_RESPONSE\_FLAG\_** constants define options to configure responses in the HTTP Server API.</span></span>

<span data-ttu-id="cc445-105">Эти константы используются в элементе **flags** структуры [**HTTP \_ Response \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) .</span><span class="sxs-lookup"><span data-stu-id="cc445-105">These constants are used in the **Flags** member of the [**HTTP\_RESPONSE\_V1**](/windows/desktop/api/Http/ns-http-http_response_v1) structure.</span></span>

<dl> <dt>

<span data-ttu-id="cc445-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**\_флаг ответа \_ HTTP \_ \_ доступно несколько кодировок \_**</span><span class="sxs-lookup"><span data-stu-id="cc445-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP\_RESPONSE\_FLAG\_MULTIPLE\_ENCODINGS\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc445-107">Для этого ресурса доступны кодировки, отличные от формы Identity.</span><span class="sxs-lookup"><span data-stu-id="cc445-107">Encodings other than identity form are available for this resource.</span></span> <span data-ttu-id="cc445-108">Этот флаг пропускается, если приложение не запросило кэширование ответа.</span><span class="sxs-lookup"><span data-stu-id="cc445-108">This flag is ignored if the application has not asked for the response to be cached.</span></span> <span data-ttu-id="cc445-109">Он используется как подсказка к API HTTP-сервера для согласования содержимого при обслуживании из кэша ответов ядра.</span><span class="sxs-lookup"><span data-stu-id="cc445-109">It's used as a hint to the HTTP Server API for content negotiation when serving from the kernel response cache.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc445-110">Требования</span><span class="sxs-lookup"><span data-stu-id="cc445-110">Requirements</span></span>



| <span data-ttu-id="cc445-111">Требование</span><span class="sxs-lookup"><span data-stu-id="cc445-111">Requirement</span></span> | <span data-ttu-id="cc445-112">Значение</span><span class="sxs-lookup"><span data-stu-id="cc445-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cc445-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc445-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cc445-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cc445-114">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc445-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc445-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cc445-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc445-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cc445-117">Header</span><span class="sxs-lookup"><span data-stu-id="cc445-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc445-118"><dt>HTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc445-118"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc445-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc445-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc445-120">Константы API сервера HTTP версии 2,0</span><span class="sxs-lookup"><span data-stu-id="cc445-120">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="cc445-121">**HTTP- \_ ответ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="cc445-121">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





