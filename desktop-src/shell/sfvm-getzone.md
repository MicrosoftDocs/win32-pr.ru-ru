---
description: 'Позволяет объекту обратного вызова предоставлять сведения о зоне Интернета. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Сообщение SFVM_GETZONE (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546935"
---
# <a name="sfvm_getzone-message"></a><span data-ttu-id="c6b68-104">Сообщение СФВМ в \_ зоне</span><span class="sxs-lookup"><span data-stu-id="c6b68-104">SFVM\_GETZONE message</span></span>

<span data-ttu-id="c6b68-105">\[Это уведомление поддерживается в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c6b68-105">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="c6b68-106">В последующих версиях Windows она может не поддерживаться.\]</span><span class="sxs-lookup"><span data-stu-id="c6b68-106">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c6b68-107">Позволяет объекту обратного вызова предоставлять сведения о зоне Интернета.</span><span class="sxs-lookup"><span data-stu-id="c6b68-107">Allows the callback object to provide Internet zone information.</span></span> <span data-ttu-id="c6b68-108">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="c6b68-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a><span data-ttu-id="c6b68-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6b68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6b68-110">*зона* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c6b68-110">*zone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6b68-111">Одно из следующих значений, указывающее зону Интернета.</span><span class="sxs-lookup"><span data-stu-id="c6b68-111">One of the following values indicating the Internet zone.</span></span> <span data-ttu-id="c6b68-112">Эти значения составляют перечисление [**урлзоне**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , определенное в Urlmon. h.</span><span class="sxs-lookup"><span data-stu-id="c6b68-112">These values constitute the [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) enumeration, defined in Urlmon.h.</span></span>

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span data-ttu-id="c6b68-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**УРЛЗОНЕ \_ локальный \_ компьютер**</span><span class="sxs-lookup"><span data-stu-id="c6b68-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**URLZONE\_LOCAL\_MACHINE**</span></span>


</dt> <dd>

<span data-ttu-id="c6b68-114">Зона, используемая для содержимого, уже расположенного на локальном компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6b68-114">Zone used for content already on the user's local computer.</span></span> <span data-ttu-id="c6b68-115">Эта зона не предоставляется пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="c6b68-115">This zone is not exposed by the user interface.</span></span>

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span data-ttu-id="c6b68-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**\_интрасеть урлзоне**</span><span class="sxs-lookup"><span data-stu-id="c6b68-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**URLZONE\_INTRANET**</span></span>


</dt> <dd>

<span data-ttu-id="c6b68-117">Зона, используемая для содержимого, обнаруженного в интрасети.</span><span class="sxs-lookup"><span data-stu-id="c6b68-117">Zone used for content found on an intranet.</span></span>

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span data-ttu-id="c6b68-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**УРЛЗОНЕ \_ доверенный**</span><span class="sxs-lookup"><span data-stu-id="c6b68-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE\_TRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="c6b68-119">Зона, используемая для доверенных веб-сайтов в Интернете.</span><span class="sxs-lookup"><span data-stu-id="c6b68-119">Zone used for trusted websites on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span data-ttu-id="c6b68-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**УРЛЗОНЕ \_ Интернет**</span><span class="sxs-lookup"><span data-stu-id="c6b68-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE\_INTERNET**</span></span>


</dt> <dd>

<span data-ttu-id="c6b68-121">Зона, используемая для большей части содержимого в Интернете.</span><span class="sxs-lookup"><span data-stu-id="c6b68-121">Zone used for most of the content on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span data-ttu-id="c6b68-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**УРЛЗОНЕ \_ без доверия**</span><span class="sxs-lookup"><span data-stu-id="c6b68-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE\_UNTRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="c6b68-123">Зона, используемая для веб-сайтов, которые не являются доверенными.</span><span class="sxs-lookup"><span data-stu-id="c6b68-123">Zone used for websites that are not trusted.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6b68-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c6b68-124">Requirements</span></span>



| <span data-ttu-id="c6b68-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c6b68-125">Requirement</span></span> | <span data-ttu-id="c6b68-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c6b68-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b68-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6b68-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b68-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c6b68-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c6b68-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6b68-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b68-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c6b68-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c6b68-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c6b68-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b68-132"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b68-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
