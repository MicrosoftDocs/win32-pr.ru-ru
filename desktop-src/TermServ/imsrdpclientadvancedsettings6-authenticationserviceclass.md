---
title: IMsRdpClientAdvancedSettings6 Аусентикатионсервицекласс, свойство
description: Указывает имя участника-службы (SPN), используемое для проверки подлинности на сервере.
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Аусентикатионсервицекласс
- Службы удаленных рабочих столов свойства Аусентикатионсервицекласс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Аусентикатионсервицекласс
- Службы удаленных рабочих столов свойства Аусентикатионсервицекласс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Аусентикатионсервицекласс
- Службы удаленных рабочих столов свойства Аусентикатионсервицекласс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Аусентикатионсервицекласс
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.put_AuthenticationServiceClass
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618b55d1489f46e0e1119186bd5003fb68dbfebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802290"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a><span data-ttu-id="22415-110">Свойство IMsRdpClientAdvancedSettings6:: Аусентикатионсервицекласс</span><span class="sxs-lookup"><span data-stu-id="22415-110">IMsRdpClientAdvancedSettings6::AuthenticationServiceClass property</span></span>

<span data-ttu-id="22415-111">Указывает имя участника-службы (SPN), используемое для проверки подлинности на сервере.</span><span class="sxs-lookup"><span data-stu-id="22415-111">Specifies the service principal name (SPN) to use for authentication to the server.</span></span>

<span data-ttu-id="22415-112">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="22415-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="22415-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22415-113">Syntax</span></span>


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a><span data-ttu-id="22415-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="22415-114">Property value</span></span>

<span data-ttu-id="22415-115">Указывает имя субъекта-службы для использования.</span><span class="sxs-lookup"><span data-stu-id="22415-115">Specifies the service principal name to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="22415-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22415-116">Remarks</span></span>

<span data-ttu-id="22415-117">Это свойство поддерживается только клиентами подключение к удаленному рабочему столу 6,1 и 7,0.</span><span class="sxs-lookup"><span data-stu-id="22415-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="22415-118">Имена субъектов-служб (SPN) связаны с субъектом безопасности (пользователем или группами), в контексте безопасности которого выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="22415-118">Service principal names (SPNs) are associated with the security principal (user or groups) in whose security context the service executes.</span></span> <span data-ttu-id="22415-119">Имена участников-служб используются для поддержки взаимной проверки подлинности между клиентским приложением и службой.</span><span class="sxs-lookup"><span data-stu-id="22415-119">SPNs are used to support mutual authentication between a client application and a service.</span></span>

## <a name="requirements"></a><span data-ttu-id="22415-120">Требования</span><span class="sxs-lookup"><span data-stu-id="22415-120">Requirements</span></span>



| <span data-ttu-id="22415-121">Требование</span><span class="sxs-lookup"><span data-stu-id="22415-121">Requirement</span></span> | <span data-ttu-id="22415-122">Значение</span><span class="sxs-lookup"><span data-stu-id="22415-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22415-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22415-123">Minimum supported client</span></span><br/> | <span data-ttu-id="22415-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22415-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="22415-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22415-125">Minimum supported server</span></span><br/> | <span data-ttu-id="22415-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22415-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="22415-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="22415-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="22415-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22415-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="22415-129">DLL</span><span class="sxs-lookup"><span data-stu-id="22415-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22415-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22415-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="22415-131">IID</span><span class="sxs-lookup"><span data-stu-id="22415-131">IID</span></span><br/>                      | <span data-ttu-id="22415-132">IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="22415-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22415-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22415-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22415-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="22415-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="22415-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="22415-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="22415-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="22415-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





