---
title: IMsRdpClientAdvancedSettings6 AuthenticationType, свойство
description: Указывает тип проверки подлинности, используемый для этого соединения.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AuthenticationType
- Службы удаленных рабочих столов свойства AuthenticationType, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, Свойство AuthenticationType
- Службы удаленных рабочих столов свойства AuthenticationType, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, Свойство AuthenticationType
- Службы удаленных рабочих столов свойства AuthenticationType, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, Свойство AuthenticationType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135906"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a><span data-ttu-id="28d63-110">Свойство IMsRdpClientAdvancedSettings6:: AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="28d63-110">IMsRdpClientAdvancedSettings6::AuthenticationType property</span></span>

<span data-ttu-id="28d63-111">Указывает тип проверки подлинности, используемый для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="28d63-111">Specifies the type of authentication used for this connection.</span></span>

<span data-ttu-id="28d63-112">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="28d63-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d63-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28d63-113">Syntax</span></span>


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a><span data-ttu-id="28d63-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="28d63-114">Property value</span></span>

<span data-ttu-id="28d63-115">Получает значение, указывающее тип проверки подлинности, используемый для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="28d63-115">Receives a value that specifies the type of authentication used for this connection.</span></span> <span data-ttu-id="28d63-116">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="28d63-116">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="28d63-117">0</span><span class="sxs-lookup"><span data-stu-id="28d63-117">0</span></span>
</dt> <dd>

<span data-ttu-id="28d63-118">Проверка подлинности не используется.</span><span class="sxs-lookup"><span data-stu-id="28d63-118">No authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="28d63-119">1</span><span class="sxs-lookup"><span data-stu-id="28d63-119">1</span></span>
</dt> <dd>

<span data-ttu-id="28d63-120">Используется проверка подлинности с помощью сертификата.</span><span class="sxs-lookup"><span data-stu-id="28d63-120">Certificate authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="28d63-121">2</span><span class="sxs-lookup"><span data-stu-id="28d63-121">2</span></span>
</dt> <dd>

<span data-ttu-id="28d63-122">Используется проверка подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="28d63-122">Kerberos authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="28d63-123">3</span><span class="sxs-lookup"><span data-stu-id="28d63-123">3</span></span>
</dt> <dd>

<span data-ttu-id="28d63-124">Используются как сертификат, так и проверка подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="28d63-124">Both certificate and Kerberos authentication are used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28d63-125">Требования</span><span class="sxs-lookup"><span data-stu-id="28d63-125">Requirements</span></span>



| <span data-ttu-id="28d63-126">Требование</span><span class="sxs-lookup"><span data-stu-id="28d63-126">Requirement</span></span> | <span data-ttu-id="28d63-127">Значение</span><span class="sxs-lookup"><span data-stu-id="28d63-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28d63-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28d63-128">Minimum supported client</span></span><br/> | <span data-ttu-id="28d63-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28d63-129">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="28d63-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28d63-130">Minimum supported server</span></span><br/> | <span data-ttu-id="28d63-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28d63-131">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="28d63-132">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="28d63-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="28d63-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28d63-133"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="28d63-134">DLL</span><span class="sxs-lookup"><span data-stu-id="28d63-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28d63-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28d63-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="28d63-136">IID</span><span class="sxs-lookup"><span data-stu-id="28d63-136">IID</span></span><br/>                      | <span data-ttu-id="28d63-137">IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="28d63-137">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28d63-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28d63-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d63-139">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="28d63-139">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="28d63-140">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="28d63-140">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="28d63-141">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="28d63-141">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





