---
title: IMsRdpClient8 Сендремотеактион, метод
description: Вызывает выполнение действия в удаленном сеансе.
ms.assetid: d6a43662-7e51-404a-a3f9-a8b51cbc69d1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сендремотеактион
- Службы удаленных рабочих столов метода Сендремотеактион, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Сендремотеактион
- Службы удаленных рабочих столов метода Сендремотеактион, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Сендремотеактион
- Службы удаленных рабочих столов метода Сендремотеактион, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Сендремотеактион
topic_type:
- apiref
api_name:
- IMsRdpClient8.SendRemoteAction
- IMsRdpClient9.SendRemoteAction
- IMsRdpClient10.SendRemoteAction
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28fc9695686402e0a8e98ed17fc1bc6a47939d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493194"
---
# <a name="imsrdpclient8sendremoteaction-method"></a><span data-ttu-id="e90d8-110">Метод IMsRdpClient8:: Сендремотеактион</span><span class="sxs-lookup"><span data-stu-id="e90d8-110">IMsRdpClient8::SendRemoteAction method</span></span>

<span data-ttu-id="e90d8-111">Вызывает выполнение действия в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="e90d8-111">Causes an action to be performed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90d8-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e90d8-112">Syntax</span></span>


```C++
HRESULT SendRemoteAction(
  [in] RemoteSessionActionType actionType
);
```



## <a name="parameters"></a><span data-ttu-id="e90d8-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="e90d8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90d8-114">Некоторая  \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e90d8-114">*actionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90d8-115">Значение перечисления [**ремотесессионактионтипе**](remotesessionactiontype.md) , указывающее действие, которое будет отправлено удаленному сеансу.</span><span class="sxs-lookup"><span data-stu-id="e90d8-115">A value of the [**RemoteSessionActionType**](remotesessionactiontype.md) enumeration that specifies the action to send to the remote session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90d8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e90d8-116">Return value</span></span>

<span data-ttu-id="e90d8-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e90d8-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e90d8-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e90d8-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90d8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e90d8-119">Requirements</span></span>



| <span data-ttu-id="e90d8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e90d8-120">Requirement</span></span> | <span data-ttu-id="e90d8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e90d8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e90d8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e90d8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e90d8-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e90d8-123">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="e90d8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e90d8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e90d8-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e90d8-125">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="e90d8-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e90d8-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="e90d8-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90d8-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e90d8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e90d8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90d8-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90d8-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e90d8-130">IID</span><span class="sxs-lookup"><span data-stu-id="e90d8-130">IID</span></span><br/>                      | <span data-ttu-id="e90d8-131">IID \_ IMsRdpClient8 определен как 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="e90d8-131">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e90d8-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e90d8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90d8-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e90d8-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e90d8-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e90d8-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e90d8-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e90d8-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





