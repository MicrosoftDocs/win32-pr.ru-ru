---
title: IMsRdpClient8 AdvancedSettings9, свойство
description: Содержит объект, который поддерживает интерфейс IMsRdpClientAdvancedSettings8.
ms.assetid: eb7bf118-15e7-4a11-91b1-e48f18afb436
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings9
- Службы удаленных рабочих столов свойства AdvancedSettings9, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings9
- Службы удаленных рабочих столов свойства AdvancedSettings9, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings9
- Службы удаленных рабочих столов свойства AdvancedSettings9, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings9
topic_type:
- apiref
api_name:
- IMsRdpClient8.AdvancedSettings9
- IMsRdpClient8.get_AdvancedSettings9
- IMsRdpClient9.AdvancedSettings9
- IMsRdpClient9.get_AdvancedSettings9
- IMsRdpClient10.AdvancedSettings9
- IMsRdpClient10.get_AdvancedSettings9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fce4c6f07b0c6c798d613e5312b3ae2b258c9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682148"
---
# <a name="imsrdpclient8advancedsettings9-property"></a><span data-ttu-id="c8a2b-110">Свойство IMsRdpClient8:: AdvancedSettings9</span><span class="sxs-lookup"><span data-stu-id="c8a2b-110">IMsRdpClient8::AdvancedSettings9 property</span></span>

<span data-ttu-id="c8a2b-111">Содержит объект, который поддерживает интерфейс [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .</span><span class="sxs-lookup"><span data-stu-id="c8a2b-111">Contains an object that supports the [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface.</span></span>

<span data-ttu-id="c8a2b-112">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c8a2b-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a2b-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8a2b-113">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings9(
  [out, retval] IMsRdpClientAdvancedSettings8 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="c8a2b-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c8a2b-114">Property value</span></span>

<span data-ttu-id="c8a2b-115">Интерфейс [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) , представляющий объект Settings.</span><span class="sxs-lookup"><span data-stu-id="c8a2b-115">An [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface that represents the settings object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a2b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c8a2b-116">Requirements</span></span>



| <span data-ttu-id="c8a2b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c8a2b-117">Requirement</span></span> | <span data-ttu-id="c8a2b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c8a2b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a2b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8a2b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c8a2b-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c8a2b-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="c8a2b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8a2b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c8a2b-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8a2b-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="c8a2b-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c8a2b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c8a2b-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8a2b-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c8a2b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c8a2b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8a2b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8a2b-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c8a2b-127">IID</span><span class="sxs-lookup"><span data-stu-id="c8a2b-127">IID</span></span><br/>                      | <span data-ttu-id="c8a2b-128">IID \_ IMsRdpClient8 определен как 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="c8a2b-128">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c8a2b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8a2b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a2b-130">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c8a2b-130">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c8a2b-131">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c8a2b-131">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c8a2b-132">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="c8a2b-132">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





