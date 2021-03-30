---
title: Имсрдпклиенттранспортсеттингс Гатевайиссуппортед, свойство
description: Указывает, поддерживается ли шлюз удаленных рабочих столов удаленный рабочий стол.
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайиссуппортед
- Службы удаленных рабочих столов свойства Гатевайиссуппортед, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайиссуппортед
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414760"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a><span data-ttu-id="a02f3-106">Свойство Имсрдпклиенттранспортсеттингс:: Гатевайиссуппортед</span><span class="sxs-lookup"><span data-stu-id="a02f3-106">IMsRdpClientTransportSettings::GatewayIsSupported property</span></span>

<span data-ttu-id="a02f3-107">Указывает, поддерживается ли шлюз удаленных рабочих столов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="a02f3-107">Specifies whether Remote Desktop Gateway (RD Gateway) is supported.</span></span>

<span data-ttu-id="a02f3-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a02f3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a02f3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a02f3-109">Syntax</span></span>


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a><span data-ttu-id="a02f3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a02f3-110">Property value</span></span>

<span data-ttu-id="a02f3-111">Указывает, поддерживается ли шлюз удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="a02f3-111">Specifies whether RD Gateway is supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a02f3-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a02f3-112">Error codes</span></span>

<span data-ttu-id="a02f3-113">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="a02f3-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a02f3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a02f3-114">Requirements</span></span>



| <span data-ttu-id="a02f3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a02f3-115">Requirement</span></span> | <span data-ttu-id="a02f3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a02f3-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a02f3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a02f3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a02f3-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a02f3-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a02f3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a02f3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a02f3-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a02f3-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a02f3-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a02f3-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a02f3-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a02f3-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a02f3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a02f3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a02f3-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a02f3-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a02f3-125">IID</span><span class="sxs-lookup"><span data-stu-id="a02f3-125">IID</span></span><br/>                      | <span data-ttu-id="a02f3-126">IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="a02f3-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a02f3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a02f3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a02f3-128">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="a02f3-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





