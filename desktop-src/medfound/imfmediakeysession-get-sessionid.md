---
description: Возвращает уникальный идентификатор сеанса, созданный для данного сеанса.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: 'Метод Имфмедиакэйсессион:: get_SessionId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7110dbe6c24d1189019fb242621c7e3c01253264
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664805"
---
# <a name="imfmediakeysessionget_sessionid-method"></a><span data-ttu-id="e3900-103">Метод Имфмедиакэйсессион:: Get \_ SessionID</span><span class="sxs-lookup"><span data-stu-id="e3900-103">IMFMediaKeySession::get\_SessionId method</span></span>

<span data-ttu-id="e3900-104">Возвращает уникальный идентификатор сеанса, созданный для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="e3900-104">Gets a unique session id created for this session.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3900-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3900-105">Syntax</span></span>


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a><span data-ttu-id="e3900-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3900-107">*sessionID*</span><span class="sxs-lookup"><span data-stu-id="e3900-107">*sessionId*</span></span> 
</dt> <dd>

<span data-ttu-id="e3900-108">Идентификатор сеанса ключа носителя.</span><span class="sxs-lookup"><span data-stu-id="e3900-108">The media key session id.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3900-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3900-109">Return value</span></span>

<span data-ttu-id="e3900-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e3900-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3900-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3900-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3900-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e3900-112">Requirements</span></span>



| <span data-ttu-id="e3900-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e3900-113">Requirement</span></span> | <span data-ttu-id="e3900-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e3900-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3900-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3900-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e3900-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3900-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e3900-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3900-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e3900-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3900-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e3900-119">IDL</span><span class="sxs-lookup"><span data-stu-id="e3900-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3900-120"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3900-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3900-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3900-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3900-122">**имфмедиакэйсессион**</span><span class="sxs-lookup"><span data-stu-id="e3900-122">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




