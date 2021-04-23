---
title: IMsRdpClientTransportSettings2 Гатевайкредшаринг, свойство
description: Указывает или получает параметр, указывающий, включена ли функция общего доступа к учетным данным шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайкредшаринг
- Службы удаленных рабочих столов свойства Гатевайкредшаринг, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайкредшаринг
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489519"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a><span data-ttu-id="243cc-106">Свойство IMsRdpClientTransportSettings2:: Гатевайкредшаринг</span><span class="sxs-lookup"><span data-stu-id="243cc-106">IMsRdpClientTransportSettings2::GatewayCredSharing property</span></span>

<span data-ttu-id="243cc-107">Указывает или получает параметр, указывающий, включена ли функция общего доступа к учетным данным шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="243cc-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) credential sharing feature is enabled.</span></span> <span data-ttu-id="243cc-108">Если эта функция включена, удаленный рабочий стол элемент управления ActiveX пытается использовать те же учетные данные для проверки подлинности на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) и на сервере шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="243cc-108">When the feature is enabled, the Remote Desktop ActiveX control tries to use the same credentials to authenticate to the Remote Desktop Session Host (RD Session Host) server and to the RD Gateway server.</span></span>

<span data-ttu-id="243cc-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="243cc-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="243cc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="243cc-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a><span data-ttu-id="243cc-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="243cc-111">Property value</span></span>

<span data-ttu-id="243cc-112">Если задано значение One, совместное использование учетных данных включено.</span><span class="sxs-lookup"><span data-stu-id="243cc-112">If set to one, credential sharing is enabled.</span></span> <span data-ttu-id="243cc-113">Если задано значение 0, совместное использование учетных данных отключено.</span><span class="sxs-lookup"><span data-stu-id="243cc-113">If set to zero, credential sharing is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="243cc-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="243cc-114">Error codes</span></span>

<span data-ttu-id="243cc-115">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="243cc-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="243cc-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="243cc-116">Remarks</span></span>

<span data-ttu-id="243cc-117">Это свойство используется элементом управления ActiveX для реализации единого запроса на обмен учетными данными между сервером узла сеансов удаленных рабочих столов и сервером шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="243cc-117">This property is used by the ActiveX control to implement a single prompt for credential sharing between the RD Session Host server and the RD Gateway server.</span></span> <span data-ttu-id="243cc-118">Совместное использование учетных данных не поддерживает общий доступ к паролю с использованием [**гатевайпассворд**](imsrdpclienttransportsettings2-gatewaypassword.md) или [**клеартекстпассворд**](imstscnonscriptable-cleartextpassword.md).</span><span class="sxs-lookup"><span data-stu-id="243cc-118">Credential sharing does not support web-based password sharing with [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) or [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="243cc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="243cc-119">Requirements</span></span>



| <span data-ttu-id="243cc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="243cc-120">Requirement</span></span> | <span data-ttu-id="243cc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="243cc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="243cc-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="243cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="243cc-123">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="243cc-123">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="243cc-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="243cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="243cc-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="243cc-125">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="243cc-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="243cc-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="243cc-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="243cc-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="243cc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="243cc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="243cc-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="243cc-129"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="243cc-130">IID</span><span class="sxs-lookup"><span data-stu-id="243cc-130">IID</span></span><br/>                      | <span data-ttu-id="243cc-131">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="243cc-131">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="243cc-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="243cc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243cc-133">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="243cc-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="243cc-134">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="243cc-134">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





