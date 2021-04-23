---
title: IMsRdpClientTransportSettings2 Гатевайусернаме, свойство
description: Указывает или получает имя пользователя, предоставленное на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайусернаме
- Службы удаленных рабочих столов свойства Гатевайусернаме, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайусернаме
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48244c49c942c917c58bfc2790b423981f17fe98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672542"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a><span data-ttu-id="840e3-106">Свойство IMsRdpClientTransportSettings2:: Гатевайусернаме</span><span class="sxs-lookup"><span data-stu-id="840e3-106">IMsRdpClientTransportSettings2::GatewayUserName property</span></span>

<span data-ttu-id="840e3-107">Указывает или получает имя пользователя, предоставленное на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="840e3-107">Specifies or retrieves the user name that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="840e3-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="840e3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="840e3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="840e3-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a><span data-ttu-id="840e3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="840e3-110">Property value</span></span>

<span data-ttu-id="840e3-111">Имя пользователя, которое предоставляется для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="840e3-111">The user name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="840e3-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="840e3-112">Error codes</span></span>

<span data-ttu-id="840e3-113">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="840e3-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="840e3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="840e3-114">Requirements</span></span>



| <span data-ttu-id="840e3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="840e3-115">Requirement</span></span> | <span data-ttu-id="840e3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="840e3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="840e3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="840e3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="840e3-118">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="840e3-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="840e3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="840e3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="840e3-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="840e3-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="840e3-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="840e3-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="840e3-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="840e3-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="840e3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="840e3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="840e3-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="840e3-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="840e3-125">IID</span><span class="sxs-lookup"><span data-stu-id="840e3-125">IID</span></span><br/>                      | <span data-ttu-id="840e3-126">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="840e3-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="840e3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="840e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="840e3-128">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="840e3-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="840e3-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="840e3-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





