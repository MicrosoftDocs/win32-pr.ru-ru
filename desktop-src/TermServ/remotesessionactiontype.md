---
title: Перечисление Ремотесессионактионтипе
description: Используется для указания типа удаленного действия.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов перечисления Ремотесессионактионтипе
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681828"
---
# <a name="remotesessionactiontype-enumeration"></a><span data-ttu-id="1d6c7-104">Перечисление Ремотесессионактионтипе</span><span class="sxs-lookup"><span data-stu-id="1d6c7-104">RemoteSessionActionType enumeration</span></span>

<span data-ttu-id="1d6c7-105">Используется для указания типа удаленного действия.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-105">Used to specify the type of remote action.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d6c7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d6c7-106">Syntax</span></span>


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a><span data-ttu-id="1d6c7-107">Константы</span><span class="sxs-lookup"><span data-stu-id="1d6c7-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1d6c7-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**ремотесессионактиончармс**</span><span class="sxs-lookup"><span data-stu-id="1d6c7-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span></span>
</dt> <dd>

<span data-ttu-id="1d6c7-109">Отображает чудо в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-109">Displays the charms in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="1d6c7-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**ремотесессионактионаппбар**</span><span class="sxs-lookup"><span data-stu-id="1d6c7-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span></span>
</dt> <dd>

<span data-ttu-id="1d6c7-111">Отображает панель приложений в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-111">Displays the app bar in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="1d6c7-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**ремотесессионактионснап**</span><span class="sxs-lookup"><span data-stu-id="1d6c7-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span></span>
</dt> <dd>

<span data-ttu-id="1d6c7-113">Закрепляет приложение в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-113">Docks the application in the remote session.</span></span> <span data-ttu-id="1d6c7-114">Этот параметр является устаревшим и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-114">This option has been deprecated and should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="1d6c7-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**ремотесессионактионстартскрин**</span><span class="sxs-lookup"><span data-stu-id="1d6c7-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span></span>
</dt> <dd>

<span data-ttu-id="1d6c7-116">Приводит к отображению начального экрана в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-116">Causes the start screen to be displayed in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="1d6c7-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**ремотесессионактионаппсвитч**</span><span class="sxs-lookup"><span data-stu-id="1d6c7-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span></span>
</dt> <dd>

<span data-ttu-id="1d6c7-118">Вызывает отображение окна переключения приложения в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-118">Causes the application switch window to be displayed in the remote session.</span></span> <span data-ttu-id="1d6c7-119">Это то же самое, что пользователь нажимает клавиши ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-119">This is the same as the user pressing Alt+Tab.</span></span>

</dd> <dt>

<span data-ttu-id="1d6c7-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**ремотесессионактионактионцентер**</span><span class="sxs-lookup"><span data-stu-id="1d6c7-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span></span>
</dt> <dd>

<span data-ttu-id="1d6c7-121">Приводит к отображению центра уведомлений в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-121">Causes the Action Center to be displayed in the remote session.</span></span> <span data-ttu-id="1d6c7-122">То же самое, что пользователь нажимает клавишу Win + A.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-122">This is the same as the user pressing Win+A.</span></span>

<span data-ttu-id="1d6c7-123">**Windows server 2012 R2, Windows 8.1, Windows Server 2012 и Windows 8:** Это значение не поддерживается до Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1d6c7-123">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:** This value is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d6c7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1d6c7-124">Requirements</span></span>



| <span data-ttu-id="1d6c7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1d6c7-125">Requirement</span></span> | <span data-ttu-id="1d6c7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1d6c7-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6c7-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d6c7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1d6c7-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1d6c7-128">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="1d6c7-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d6c7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1d6c7-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d6c7-130">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="1d6c7-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1d6c7-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d6c7-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d6c7-132"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d6c7-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d6c7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6c7-134">**IMsRdpClient8:: Сендремотеактион**</span><span class="sxs-lookup"><span data-stu-id="1d6c7-134">**IMsRdpClient8::SendRemoteAction**</span></span>](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





