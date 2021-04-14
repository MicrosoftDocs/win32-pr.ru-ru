---
title: IMsRdpClientTransportSettings2 Гатевайпреауссервераддр, свойство
description: Указывает или получает веб-адрес сервера предварительной проверки подлинности, который используется для функции одноразового пароля шлюза удаленный рабочий стол (OTP).
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайпреауссервераддр
- Службы удаленных рабочих столов свойства Гатевайпреауссервераддр, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайпреауссервераддр
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415040"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a><span data-ttu-id="3098c-106">Свойство IMsRdpClientTransportSettings2:: Гатевайпреауссервераддр</span><span class="sxs-lookup"><span data-stu-id="3098c-106">IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr property</span></span>

<span data-ttu-id="3098c-107">Указывает или получает веб-адрес сервера предварительной проверки подлинности, который используется для функции одноразового пароля шлюза удаленный рабочий стол (OTP).</span><span class="sxs-lookup"><span data-stu-id="3098c-107">Specifies or retrieves the web address of the pre-authentication server, which is used for the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature.</span></span>

<span data-ttu-id="3098c-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3098c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3098c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3098c-109">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="3098c-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3098c-110">Property value</span></span>

<span data-ttu-id="3098c-111">Веб-адрес сервера предварительной проверки подлинности; Например, веб-адрес сервера Microsoft Internet Security and Acceleration (ISA) Server.</span><span class="sxs-lookup"><span data-stu-id="3098c-111">The web address of the pre-authentication server; for example, the web address of the Microsoft Internet Security and Acceleration (ISA) server.</span></span> <span data-ttu-id="3098c-112">Укажите веб-адрес, используя формат "https://*имя узла*. *Имя_домена*. com/*имя_веб-сайта* или *имя узла* HTTPS://. *Имя_домена*. com/*имя_веб-сайта*.</span><span class="sxs-lookup"><span data-stu-id="3098c-112">Specify the web address by using the format "https://*HostName*.*DomainName*.com/*WebsiteName*" or "https://*HostName*.*DomainName*.com/*WebsiteName*".</span></span>

## <a name="error-codes"></a><span data-ttu-id="3098c-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3098c-113">Error codes</span></span>

<span data-ttu-id="3098c-114">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="3098c-114">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="3098c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3098c-115">Requirements</span></span>



| <span data-ttu-id="3098c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3098c-116">Requirement</span></span> | <span data-ttu-id="3098c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3098c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3098c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3098c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3098c-119">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="3098c-119">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="3098c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3098c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3098c-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3098c-121">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="3098c-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3098c-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="3098c-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3098c-123"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="3098c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3098c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3098c-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3098c-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="3098c-126">IID</span><span class="sxs-lookup"><span data-stu-id="3098c-126">IID</span></span><br/>                      | <span data-ttu-id="3098c-127">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="3098c-127">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3098c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3098c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3098c-129">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="3098c-129">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="3098c-130">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="3098c-130">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





