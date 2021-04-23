---
title: Имсрдпклиенттранспортсеттингс Гатевайпрофилеусажемесод, свойство
description: Указывает, следует ли использовать параметры шлюза удаленный рабочий стол по умолчанию (шлюз удаленных рабочих столов).
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайпрофилеусажемесод
- Службы удаленных рабочих столов свойства Гатевайпрофилеусажемесод, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайпрофилеусажемесод
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a12a9836e89348d1eb7ccdf680b23e2695c938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415460"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a><span data-ttu-id="331d6-106">Свойство Имсрдпклиенттранспортсеттингс:: Гатевайпрофилеусажемесод</span><span class="sxs-lookup"><span data-stu-id="331d6-106">IMsRdpClientTransportSettings::GatewayProfileUsageMethod property</span></span>

<span data-ttu-id="331d6-107">Указывает, следует ли использовать параметры шлюза удаленный рабочий стол по умолчанию (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="331d6-107">Specifies whether to use default Remote Desktop Gateway (RD Gateway) settings.</span></span>

<span data-ttu-id="331d6-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="331d6-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="331d6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="331d6-109">Syntax</span></span>


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="331d6-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="331d6-110">Property value</span></span>

<span data-ttu-id="331d6-111">Метод использования профиля шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="331d6-111">The RD Gateway profile usage method.</span></span> <span data-ttu-id="331d6-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="331d6-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span data-ttu-id="331d6-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**Таймер TSC \_ \_Режим профиля \_ прокси \_ по умолчанию** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="331d6-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC\_PROXY\_PROFILE\_MODE\_DEFAULT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="331d6-114">Используйте режим профиля по умолчанию, указанный администратором.</span><span class="sxs-lookup"><span data-stu-id="331d6-114">Use the default profile mode, as specified by the administrator.</span></span>

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span data-ttu-id="331d6-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**Таймер TSC \_ \_ \_ \_ Явный режим профиля прокси-сервера** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="331d6-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC\_PROXY\_PROFILE\_MODE\_EXPLICIT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="331d6-116">Используйте явные параметры, указанные пользователем.</span><span class="sxs-lookup"><span data-stu-id="331d6-116">Use explicit settings, as specified by the user.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="331d6-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="331d6-117">Error codes</span></span>

<span data-ttu-id="331d6-118">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="331d6-118">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="331d6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="331d6-119">Requirements</span></span>



| <span data-ttu-id="331d6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="331d6-120">Requirement</span></span> | <span data-ttu-id="331d6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="331d6-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="331d6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="331d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="331d6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="331d6-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="331d6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="331d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="331d6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="331d6-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="331d6-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="331d6-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="331d6-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="331d6-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="331d6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="331d6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="331d6-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="331d6-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="331d6-130">IID</span><span class="sxs-lookup"><span data-stu-id="331d6-130">IID</span></span><br/>                      | <span data-ttu-id="331d6-131">IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="331d6-131">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="331d6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="331d6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="331d6-133">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="331d6-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





