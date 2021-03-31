---
description: Указывает, что процесс приостановки запущен, а ресурсы должны быть переведены в целостное состояние.
ms.assetid: 5cf3d249-3d8b-4596-9d8b-e7b95a270eff
title: 'Метод Имфкдмсуспенднотифи:: Begin'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.Begin
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 84453a6c846e88a9d6e6c32c5253d97d36e89c7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808398"
---
# <a name="imfcdmsuspendnotifybegin-method"></a><span data-ttu-id="6b47a-103">Метод Имфкдмсуспенднотифи:: Begin</span><span class="sxs-lookup"><span data-stu-id="6b47a-103">IMFCdmSuspendNotify::Begin method</span></span>

<span data-ttu-id="6b47a-104">Указывает, что процесс приостановки запущен, а ресурсы должны быть переведены в целостное состояние.</span><span class="sxs-lookup"><span data-stu-id="6b47a-104">Indicates that the suspend process is starting and resources should be brought into a consistent state.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b47a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b47a-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="6b47a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b47a-106">Parameters</span></span>

<span data-ttu-id="6b47a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6b47a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b47a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b47a-108">Return value</span></span>

<span data-ttu-id="6b47a-109">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6b47a-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6b47a-110">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b47a-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b47a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6b47a-111">Requirements</span></span>



| <span data-ttu-id="6b47a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6b47a-112">Requirement</span></span> | <span data-ttu-id="6b47a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6b47a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b47a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b47a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6b47a-115">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b47a-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6b47a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b47a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6b47a-117">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b47a-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6b47a-118">IDL</span><span class="sxs-lookup"><span data-stu-id="6b47a-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b47a-119"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b47a-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b47a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b47a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b47a-121">**имфкдмсуспенднотифи**</span><span class="sxs-lookup"><span data-stu-id="6b47a-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




