---
title: IMsRdpClientTransportSettings2 Гатевайдомаин, свойство
description: Указывает или получает доменное имя пользователя, предоставленного на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 792ff7c6-afeb-4a2a-86b4-7722513a08e0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайдомаин
- Службы удаленных рабочих столов свойства Гатевайдомаин, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайдомаин
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayDomain
- IMsRdpClientTransportSettings2.get_GatewayDomain
- IMsRdpClientTransportSettings2.put_GatewayDomain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088780fbbaa4ab86fc416a3e9aa353920cc25e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415041"
---
# <a name="imsrdpclienttransportsettings2gatewaydomain-property"></a><span data-ttu-id="06c0d-106">Свойство IMsRdpClientTransportSettings2:: Гатевайдомаин</span><span class="sxs-lookup"><span data-stu-id="06c0d-106">IMsRdpClientTransportSettings2::GatewayDomain property</span></span>

<span data-ttu-id="06c0d-107">Указывает или получает доменное имя пользователя, предоставленного на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="06c0d-107">Specifies or retrieves the domain name of a user that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="06c0d-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="06c0d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c0d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06c0d-109">Syntax</span></span>


```C++
HRESULT put_GatewayDomain(
  [in]  BSTR proxyDomain
);

HRESULT get_GatewayDomain(
  [out] BSTR *pProxyDomain
);
```



## <a name="property-value"></a><span data-ttu-id="06c0d-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="06c0d-110">Property value</span></span>

<span data-ttu-id="06c0d-111">Доменное имя, которое предоставляется для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="06c0d-111">The domain name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06c0d-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="06c0d-112">Error codes</span></span>

<span data-ttu-id="06c0d-113">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="06c0d-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c0d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="06c0d-114">Requirements</span></span>



| <span data-ttu-id="06c0d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="06c0d-115">Requirement</span></span> | <span data-ttu-id="06c0d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="06c0d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c0d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06c0d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="06c0d-118">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="06c0d-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="06c0d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06c0d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="06c0d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06c0d-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="06c0d-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="06c0d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="06c0d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06c0d-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="06c0d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="06c0d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06c0d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06c0d-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="06c0d-125">IID</span><span class="sxs-lookup"><span data-stu-id="06c0d-125">IID</span></span><br/>                      | <span data-ttu-id="06c0d-126">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="06c0d-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06c0d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06c0d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c0d-128">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="06c0d-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="06c0d-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="06c0d-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





