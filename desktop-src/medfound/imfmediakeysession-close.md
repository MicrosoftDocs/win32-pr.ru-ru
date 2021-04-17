---
description: Закрывает сеанс ключа мультимедиа и должен вызываться перед освобождением сеанса ключа.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'Метод Имфмедиакэйсессион:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684742"
---
# <a name="imfmediakeysessionclose-method"></a><span data-ttu-id="dd93f-103">Метод Имфмедиакэйсессион:: Close</span><span class="sxs-lookup"><span data-stu-id="dd93f-103">IMFMediaKeySession::Close method</span></span>

<span data-ttu-id="dd93f-104">Закрывает сеанс ключа мультимедиа и должен вызываться перед освобождением сеанса ключа.</span><span class="sxs-lookup"><span data-stu-id="dd93f-104">Closes the media key session and must be called before the key session is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd93f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd93f-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="dd93f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd93f-106">Parameters</span></span>

<span data-ttu-id="dd93f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="dd93f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd93f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd93f-108">Return value</span></span>

<span data-ttu-id="dd93f-109">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="dd93f-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd93f-110">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd93f-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd93f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="dd93f-111">Requirements</span></span>



| <span data-ttu-id="dd93f-112">Требование</span><span class="sxs-lookup"><span data-stu-id="dd93f-112">Requirement</span></span> | <span data-ttu-id="dd93f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="dd93f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd93f-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd93f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dd93f-115">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd93f-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dd93f-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd93f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dd93f-117">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd93f-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dd93f-118">IDL</span><span class="sxs-lookup"><span data-stu-id="dd93f-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd93f-119"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd93f-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd93f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd93f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd93f-121">**имфмедиакэйсессион**</span><span class="sxs-lookup"><span data-stu-id="dd93f-121">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




