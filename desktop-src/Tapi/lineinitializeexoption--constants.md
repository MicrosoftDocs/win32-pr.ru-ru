---
description: '\_Константы линеинитиализиксоптион указывают, какой механизм уведомления о событиях следует использовать при инициализации сеанса.'
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Константы LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689160"
---
# <a name="lineinitializeexoption_-constants"></a><span data-ttu-id="7af24-103">\_Константы линеинитиализиксоптион</span><span class="sxs-lookup"><span data-stu-id="7af24-103">LINEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="7af24-104">Константы **линеинитиализиксоптион \_** указывают, какой механизм уведомления о событиях следует использовать при инициализации сеанса.</span><span class="sxs-lookup"><span data-stu-id="7af24-104">The **LINEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="7af24-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**ЛИНЕИНИТИАЛИЗИКСОПТИОН \_ каллхубтраккинг**</span><span class="sxs-lookup"><span data-stu-id="7af24-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7af24-106">Приложение похочет использовать механизм уведомления о событии для отслеживания центра вызовов.</span><span class="sxs-lookup"><span data-stu-id="7af24-106">The application desires to use the call hub tracking event notification mechanism.</span></span> <span data-ttu-id="7af24-107">Эта константа предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="7af24-107">This constant is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7af24-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**ЛИНЕИНИТИАЛИЗИКСОПТИОН \_ усекомплетионпорт**</span><span class="sxs-lookup"><span data-stu-id="7af24-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7af24-109">Приложение похочет использовать механизм уведомления о событиях порта завершения.</span><span class="sxs-lookup"><span data-stu-id="7af24-109">The application desires to use the Completion Port event notification mechanism.</span></span> <span data-ttu-id="7af24-110">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="7af24-110">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7af24-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**ЛИНЕИНИТИАЛИЗИКСОПТИОН \_ усивент**</span><span class="sxs-lookup"><span data-stu-id="7af24-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7af24-112">Приложение использует механизм уведомления о событиях обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="7af24-112">The application desires to use the Event Handle event notification mechanism.</span></span> <span data-ttu-id="7af24-113">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="7af24-113">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7af24-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**ЛИНЕИНИТИАЛИЗИКСОПТИОН \_ усехидденвиндов**</span><span class="sxs-lookup"><span data-stu-id="7af24-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7af24-115">Необходимо, чтобы приложение использовало механизм уведомления о событиях скрытого окна.</span><span class="sxs-lookup"><span data-stu-id="7af24-115">The application desires to use the Hidden Window event notification mechanism.</span></span> <span data-ttu-id="7af24-116">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="7af24-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7af24-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7af24-117">Remarks</span></span>

<span data-ttu-id="7af24-118">Дополнительные сведения о работе этих параметров см. в разделе [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="7af24-118">See [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af24-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7af24-119">Requirements</span></span>



| <span data-ttu-id="7af24-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7af24-120">Requirement</span></span> | <span data-ttu-id="7af24-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7af24-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7af24-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="7af24-122">TAPI version</span></span><br/> | <span data-ttu-id="7af24-123">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7af24-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7af24-124">Header</span><span class="sxs-lookup"><span data-stu-id="7af24-124">Header</span></span><br/>       | <dl> <span data-ttu-id="7af24-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7af24-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




