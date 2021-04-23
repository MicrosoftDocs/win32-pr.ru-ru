---
description: Представляет маркер ответа OCSP, связанного с цепочкой сертификатов сервера.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912032"
---
# <a name="hcert_server_ocsp_response"></a><span data-ttu-id="0d6a7-103">\_ \_ ответ OCSP сервера \_ хцерт</span><span class="sxs-lookup"><span data-stu-id="0d6a7-103">HCERT\_SERVER\_OCSP\_RESPONSE</span></span>

<span data-ttu-id="0d6a7-104">Тип **данных \_ \_ \_ ответа OCSP сервера хцерт** представляет собой маркер ответа OCSP, связанного с цепочкой сертификатов сервера.</span><span class="sxs-lookup"><span data-stu-id="0d6a7-104">The **HCERT\_SERVER\_OCSP\_RESPONSE** data type represents a handle to an OCSP response associated with a server certificate chain.</span></span>

<span data-ttu-id="0d6a7-105">Этот тип используется следующими интерфейсами API.</span><span class="sxs-lookup"><span data-stu-id="0d6a7-105">This type is used by the following APIs.</span></span>

-   [<span data-ttu-id="0d6a7-106">**цертопенсерверокспреспонсе**</span><span class="sxs-lookup"><span data-stu-id="0d6a7-106">**CertOpenServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [<span data-ttu-id="0d6a7-107">**цертаддрефсерверокспреспонсе**</span><span class="sxs-lookup"><span data-stu-id="0d6a7-107">**CertAddRefServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [<span data-ttu-id="0d6a7-108">**цертклосесерверокспреспонсе**</span><span class="sxs-lookup"><span data-stu-id="0d6a7-108">**CertCloseServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [<span data-ttu-id="0d6a7-109">**цертжетсерверокспреспонсеконтекст**</span><span class="sxs-lookup"><span data-stu-id="0d6a7-109">**CertGetServerOcspResponseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a><span data-ttu-id="0d6a7-110">Требования</span><span class="sxs-lookup"><span data-stu-id="0d6a7-110">Requirements</span></span>



| <span data-ttu-id="0d6a7-111">Требование</span><span class="sxs-lookup"><span data-stu-id="0d6a7-111">Requirement</span></span> | <span data-ttu-id="0d6a7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0d6a7-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6a7-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d6a7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0d6a7-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d6a7-114">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d6a7-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d6a7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0d6a7-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d6a7-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d6a7-117">Header</span><span class="sxs-lookup"><span data-stu-id="0d6a7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d6a7-118"><dt>Винкрипт. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d6a7-118"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 




