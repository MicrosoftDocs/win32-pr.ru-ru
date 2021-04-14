---
title: IMsRdpClientTransportSettings2 Гатевайсуппортурл, свойство
description: Указывает или получает веб-адрес сайта, который предоставляет техническую поддержку для этого сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайсуппортурл
- Службы удаленных рабочих столов свойства Гатевайсуппортурл, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайсуппортурл
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4212dd03d5fb217753e14c2869973bda87476367
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415037"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a><span data-ttu-id="53f19-106">Свойство IMsRdpClientTransportSettings2:: Гатевайсуппортурл</span><span class="sxs-lookup"><span data-stu-id="53f19-106">IMsRdpClientTransportSettings2::GatewaySupportUrl property</span></span>

<span data-ttu-id="53f19-107">Указывает или получает веб-адрес сайта, который предоставляет техническую поддержку для этого сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="53f19-107">Specifies or retrieves the web address of the site that provides technical support for this Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="53f19-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="53f19-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f19-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53f19-109">Syntax</span></span>


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a><span data-ttu-id="53f19-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="53f19-110">Property value</span></span>

<span data-ttu-id="53f19-111">Указывает или получает веб-адрес сайта, который предоставляет техническую поддержку для этого сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="53f19-111">Specifies or retrieves the web address of the site that provides technical support for this RD Gateway server.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f19-112">Требования</span><span class="sxs-lookup"><span data-stu-id="53f19-112">Requirements</span></span>



| <span data-ttu-id="53f19-113">Требование</span><span class="sxs-lookup"><span data-stu-id="53f19-113">Requirement</span></span> | <span data-ttu-id="53f19-114">Значение</span><span class="sxs-lookup"><span data-stu-id="53f19-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f19-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53f19-115">Minimum supported client</span></span><br/> | <span data-ttu-id="53f19-116">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="53f19-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="53f19-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53f19-117">Minimum supported server</span></span><br/> | <span data-ttu-id="53f19-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53f19-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="53f19-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="53f19-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="53f19-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53f19-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="53f19-121">DLL</span><span class="sxs-lookup"><span data-stu-id="53f19-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53f19-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53f19-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="53f19-123">IID</span><span class="sxs-lookup"><span data-stu-id="53f19-123">IID</span></span><br/>                      | <span data-ttu-id="53f19-124">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="53f19-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53f19-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53f19-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f19-126">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="53f19-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="53f19-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="53f19-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





