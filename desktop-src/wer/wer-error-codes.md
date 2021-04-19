---
title: Коды ошибок WER (Верапи. h)
description: В следующей таблице приведен список настраиваемых кодов ошибок, используемых отчеты об ошибках Windows.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691816"
---
# <a name="wer-error-codes"></a><span data-ttu-id="8f3eb-103">Коды ошибок WER</span><span class="sxs-lookup"><span data-stu-id="8f3eb-103">WER Error Codes</span></span>

<span data-ttu-id="8f3eb-104">В следующей таблице приведен список настраиваемых кодов ошибок, используемых отчеты об ошибках Windows.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-104">The following table provides a list of custom error codes used by Windows Error Reporting.</span></span>



| <span data-ttu-id="8f3eb-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8f3eb-105">Constant</span></span>                                                                                                                                                                                            | <span data-ttu-id="8f3eb-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8f3eb-106">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <span data-ttu-id="8f3eb-107"><dt>**\_ \_ недостаточный \_ Размер буфера WER**</dt></span><span class="sxs-lookup"><span data-stu-id="8f3eb-107"><dt>**WER\_E\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="8f3eb-108">Буфер слишком мал для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-108">A buffer is too small to contain the data.</span></span><br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <span data-ttu-id="8f3eb-109"><dt>**\_ \_ недействительное \_ состояние WER E**</dt></span><span class="sxs-lookup"><span data-stu-id="8f3eb-109"><dt>**WER\_E\_INVALID\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="8f3eb-110">Функция была вызвана неподдерживаемым способом.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-110">A function was called in an unsupported manner.</span></span><br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <span data-ttu-id="8f3eb-111"><dt>**\_ \_ превышена длина WER по E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f3eb-111"><dt>**WER\_E\_LENGTH\_EXCEEDED**</dt></span></span> </dl>             | <span data-ttu-id="8f3eb-112">Был превышен один из ограничений длины.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-112">One of the length limits has been exceeded.</span></span><br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <span data-ttu-id="8f3eb-113"><dt>**WER \_ E \_ Missing \_ param**</dt></span><span class="sxs-lookup"><span data-stu-id="8f3eb-113"><dt>**WER\_E\_MISSING\_PARAM**</dt></span></span> </dl>                   | <span data-ttu-id="8f3eb-114">Отсутствует один или несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-114">One or more parameters are missing.</span></span><br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <span data-ttu-id="8f3eb-115"><dt>**WER \_ E \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="8f3eb-115"><dt>**WER\_E\_NOT\_FOUND**</dt></span></span> </dl>                               | <span data-ttu-id="8f3eb-116">Элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-116">Element not found.</span></span><br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <span data-ttu-id="8f3eb-117"><dt>**\_электронное \_ хранилище WER \_ отключено**</dt></span><span class="sxs-lookup"><span data-stu-id="8f3eb-117"><dt>**WER\_E\_STORE\_DISABLED**</dt></span></span> </dl>                | <span data-ttu-id="8f3eb-118">Хранилище отключено.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-118">The store has been disabled.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="8f3eb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8f3eb-119">Requirements</span></span>



| <span data-ttu-id="8f3eb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8f3eb-120">Requirement</span></span> | <span data-ttu-id="8f3eb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8f3eb-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3eb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f3eb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8f3eb-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f3eb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8f3eb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f3eb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8f3eb-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8f3eb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8f3eb-126">Header</span><span class="sxs-lookup"><span data-stu-id="8f3eb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f3eb-127"><dt>Верапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f3eb-127"><dt>Werapi.h</dt></span></span> </dl> |



 

 





