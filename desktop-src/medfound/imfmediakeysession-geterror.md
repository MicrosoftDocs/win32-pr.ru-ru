---
description: Возвращает состояние ошибки, связанное с сеансом ключа мультимедиа.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: 'Метод Имфмедиакэйсессион:: Error'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4f0a42601698a9cd62dc6cb23ca9e69ac2cc8a49
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720053"
---
# <a name="imfmediakeysessiongeterror-method"></a><span data-ttu-id="15b84-103">Метод Имфмедиакэйсессион:: Error</span><span class="sxs-lookup"><span data-stu-id="15b84-103">IMFMediaKeySession::GetError method</span></span>

<span data-ttu-id="15b84-104">Возвращает состояние ошибки, связанное с сеансом ключа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="15b84-104">Gets the error state associated with the media key session.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b84-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15b84-105">Syntax</span></span>


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a><span data-ttu-id="15b84-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15b84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15b84-107">*code*</span><span class="sxs-lookup"><span data-stu-id="15b84-107">*code*</span></span> 
</dt> <dd>

<span data-ttu-id="15b84-108">Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="15b84-108">The error code.</span></span>

</dd> <dt>

<span data-ttu-id="15b84-109">*системкоде*</span><span class="sxs-lookup"><span data-stu-id="15b84-109">*systemCode*</span></span> 
</dt> <dd>

<span data-ttu-id="15b84-110">Сведения об ошибках, специфичных для платформы.</span><span class="sxs-lookup"><span data-stu-id="15b84-110">Platform specific error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15b84-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15b84-111">Return value</span></span>

<span data-ttu-id="15b84-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="15b84-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15b84-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15b84-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="15b84-114">Требования</span><span class="sxs-lookup"><span data-stu-id="15b84-114">Requirements</span></span>



| <span data-ttu-id="15b84-115">Требование</span><span class="sxs-lookup"><span data-stu-id="15b84-115">Requirement</span></span> | <span data-ttu-id="15b84-116">Значение</span><span class="sxs-lookup"><span data-stu-id="15b84-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b84-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15b84-117">Minimum supported client</span></span><br/> | <span data-ttu-id="15b84-118">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15b84-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="15b84-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15b84-119">Minimum supported server</span></span><br/> | <span data-ttu-id="15b84-120">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="15b84-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="15b84-121">IDL</span><span class="sxs-lookup"><span data-stu-id="15b84-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15b84-122"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15b84-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15b84-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15b84-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b84-124">**имфмедиакэйсессион**</span><span class="sxs-lookup"><span data-stu-id="15b84-124">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




