---
title: IMsRdpClientTransportSettings3 Гатевайауслогинпаже, свойство
description: Адрес веб-страницы входа, используемой для проверки подлинности пользователя.
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайауслогинпаже
- Службы удаленных рабочих столов свойства Гатевайауслогинпаже, интерфейс IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, свойство Гатевайауслогинпаже
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5be535dea0a89f1cf6e7c238029e53f38f58b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137506"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a><span data-ttu-id="70672-106">Свойство IMsRdpClientTransportSettings3:: Гатевайауслогинпаже</span><span class="sxs-lookup"><span data-stu-id="70672-106">IMsRdpClientTransportSettings3::GatewayAuthLoginPage property</span></span>

<span data-ttu-id="70672-107">Адрес веб-страницы входа, используемой для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="70672-107">The address of the login webpage to use to authenticate a user.</span></span>

<span data-ttu-id="70672-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="70672-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70672-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70672-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a><span data-ttu-id="70672-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="70672-110">Property value</span></span>

<span data-ttu-id="70672-111">Новый адрес веб-страницы входа.</span><span class="sxs-lookup"><span data-stu-id="70672-111">The new login webpage address.</span></span>

## <a name="requirements"></a><span data-ttu-id="70672-112">Требования</span><span class="sxs-lookup"><span data-stu-id="70672-112">Requirements</span></span>



| <span data-ttu-id="70672-113">Требование</span><span class="sxs-lookup"><span data-stu-id="70672-113">Requirement</span></span> | <span data-ttu-id="70672-114">Значение</span><span class="sxs-lookup"><span data-stu-id="70672-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70672-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70672-115">Minimum supported client</span></span><br/> | <span data-ttu-id="70672-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="70672-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="70672-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70672-117">Minimum supported server</span></span><br/> | <span data-ttu-id="70672-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70672-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="70672-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="70672-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="70672-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70672-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="70672-121">DLL</span><span class="sxs-lookup"><span data-stu-id="70672-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70672-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70672-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70672-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70672-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70672-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="70672-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





