---
description: Вызывается при переключении удостоверений пользователя.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'Метод Иидентитичанженотифи:: Свитчидентитиес (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997666"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a><span data-ttu-id="1936f-103">Метод Иидентитичанженотифи:: Свитчидентитиес</span><span class="sxs-lookup"><span data-stu-id="1936f-103">IIdentityChangeNotify::SwitchIdentities method</span></span>

<span data-ttu-id="1936f-104">\[**Свитчидентитиес** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="1936f-104">\[**SwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1936f-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="1936f-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="1936f-106">Вызывается при переключении удостоверений пользователя.</span><span class="sxs-lookup"><span data-stu-id="1936f-106">Called when user identities are switched.</span></span>

## <a name="syntax"></a><span data-ttu-id="1936f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1936f-107">Syntax</span></span>


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="1936f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1936f-108">Parameters</span></span>

<span data-ttu-id="1936f-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1936f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1936f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1936f-110">Return value</span></span>

<span data-ttu-id="1936f-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1936f-111">Type: **HRESULT**</span></span>

<span data-ttu-id="1936f-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1936f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1936f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1936f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1936f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1936f-114">Remarks</span></span>

<span data-ttu-id="1936f-115">Этот метод можно реализовать, чтобы обеспечить пользовательское поведение приложения, когда пользователь успешно переключил удостоверения.</span><span class="sxs-lookup"><span data-stu-id="1936f-115">You may implement this method to provide custom behavior for your application when a user has successfully switched identities.</span></span> <span data-ttu-id="1936f-116">Чтобы обеспечить пользовательское поведение перед переключением удостоверения пользователя, реализуйте метод [**иидентитичанженотифи:: куерисвитчидентитиес**](iidentitychangenotify-queryswitchidentities.md) .</span><span class="sxs-lookup"><span data-stu-id="1936f-116">To provide custom behavior before a user identity switch occurs, implement the [**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1936f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1936f-117">Requirements</span></span>



| <span data-ttu-id="1936f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1936f-118">Requirement</span></span> | <span data-ttu-id="1936f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1936f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1936f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1936f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1936f-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1936f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1936f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1936f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1936f-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1936f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1936f-124">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1936f-124">End of client support</span></span><br/>    | <span data-ttu-id="1936f-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1936f-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="1936f-126">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1936f-126">End of server support</span></span><br/>    | <span data-ttu-id="1936f-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1936f-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="1936f-128">Header</span><span class="sxs-lookup"><span data-stu-id="1936f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1936f-129"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="1936f-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="1936f-130">IDL</span><span class="sxs-lookup"><span data-stu-id="1936f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1936f-131"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1936f-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="1936f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1936f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1936f-133"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1936f-133"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1936f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1936f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1936f-135">**иидентитичанженотифи**</span><span class="sxs-lookup"><span data-stu-id="1936f-135">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="1936f-136">**Иидентитичанженотифи:: Куерисвитчидентитиес**</span><span class="sxs-lookup"><span data-stu-id="1936f-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




