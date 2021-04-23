---
description: Удаляет все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: 'Исканпрофилемгр: метод:D Елетеаллпрофилесфорусер (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c5d723379bb542346e3612f70c19a1629d325ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154870"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a><span data-ttu-id="2f591-103">Исканпрофилемгр: метод:D Елетеаллпрофилесфорусер</span><span class="sxs-lookup"><span data-stu-id="2f591-103">IScanProfileMgr::DeleteAllProfilesForUser method</span></span>

<span data-ttu-id="2f591-104">Удаляет все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="2f591-104">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f591-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f591-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a><span data-ttu-id="2f591-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f591-106">Parameters</span></span>

<span data-ttu-id="2f591-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2f591-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f591-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f591-108">Return value</span></span>

<span data-ttu-id="2f591-109">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2f591-109">Type: **HRESULT**</span></span>

<span data-ttu-id="2f591-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2f591-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f591-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f591-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f591-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2f591-112">Requirements</span></span>



| <span data-ttu-id="2f591-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2f591-113">Requirement</span></span> | <span data-ttu-id="2f591-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2f591-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f591-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f591-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2f591-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f591-116">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2f591-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f591-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2f591-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f591-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f591-119">Header</span><span class="sxs-lookup"><span data-stu-id="2f591-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f591-120"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f591-120"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="2f591-121">IDL</span><span class="sxs-lookup"><span data-stu-id="2f591-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f591-122"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f591-122"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f591-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f591-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f591-124">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="2f591-124">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="2f591-125">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="2f591-125">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




