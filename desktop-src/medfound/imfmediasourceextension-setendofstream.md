---
description: Указывает, что достигнут конец потока мультимедиа.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: 'Метод Имфмедиасаурцеекстенсион:: Сетендофстреам'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713279"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a><span data-ttu-id="d551b-103">Метод Имфмедиасаурцеекстенсион:: Сетендофстреам</span><span class="sxs-lookup"><span data-stu-id="d551b-103">IMFMediaSourceExtension::SetEndOfStream method</span></span>

<span data-ttu-id="d551b-104">Указывает, что достигнут конец потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d551b-104">Indicate that the end of the media stream has been reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="d551b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d551b-105">Syntax</span></span>


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a><span data-ttu-id="d551b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d551b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d551b-107">*Ошибка при* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d551b-107">*error* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d551b-108">Используется для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d551b-108">Used to pass error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d551b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d551b-109">Return value</span></span>

<span data-ttu-id="d551b-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d551b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d551b-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d551b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d551b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d551b-112">Requirements</span></span>



| <span data-ttu-id="d551b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d551b-113">Requirement</span></span> | <span data-ttu-id="d551b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d551b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d551b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d551b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d551b-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d551b-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d551b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d551b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d551b-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d551b-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d551b-119">IDL</span><span class="sxs-lookup"><span data-stu-id="d551b-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d551b-120"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d551b-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d551b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d551b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d551b-122">**имфмедиасаурцеекстенсион**</span><span class="sxs-lookup"><span data-stu-id="d551b-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[<span data-ttu-id="d551b-123">**MF \_ , \_ Ошибка MSE**</span><span class="sxs-lookup"><span data-stu-id="d551b-123">**MF\_MSE\_ERROR**</span></span>](mf-mse-error.md)
</dt> </dl>

 

 




