---
description: Вызывается, когда текущий пользователь запросил переключить удостоверение пользователя, но перед тем, как произойдет переключение.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'Метод Иидентитичанженотифи:: Куерисвитчидентитиес (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909519"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a><span data-ttu-id="b33b3-103">Метод Иидентитичанженотифи:: Куерисвитчидентитиес</span><span class="sxs-lookup"><span data-stu-id="b33b3-103">IIdentityChangeNotify::QuerySwitchIdentities method</span></span>

<span data-ttu-id="b33b3-104">\[**Куерисвитчидентитиес** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b33b3-104">\[**QuerySwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b33b3-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="b33b3-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="b33b3-106">Вызывается, когда текущий пользователь запросил переключить удостоверение пользователя, но перед тем, как произойдет переключение.</span><span class="sxs-lookup"><span data-stu-id="b33b3-106">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b33b3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b33b3-107">Syntax</span></span>


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="b33b3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b33b3-108">Parameters</span></span>

<span data-ttu-id="b33b3-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b33b3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b33b3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b33b3-110">Return value</span></span>

<span data-ttu-id="b33b3-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b33b3-111">Type: **HRESULT**</span></span>

<span data-ttu-id="b33b3-112">Результат запроса Switch.</span><span class="sxs-lookup"><span data-stu-id="b33b3-112">Result of the switch query.</span></span> <span data-ttu-id="b33b3-113">Если параметр должен продолжать работу, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b33b3-113">If the switch should proceed, return S\_OK.</span></span> <span data-ttu-id="b33b3-114">В противном случае возвращается \_ параметр E Process отмена процесса, \_ \_ чтобы указать, что параметр удостоверения пользователя следует прерывать.</span><span class="sxs-lookup"><span data-stu-id="b33b3-114">Otherwise, return E\_PROCESS\_CANCELLED\_SWITCH to indicate that the user identity switch should be aborted.</span></span>

## <a name="remarks"></a><span data-ttu-id="b33b3-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b33b3-115">Remarks</span></span>

<span data-ttu-id="b33b3-116">Этот метод можно реализовать, чтобы обеспечить пользовательское поведение приложения, когда пользователь запрашивает переключение этих удостоверений.</span><span class="sxs-lookup"><span data-stu-id="b33b3-116">You may implement this method to provide custom behavior for your application when a user requests that identities be switched.</span></span> <span data-ttu-id="b33b3-117">Вы можете остановить ожидающее переключение удостоверения, вернувшись в значение \_ \_ параметра отмены процесса отменено \_ .</span><span class="sxs-lookup"><span data-stu-id="b33b3-117">You can stop the pending identity switch by returning the value E\_PROCESS\_CANCELLED\_SWITCH.</span></span>

## <a name="requirements"></a><span data-ttu-id="b33b3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b33b3-118">Requirements</span></span>



| <span data-ttu-id="b33b3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b33b3-119">Requirement</span></span> | <span data-ttu-id="b33b3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b33b3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b33b3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b33b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b33b3-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b33b3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b33b3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b33b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b33b3-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b33b3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b33b3-125">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b33b3-125">End of client support</span></span><br/>    | <span data-ttu-id="b33b3-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b33b3-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b33b3-127">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b33b3-127">End of server support</span></span><br/>    | <span data-ttu-id="b33b3-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b33b3-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b33b3-129">Header</span><span class="sxs-lookup"><span data-stu-id="b33b3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b33b3-130"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b33b3-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="b33b3-131">IDL</span><span class="sxs-lookup"><span data-stu-id="b33b3-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b33b3-132"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b33b3-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="b33b3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b33b3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b33b3-134"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b33b3-134"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b33b3-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b33b3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b33b3-136">**иидентитичанженотифи**</span><span class="sxs-lookup"><span data-stu-id="b33b3-136">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="b33b3-137">**Иидентитичанженотифи:: Свитчидентитиес**</span><span class="sxs-lookup"><span data-stu-id="b33b3-137">**IIdentityChangeNotify::SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




