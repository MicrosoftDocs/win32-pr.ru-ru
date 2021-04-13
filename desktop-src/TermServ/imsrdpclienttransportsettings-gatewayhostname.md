---
title: Имсрдпклиенттранспортсеттингс Гатевайхостнаме, свойство
description: Указывает имя узла сервера шлюза удаленный рабочий стол.
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайхостнаме
- Службы удаленных рабочих столов свойства Гатевайхостнаме, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайхостнаме
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03835faf48fa8aba557f82da158fdba827a84831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340445"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a><span data-ttu-id="ccbc7-106">Свойство Имсрдпклиенттранспортсеттингс:: Гатевайхостнаме</span><span class="sxs-lookup"><span data-stu-id="ccbc7-106">IMsRdpClientTransportSettings::GatewayHostname property</span></span>

<span data-ttu-id="ccbc7-107">Указывает имя узла сервера шлюза удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ccbc7-107">Specifies the host name of the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="ccbc7-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ccbc7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccbc7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccbc7-109">Syntax</span></span>


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a><span data-ttu-id="ccbc7-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ccbc7-110">Property value</span></span>

<span data-ttu-id="ccbc7-111">Строка, содержащая имя узла сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ccbc7-111">A string that contains the RD Gateway server host name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccbc7-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ccbc7-112">Error codes</span></span>

<span data-ttu-id="ccbc7-113">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="ccbc7-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccbc7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ccbc7-114">Requirements</span></span>



| <span data-ttu-id="ccbc7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ccbc7-115">Requirement</span></span> | <span data-ttu-id="ccbc7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ccbc7-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccbc7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ccbc7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ccbc7-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccbc7-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ccbc7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ccbc7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ccbc7-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccbc7-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ccbc7-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ccbc7-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccbc7-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccbc7-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ccbc7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ccbc7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccbc7-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccbc7-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ccbc7-125">IID</span><span class="sxs-lookup"><span data-stu-id="ccbc7-125">IID</span></span><br/>                      | <span data-ttu-id="ccbc7-126">IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="ccbc7-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ccbc7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccbc7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccbc7-128">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="ccbc7-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





