---
title: IMsRdpClientTransportSettings2 Гатевайпреаусрекуиремент, свойство
description: Указывает или получает параметр, указывающий, включена ли функция одноразового пароля (OTP) шлюза удаленный рабочий стол.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайпреаусрекуиремент
- Службы удаленных рабочих столов свойства Гатевайпреаусрекуиремент, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайпреаусрекуиремент
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535327"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a><span data-ttu-id="8787f-106">Свойство IMsRdpClientTransportSettings2:: Гатевайпреаусрекуиремент</span><span class="sxs-lookup"><span data-stu-id="8787f-106">IMsRdpClientTransportSettings2::GatewayPreAuthRequirement property</span></span>

<span data-ttu-id="8787f-107">Указывает или получает параметр, указывающий, включена ли функция одноразового пароля (OTP) шлюза удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="8787f-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature is enabled.</span></span>

<span data-ttu-id="8787f-108">Если включен OTP, **гатевайпреаусрекуиремент** пытается запросить файл cookie OTP из хранилища файлов cookie Интернета с помощью свойства [**гатевайпреауссервераддр**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) .</span><span class="sxs-lookup"><span data-stu-id="8787f-108">When OTP is enabled, **GatewayPreAuthRequirement** tries to query the OTP cookie from the Internet cookie store by using the [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) property.</span></span> <span data-ttu-id="8787f-109">В случае успеха **гатевайпреаусрекуиремент** отправляет файл cookie OTP на сервер брандмауэра (например, Microsoft Internet Security and Acceleration \[ ISA \] Server) для предварительной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8787f-109">If successful, **GatewayPreAuthRequirement** sends the OTP cookie to the firewall server (such as Microsoft Internet Security and Acceleration \[ISA\] server) for pre-authentication.</span></span>

<span data-ttu-id="8787f-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8787f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8787f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8787f-111">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a><span data-ttu-id="8787f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8787f-112">Property value</span></span>

<span data-ttu-id="8787f-113">Если задано значение 1, функция OTP включена.</span><span class="sxs-lookup"><span data-stu-id="8787f-113">If set to 1, the OTP feature is enabled.</span></span> <span data-ttu-id="8787f-114">Если задано значение 0, функция OTP отключена.</span><span class="sxs-lookup"><span data-stu-id="8787f-114">If set to 0, the OTP feature is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8787f-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8787f-115">Error codes</span></span>

<span data-ttu-id="8787f-116">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="8787f-116">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="8787f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8787f-117">Requirements</span></span>



| <span data-ttu-id="8787f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8787f-118">Requirement</span></span> | <span data-ttu-id="8787f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8787f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8787f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8787f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8787f-121">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="8787f-121">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="8787f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8787f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8787f-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8787f-123">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="8787f-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8787f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8787f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8787f-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="8787f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8787f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8787f-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8787f-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="8787f-128">IID</span><span class="sxs-lookup"><span data-stu-id="8787f-128">IID</span></span><br/>                      | <span data-ttu-id="8787f-129">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="8787f-129">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8787f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8787f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8787f-131">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="8787f-131">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="8787f-132">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="8787f-132">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





