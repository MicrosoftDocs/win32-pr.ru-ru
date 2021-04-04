---
title: Имстскаксевентс Онремотепрограмдисплайед, метод
description: Вызывается при отображении программы RemoteApp.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онремотепрограмдисплайед
- Службы удаленных рабочих столов метода Онремотепрограмдисплайед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онремотепрограмдисплайед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802734"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a><span data-ttu-id="74958-106">Метод Имстскаксевентс:: Онремотепрограмдисплайед</span><span class="sxs-lookup"><span data-stu-id="74958-106">IMsTscAxEvents::OnRemoteProgramDisplayed method</span></span>

<span data-ttu-id="74958-107">Вызывается при отображении программы RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="74958-107">Called when a RemoteApp program is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="74958-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74958-108">Syntax</span></span>


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a><span data-ttu-id="74958-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="74958-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74958-110">*вбдисплайед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74958-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74958-111">Указывает, отображается ли приложение RemoteApp или скрыто.</span><span class="sxs-lookup"><span data-stu-id="74958-111">Indicates whether the RemoteApp program is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="74958-112">*удисплайинформатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74958-112">*uDisplayInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74958-113">Отображаемые сведения.</span><span class="sxs-lookup"><span data-stu-id="74958-113">The display information.</span></span>

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span data-ttu-id="74958-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**Шина \_ аппдисплай \_ аутореконнект**</span><span class="sxs-lookup"><span data-stu-id="74958-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL\_APPDISPLAY\_AUTORECONNECT**</span></span>


</dt> <dd>

<span data-ttu-id="74958-115">Выполняется автоматическое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="74958-115">Automatic reconnect is in progress.</span></span>

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span data-ttu-id="74958-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**Шина \_ аппдисплай \_ десктофукед**</span><span class="sxs-lookup"><span data-stu-id="74958-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL\_APPDISPLAY\_DESKTOPHOOKED**</span></span>


</dt> <dd>

<span data-ttu-id="74958-117">Число RemoteApp было просто обнулено.</span><span class="sxs-lookup"><span data-stu-id="74958-117">The RemoteApp count just went to zero.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74958-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74958-118">Return value</span></span>

<span data-ttu-id="74958-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="74958-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74958-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74958-120">Remarks</span></span>

<span data-ttu-id="74958-121">Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что приложение RemoteApp отображается.</span><span class="sxs-lookup"><span data-stu-id="74958-121">Implement this method in your event sink to receive notification that a RemoteApp has been displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="74958-122">Требования</span><span class="sxs-lookup"><span data-stu-id="74958-122">Requirements</span></span>



| <span data-ttu-id="74958-123">Требование</span><span class="sxs-lookup"><span data-stu-id="74958-123">Requirement</span></span> | <span data-ttu-id="74958-124">Значение</span><span class="sxs-lookup"><span data-stu-id="74958-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74958-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74958-125">Minimum supported client</span></span><br/> | <span data-ttu-id="74958-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74958-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="74958-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74958-127">Minimum supported server</span></span><br/> | <span data-ttu-id="74958-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74958-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="74958-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="74958-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="74958-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74958-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="74958-131">DLL</span><span class="sxs-lookup"><span data-stu-id="74958-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74958-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74958-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="74958-133">IID</span><span class="sxs-lookup"><span data-stu-id="74958-133">IID</span></span><br/>                      | <span data-ttu-id="74958-134">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="74958-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



 

 





