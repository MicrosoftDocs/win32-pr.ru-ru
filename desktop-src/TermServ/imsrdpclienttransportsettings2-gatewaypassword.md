---
title: IMsRdpClientTransportSettings2 Гатевайпассворд, свойство
description: Указывает пароль, предоставляемый пользователем для подключения к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайпассворд
- Службы удаленных рабочих столов свойства Гатевайпассворд, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайпассворд
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533872"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a><span data-ttu-id="ebea5-106">Свойство IMsRdpClientTransportSettings2:: Гатевайпассворд</span><span class="sxs-lookup"><span data-stu-id="ebea5-106">IMsRdpClientTransportSettings2::GatewayPassword property</span></span>

<span data-ttu-id="ebea5-107">Указывает пароль, предоставляемый пользователем для подключения к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="ebea5-107">Specifies the password that a user provides to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="ebea5-108">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="ebea5-108">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebea5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebea5-109">Syntax</span></span>


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a><span data-ttu-id="ebea5-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ebea5-110">Property value</span></span>

<span data-ttu-id="ebea5-111">Пароль, предоставляемый пользователем для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ebea5-111">The password that a user provides to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ebea5-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ebea5-112">Error codes</span></span>

<span data-ttu-id="ebea5-113">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="ebea5-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebea5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ebea5-114">Requirements</span></span>



| <span data-ttu-id="ebea5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ebea5-115">Requirement</span></span> | <span data-ttu-id="ebea5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ebea5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebea5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebea5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ebea5-118">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ebea5-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="ebea5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebea5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ebea5-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebea5-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="ebea5-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ebea5-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebea5-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebea5-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="ebea5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ebea5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebea5-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebea5-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="ebea5-125">IID</span><span class="sxs-lookup"><span data-stu-id="ebea5-125">IID</span></span><br/>                      | <span data-ttu-id="ebea5-126">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="ebea5-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebea5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebea5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebea5-128">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="ebea5-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="ebea5-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="ebea5-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





