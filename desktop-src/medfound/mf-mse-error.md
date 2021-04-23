---
description: Определяет различные состояния ошибок расширения источника мультимедиа.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: Перечисление MF_MSE_ERROR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155563"
---
# <a name="mf_mse_error-enumeration"></a><span data-ttu-id="f3e26-103">\_ \_ Перечисление ошибок MF MSE</span><span class="sxs-lookup"><span data-stu-id="f3e26-103">MF\_MSE\_ERROR enumeration</span></span>

<span data-ttu-id="f3e26-104">Определяет различные состояния ошибок расширения источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f3e26-104">Defines the different error states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e26-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3e26-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a><span data-ttu-id="f3e26-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f3e26-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f3e26-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF \_ MSE \_ ошибка ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="f3e26-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF\_MSE\_ERROR\_NOERROR**</span></span>
</dt> <dd>

<span data-ttu-id="f3e26-108">Не указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="f3e26-108">Specifies no error.</span></span>

</dd> <dt>

<span data-ttu-id="f3e26-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**\_ \_ Сетевая ошибка MF MSE \_**</span><span class="sxs-lookup"><span data-stu-id="f3e26-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF\_MSE\_ERROR\_NETWORK**</span></span>
</dt> <dd>

<span data-ttu-id="f3e26-110">Указывает ошибку в сети.</span><span class="sxs-lookup"><span data-stu-id="f3e26-110">Specifies an error with the network.</span></span>

</dd> <dt>

<span data-ttu-id="f3e26-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_ \_ расшифровка ошибок MF в MSE \_**</span><span class="sxs-lookup"><span data-stu-id="f3e26-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**MF\_MSE\_ERROR\_DECODE**</span></span>
</dt> <dd>

<span data-ttu-id="f3e26-112">Указывает ошибку при декодировании.</span><span class="sxs-lookup"><span data-stu-id="f3e26-112">Specifies an error with decoding.</span></span>

</dd> <dt>

<span data-ttu-id="f3e26-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF \_ MSE \_ Ошибка \_ неизвестная \_ Ошибка**</span><span class="sxs-lookup"><span data-stu-id="f3e26-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF\_MSE\_ERROR\_UNKNOWN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="f3e26-114">Указывает неизвестную ошибку.</span><span class="sxs-lookup"><span data-stu-id="f3e26-114">Specifies an unknown error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3e26-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f3e26-115">Requirements</span></span>



| <span data-ttu-id="f3e26-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f3e26-116">Requirement</span></span> | <span data-ttu-id="f3e26-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f3e26-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e26-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3e26-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e26-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f3e26-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f3e26-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3e26-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e26-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3e26-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f3e26-122">IDL</span><span class="sxs-lookup"><span data-stu-id="f3e26-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3e26-123"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3e26-123"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3e26-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3e26-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e26-125">Перечисления Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3e26-125">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




