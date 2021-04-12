---
title: IMsRdpClientTransportSettings3 Гатевайаускукиесервераддр, свойство
description: Адрес сервера для проверки подлинности на основе файлов cookie.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайаускукиесервераддр
- Службы удаленных рабочих столов свойства Гатевайаускукиесервераддр, интерфейс IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, свойство Гатевайаускукиесервераддр
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc238129d0bb9f698e90fc5e1de85e7257a4d16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492933"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a><span data-ttu-id="3a8ca-106">Свойство IMsRdpClientTransportSettings3:: Гатевайаускукиесервераддр</span><span class="sxs-lookup"><span data-stu-id="3a8ca-106">IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr property</span></span>

<span data-ttu-id="3a8ca-107">Адрес сервера для проверки подлинности на основе файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="3a8ca-107">The server address for cookie-based authentication.</span></span>

<span data-ttu-id="3a8ca-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3a8ca-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a8ca-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a8ca-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="3a8ca-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3a8ca-110">Property value</span></span>

<span data-ttu-id="3a8ca-111">Новый адрес сервера для проверки подлинности на основе файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="3a8ca-111">The new server address for cookie-based authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a8ca-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3a8ca-112">Requirements</span></span>



| <span data-ttu-id="3a8ca-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3a8ca-113">Requirement</span></span> | <span data-ttu-id="3a8ca-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3a8ca-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8ca-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a8ca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3a8ca-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a8ca-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="3a8ca-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a8ca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3a8ca-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a8ca-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3a8ca-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3a8ca-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a8ca-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a8ca-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3a8ca-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3a8ca-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a8ca-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a8ca-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a8ca-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a8ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a8ca-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="3a8ca-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





