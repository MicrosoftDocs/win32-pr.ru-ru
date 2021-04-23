---
title: IMsRdpClientAdvancedSettings6 ПКБ, свойство
description: Задает параметр предварительного подключения BLOB-объекта (ПКБ), используемый перед подключением для передачи на сервер. | IMsRdpClientAdvancedSettings6 ПКБ, свойство
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства ПКБ
- Службы удаленных рабочих столов свойства ПКБ, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство ПКБ
- Службы удаленных рабочих столов свойства ПКБ, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство ПКБ
- Службы удаленных рабочих столов свойства ПКБ, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство ПКБ
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da9cfa12ec944ea8f745ec3399c2a53f6b7c6b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674582"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a><span data-ttu-id="ef078-111">IMsRdpClientAdvancedSettings6::P свойство CB</span><span class="sxs-lookup"><span data-stu-id="ef078-111">IMsRdpClientAdvancedSettings6::PCB property</span></span>

<span data-ttu-id="ef078-112">Задает параметр предварительного подключения BLOB-объекта (ПКБ), используемый перед подключением для передачи на сервер.</span><span class="sxs-lookup"><span data-stu-id="ef078-112">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="ef078-113">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ef078-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef078-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef078-114">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="ef078-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ef078-115">Property value</span></span>

<span data-ttu-id="ef078-116">Указывает параметр большого двоичного объекта, который будет использоваться перед подключением.</span><span class="sxs-lookup"><span data-stu-id="ef078-116">Specifies the BLOB setting to use prior to connecting.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef078-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef078-117">Remarks</span></span>

<span data-ttu-id="ef078-118">Это свойство поддерживается только клиентами подключение к удаленному рабочему столу 6,1 и 7,0.</span><span class="sxs-lookup"><span data-stu-id="ef078-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="ef078-119">Сервер использует параметр большого двоичного объекта для определения целевого процесса для соединения.</span><span class="sxs-lookup"><span data-stu-id="ef078-119">The server uses the BLOB setting to identify the target process for the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef078-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ef078-120">Requirements</span></span>



| <span data-ttu-id="ef078-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ef078-121">Requirement</span></span> | <span data-ttu-id="ef078-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ef078-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef078-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef078-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ef078-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ef078-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="ef078-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef078-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ef078-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef078-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="ef078-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ef078-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef078-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef078-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ef078-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ef078-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef078-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef078-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ef078-131">IID</span><span class="sxs-lookup"><span data-stu-id="ef078-131">IID</span></span><br/>                      | <span data-ttu-id="ef078-132">IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="ef078-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef078-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef078-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef078-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ef078-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ef078-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ef078-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ef078-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ef078-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





