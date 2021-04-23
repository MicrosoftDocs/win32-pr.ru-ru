---
description: XAudio2 конкретные коды ошибок, возвращаемые методами XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Коды ошибок XAudio2 (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699046"
---
# <a name="xaudio2-error-codes"></a><span data-ttu-id="b3ee4-103">Коды ошибок XAudio2</span><span class="sxs-lookup"><span data-stu-id="b3ee4-103">XAudio2 Error Codes</span></span>

<span data-ttu-id="b3ee4-104">XAudio2 конкретные коды ошибок, возвращаемые методами XAudio2.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-104">XAudio2 specific error codes returned by XAudio2 methods.</span></span>



| <span data-ttu-id="b3ee4-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="b3ee4-105">Constant/value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="b3ee4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b3ee4-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <span data-ttu-id="b3ee4-107"><dt>**XAUDIO2 \_ E \_ Недопустимый \_ вызов**</dt> <dt>0x88960001</dt></span><span class="sxs-lookup"><span data-stu-id="b3ee4-107"><dt>**XAUDIO2\_E\_INVALID\_CALL**</dt> <dt>0x88960001</dt></span></span> </dl>                          | <span data-ttu-id="b3ee4-108">Возвращается функцией XAudio2 для определенных ошибок использования API (недопустимые вызовы и т. д.), которые трудно избежать полностью и должны обрабатываться заголовком во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-108">Returned by XAudio2 for certain API usage errors (invalid calls and so on) that are hard to avoid completely and should be handled by a title at runtime.</span></span> <span data-ttu-id="b3ee4-109">(Ошибки использования API, которые полностью избегают, например недопустимые параметры, вызывают утверждение в отладочных сборках и неопределенное поведение в розничных сборках, поэтому код ошибки не определен.)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-109">(API usage errors that are completely avoidable, such as invalid parameters, cause an ASSERT in debug builds and undefined behavior in retail builds, so no error code is defined for them.)</span></span><br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <span data-ttu-id="b3ee4-110"><dt>**XAUDIO2 \_ E \_ XMA \_ декодер \_ Ошибка**</dt> <dt>0x88960002</dt></span><span class="sxs-lookup"><span data-stu-id="b3ee4-110"><dt>**XAUDIO2\_E\_XMA\_DECODER\_ERROR**</dt> <dt>0x88960002</dt></span></span> </dl>          | <span data-ttu-id="b3ee4-111">Неустранимая ошибка оборудования Xbox 360 XMA.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-111">The Xbox 360 XMA hardware suffered an unrecoverable error.</span></span><br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <span data-ttu-id="b3ee4-112"><dt>**XAUDIO2 \_ \_ \_ \_ Не удалось создать ксапо**</dt> <dt>0x88960003</dt></span><span class="sxs-lookup"><span data-stu-id="b3ee4-112"><dt>**XAUDIO2\_E\_XAPO\_CREATION\_FAILED**</dt> <dt>0x88960003</dt></span></span> </dl> | <span data-ttu-id="b3ee4-113">Результату не удалось создать экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-113">An effect failed to instantiate.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <span data-ttu-id="b3ee4-114"><dt>**XAUDIO2 \_ \_ \_ Непроверенное устройство E**</dt> <dt>0x88960004</dt></span><span class="sxs-lookup"><span data-stu-id="b3ee4-114"><dt>**XAUDIO2\_E\_DEVICE\_INVALIDATED**</dt> <dt>0x88960004</dt></span></span> </dl>        | <span data-ttu-id="b3ee4-115">Звуковое устройство стало непригодным для использования посредством отключения от сети или какого-либо другого события.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-115">An audio device became unusable through being unplugged or some other event.</span></span><br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="b3ee4-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3ee4-116">Remarks</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="b3ee4-117">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="b3ee4-117">Platform Requirements</span></span>

<span data-ttu-id="b3ee4-118">Windows 10 (Ксаудио 2.9); Windows 8, Windows Phone 8 (Ксаудио 2,8); Пакет SDK для DirectX (Ксаудио 2,7)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-118">Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ee4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b3ee4-119">Requirements</span></span>



| <span data-ttu-id="b3ee4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b3ee4-120">Requirement</span></span> | <span data-ttu-id="b3ee4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b3ee4-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ee4-122">Header</span><span class="sxs-lookup"><span data-stu-id="b3ee4-122">Header</span></span><br/> | <dl> <span data-ttu-id="b3ee4-123"><dt>Xaudio2. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3ee4-123"><dt>Xaudio2.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3ee4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3ee4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ee4-125">XAudio2:: константы</span><span class="sxs-lookup"><span data-stu-id="b3ee4-125">XAudio2::Constants</span></span>](constants.md)
</dt> </dl>

 

 




