---
title: Имстскаксевентс Ончаннелрецеиведдата, метод
description: Вызывается, когда клиент получает данные в виртуальном канале, поддерживающем скрипт.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ончаннелрецеиведдата
- Службы удаленных рабочих столов метода Ончаннелрецеиведдата, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Ончаннелрецеиведдата
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135758"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a><span data-ttu-id="ace1b-106">Метод Имстскаксевентс:: Ончаннелрецеиведдата</span><span class="sxs-lookup"><span data-stu-id="ace1b-106">IMsTscAxEvents::OnChannelReceivedData method</span></span>

<span data-ttu-id="ace1b-107">Вызывается, когда клиент получает данные в виртуальном канале, поддерживающем скрипт.</span><span class="sxs-lookup"><span data-stu-id="ace1b-107">Called when the client receives data on a scriptable virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace1b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ace1b-108">Syntax</span></span>


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a><span data-ttu-id="ace1b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ace1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace1b-110">*чаннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ace1b-110">*chanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace1b-111">Имя виртуального канала, на котором были получены данные.</span><span class="sxs-lookup"><span data-stu-id="ace1b-111">The name of the virtual channel on which data was received.</span></span> <span data-ttu-id="ace1b-112">Это имя соответствует одному из каналов, созданных при вызове метода [**имстскакс:: креатевиртуалчаннелс**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="ace1b-112">This name matches one of the channels created by the call to [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="ace1b-113">*данные* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ace1b-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace1b-114">Данные, полученные в виртуальном канале с помощью скрипта.</span><span class="sxs-lookup"><span data-stu-id="ace1b-114">The data received on the scriptable virtual channel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace1b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ace1b-115">Return value</span></span>

<span data-ttu-id="ace1b-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ace1b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ace1b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ace1b-117">Remarks</span></span>

<span data-ttu-id="ace1b-118">Дополнительные сведения об этом событии см. в статье [реализация виртуальных каналов с использованием скриптов с помощью веб-подключение к удаленному рабочему столу](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) .</span><span class="sxs-lookup"><span data-stu-id="ace1b-118">Refer to [Implementing Scriptable Virtual Channels using Remote Desktop Web Connection](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) for more information about this event.</span></span>

<span data-ttu-id="ace1b-119">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ace1b-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ace1b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ace1b-120">Requirements</span></span>



| <span data-ttu-id="ace1b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ace1b-121">Requirement</span></span> | <span data-ttu-id="ace1b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ace1b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ace1b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ace1b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ace1b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ace1b-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ace1b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ace1b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ace1b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ace1b-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ace1b-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ace1b-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ace1b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace1b-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ace1b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ace1b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace1b-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace1b-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ace1b-131">IID</span><span class="sxs-lookup"><span data-stu-id="ace1b-131">IID</span></span><br/>                      | <span data-ttu-id="ace1b-132">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="ace1b-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ace1b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ace1b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace1b-134">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="ace1b-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





