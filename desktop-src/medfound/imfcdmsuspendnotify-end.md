---
description: Будет выполнена фактическая приостановка, и в модуль расшифровки содержимого (CDM) больше не будут выполняться никакие вызовы.
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: 'Метод Имфкдмсуспенднотифи:: end'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711789"
---
# <a name="imfcdmsuspendnotifyend-method"></a><span data-ttu-id="1eeb6-103">Метод Имфкдмсуспенднотифи:: end</span><span class="sxs-lookup"><span data-stu-id="1eeb6-103">IMFCdmSuspendNotify::End method</span></span>

<span data-ttu-id="1eeb6-104">Будет выполнена фактическая приостановка, и в модуль расшифровки содержимого (CDM) больше не будут выполняться никакие вызовы.</span><span class="sxs-lookup"><span data-stu-id="1eeb6-104">The actual suspend is about to occur and no more calls will be made into the Content Decryption Module (CDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="1eeb6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1eeb6-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="1eeb6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eeb6-106">Parameters</span></span>

<span data-ttu-id="1eeb6-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1eeb6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1eeb6-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1eeb6-108">Return value</span></span>

<span data-ttu-id="1eeb6-109">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1eeb6-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1eeb6-110">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1eeb6-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eeb6-111">Требования</span><span class="sxs-lookup"><span data-stu-id="1eeb6-111">Requirements</span></span>



| <span data-ttu-id="1eeb6-112">Требование</span><span class="sxs-lookup"><span data-stu-id="1eeb6-112">Requirement</span></span> | <span data-ttu-id="1eeb6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="1eeb6-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eeb6-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1eeb6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1eeb6-115">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1eeb6-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1eeb6-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1eeb6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1eeb6-117">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1eeb6-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1eeb6-118">IDL</span><span class="sxs-lookup"><span data-stu-id="1eeb6-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1eeb6-119"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb6-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eeb6-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1eeb6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eeb6-121">**имфкдмсуспенднотифи**</span><span class="sxs-lookup"><span data-stu-id="1eeb6-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




