---
description: Повторно перечисляет все профили сканирования в системе.
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: 'Метод Исканпрофилемгр:: Refresh (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e4af44e95889abf35fe13e1669411513458a16c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991274"
---
# <a name="iscanprofilemgrrefresh-method"></a><span data-ttu-id="45ec8-103">Метод Исканпрофилемгр:: Refresh</span><span class="sxs-lookup"><span data-stu-id="45ec8-103">IScanProfileMgr::Refresh method</span></span>

<span data-ttu-id="45ec8-104">Повторно перечисляет все профили сканирования в системе.</span><span class="sxs-lookup"><span data-stu-id="45ec8-104">Re-enumerates all the scan profiles in the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ec8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45ec8-105">Syntax</span></span>


```C++
HRESULT Refresh();
```



## <a name="parameters"></a><span data-ttu-id="45ec8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="45ec8-106">Parameters</span></span>

<span data-ttu-id="45ec8-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="45ec8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45ec8-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45ec8-108">Return value</span></span>

<span data-ttu-id="45ec8-109">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="45ec8-109">Type: **HRESULT**</span></span>

<span data-ttu-id="45ec8-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="45ec8-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45ec8-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="45ec8-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45ec8-112">Remarks</span></span>

<span data-ttu-id="45ec8-113">Используйте этот метод, если несколько объектов [**исканпрофилемгр**](-wia-iscanprofilemgr.md) могут создавать или удалять профили одновременно.</span><span class="sxs-lookup"><span data-stu-id="45ec8-113">Use this method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="45ec8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="45ec8-114">Requirements</span></span>



| <span data-ttu-id="45ec8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="45ec8-115">Requirement</span></span> | <span data-ttu-id="45ec8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="45ec8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ec8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45ec8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="45ec8-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45ec8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="45ec8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45ec8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="45ec8-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45ec8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45ec8-121">Header</span><span class="sxs-lookup"><span data-stu-id="45ec8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="45ec8-122"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="45ec8-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="45ec8-123">IDL</span><span class="sxs-lookup"><span data-stu-id="45ec8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45ec8-124"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45ec8-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45ec8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45ec8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ec8-126">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="45ec8-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="45ec8-127">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="45ec8-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




