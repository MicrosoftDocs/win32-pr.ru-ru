---
description: Прерывает обработку текущего сегмента мультимедиа.
ms.assetid: 31253d0d-c53f-47bd-823a-fc564cb63b78
title: 'Метод Имфсаурцебуффер:: Abort'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Abort
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 3a8b5115032fb918af66094bb87c7118eb503da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543599"
---
# <a name="imfsourcebufferabort-method"></a><span data-ttu-id="3dc25-103">Метод Имфсаурцебуффер:: Abort</span><span class="sxs-lookup"><span data-stu-id="3dc25-103">IMFSourceBuffer::Abort method</span></span>

<span data-ttu-id="3dc25-104">Прерывает обработку текущего сегмента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3dc25-104">Aborts the processing of the current media segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc25-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dc25-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="3dc25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3dc25-106">Parameters</span></span>

<span data-ttu-id="3dc25-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3dc25-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3dc25-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3dc25-108">Return value</span></span>

<span data-ttu-id="3dc25-109">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3dc25-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3dc25-110">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3dc25-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc25-111">Требования</span><span class="sxs-lookup"><span data-stu-id="3dc25-111">Requirements</span></span>



| <span data-ttu-id="3dc25-112">Требование</span><span class="sxs-lookup"><span data-stu-id="3dc25-112">Requirement</span></span> | <span data-ttu-id="3dc25-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3dc25-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc25-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dc25-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc25-115">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3dc25-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3dc25-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dc25-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc25-117">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3dc25-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3dc25-118">IDL</span><span class="sxs-lookup"><span data-stu-id="3dc25-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3dc25-119"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3dc25-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dc25-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dc25-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc25-121">**имфсаурцебуффер**</span><span class="sxs-lookup"><span data-stu-id="3dc25-121">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




