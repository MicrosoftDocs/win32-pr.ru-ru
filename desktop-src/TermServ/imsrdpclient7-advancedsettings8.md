---
title: IMsRdpClient7 AdvancedSettings8, свойство
description: Извлекает объект, который поддерживает интерфейс IMsRdpClientAdvancedSettings7.
ms.assetid: e3bb3b74-52db-4ec2-999c-9d12c24f65be
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings8
- Службы удаленных рабочих столов свойства AdvancedSettings8, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство AdvancedSettings8
- Службы удаленных рабочих столов свойства AdvancedSettings8, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings8
- Службы удаленных рабочих столов свойства AdvancedSettings8, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings8
- Службы удаленных рабочих столов свойства AdvancedSettings8, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings8
topic_type:
- apiref
api_name:
- IMsRdpClient7.AdvancedSettings8
- IMsRdpClient7.get_AdvancedSettings8
- IMsRdpClient8.AdvancedSettings8
- IMsRdpClient8.get_AdvancedSettings8
- IMsRdpClient9.AdvancedSettings8
- IMsRdpClient9.get_AdvancedSettings8
- IMsRdpClient10.AdvancedSettings8
- IMsRdpClient10.get_AdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 887306216682ba1555739a4258b8337694fabe0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135323"
---
# <a name="imsrdpclient7advancedsettings8-property"></a><span data-ttu-id="e020b-112">Свойство IMsRdpClient7:: AdvancedSettings8</span><span class="sxs-lookup"><span data-stu-id="e020b-112">IMsRdpClient7::AdvancedSettings8 property</span></span>

<span data-ttu-id="e020b-113">Извлекает объект, который поддерживает интерфейс [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .</span><span class="sxs-lookup"><span data-stu-id="e020b-113">Retrieves an object that supports the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface.</span></span>

<span data-ttu-id="e020b-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e020b-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e020b-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e020b-115">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings8(
  [out, retval] IMsRdpClientAdvancedSettings7 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="e020b-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e020b-116">Property value</span></span>

<span data-ttu-id="e020b-117">Адрес указателя интерфейса [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) , который получает объект.</span><span class="sxs-lookup"><span data-stu-id="e020b-117">The address of an [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e020b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e020b-118">Requirements</span></span>



| <span data-ttu-id="e020b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e020b-119">Requirement</span></span> | <span data-ttu-id="e020b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e020b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e020b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e020b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e020b-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e020b-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="e020b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e020b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e020b-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e020b-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="e020b-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e020b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e020b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e020b-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e020b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e020b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e020b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e020b-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e020b-129">IID</span><span class="sxs-lookup"><span data-stu-id="e020b-129">IID</span></span><br/>                      | <span data-ttu-id="e020b-130">IID \_ IMsRdpClient7 определен как b2a5b5ce-3461-444a-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="e020b-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e020b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e020b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e020b-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e020b-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e020b-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e020b-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e020b-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e020b-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e020b-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e020b-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





