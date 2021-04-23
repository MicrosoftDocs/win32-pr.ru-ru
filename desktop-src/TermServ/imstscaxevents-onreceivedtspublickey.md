---
title: Имстскаксевентс Онрецеиведтспубликкэй, метод
description: Вызывается во время последовательности подключения, когда клиент получает открытый ключ с сервера. Это событие вызывается, только если свойство Нотифитспубликкэй имеет значение VARIANT \_ true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онрецеиведтспубликкэй
- Службы удаленных рабочих столов метода Онрецеиведтспубликкэй, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онрецеиведтспубликкэй
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491325"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a><span data-ttu-id="b2909-107">Метод Имстскаксевентс:: Онрецеиведтспубликкэй</span><span class="sxs-lookup"><span data-stu-id="b2909-107">IMsTscAxEvents::OnReceivedTSPublicKey method</span></span>

<span data-ttu-id="b2909-108">Вызывается во время последовательности подключения, когда клиент получает открытый ключ с сервера.</span><span class="sxs-lookup"><span data-stu-id="b2909-108">Called during the connection sequence when the client retrieves the public key from the server.</span></span> <span data-ttu-id="b2909-109">Это событие вызывается, только если свойство **нотифитспубликкэй** имеет значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="b2909-109">This event is only called if the **NotifyTSPublicKey** property is **VARIANT\_TRUE**.</span></span> <span data-ttu-id="b2909-110">Это происходит после [**подключения**](imstscaxevents-onconnecting.md), но перед [**онаусентикатионварнингдисплайед**](imstscaxevents-onauthenticationwarningdisplayed.md) и [**подключением**](imstscaxevents-onconnected.md).</span><span class="sxs-lookup"><span data-stu-id="b2909-110">This is after [**OnConnecting**](imstscaxevents-onconnecting.md), but before [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) and [**OnConnected**](imstscaxevents-onconnected.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2909-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2909-111">Syntax</span></span>


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a><span data-ttu-id="b2909-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2909-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2909-113">*PublicKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2909-113">*publicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2909-114">Содержит открытый ключ удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="b2909-114">Contains the public key of the remote machine.</span></span>

</dd> <dt>

<span data-ttu-id="b2909-115">*пфконтинуелогон* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b2909-115">*pfContinueLogon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2909-116">Указатель на переменную **\_ bool типа Variant** , которая получает, должен ли продолжаться процесс входа в систему.</span><span class="sxs-lookup"><span data-stu-id="b2909-116">A pointer to a **VARIANT\_BOOL** variable that receives whether the logon process should continue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2909-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2909-117">Return value</span></span>

<span data-ttu-id="b2909-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b2909-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2909-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2909-119">Remarks</span></span>

<span data-ttu-id="b2909-120">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b2909-120">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2909-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b2909-121">Requirements</span></span>



| <span data-ttu-id="b2909-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b2909-122">Requirement</span></span> | <span data-ttu-id="b2909-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b2909-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2909-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2909-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b2909-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2909-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b2909-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2909-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b2909-127">Windows Server 2008, Windows Server 2008 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="b2909-127">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="b2909-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b2909-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2909-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2909-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2909-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b2909-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2909-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2909-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2909-132">IID</span><span class="sxs-lookup"><span data-stu-id="b2909-132">IID</span></span><br/>                      | <span data-ttu-id="b2909-133">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="b2909-133">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b2909-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2909-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2909-135">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="b2909-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





