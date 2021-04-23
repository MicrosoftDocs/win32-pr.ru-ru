---
description: Вызывается модулем политики, когда начинается Индивидуальная подготовка. Индивидуальная реализация осуществляется с помощью реализации интерфейса Имфконтентпротектионманажер в приложениях.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Событие Меиндивидуализатионстарт (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb8d50bbc2081c4efa41d8b15cc3e41a14ab5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656584"
---
# <a name="meindividualizationstart-event"></a><span data-ttu-id="51123-104">Событие Меиндивидуализатионстарт</span><span class="sxs-lookup"><span data-stu-id="51123-104">MEIndividualizationStart event</span></span>

<span data-ttu-id="51123-105">Вызывается модулем политики, когда начинается Индивидуальная подготовка.</span><span class="sxs-lookup"><span data-stu-id="51123-105">Raised by the policy engine when individualization is about to begin.</span></span> <span data-ttu-id="51123-106">Индивидуальная реализация осуществляется с помощью реализации интерфейса [**имфконтентпротектионманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) в приложении.</span><span class="sxs-lookup"><span data-stu-id="51123-106">Individualization is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="51123-107">Отдельное приложение — это одно из приложений, которое получило обновление до компонентов управления цифровыми правами (DRM), которое отличает его от всех остальных копий того же приложения.</span><span class="sxs-lookup"><span data-stu-id="51123-107">An individualized application is one that has received an upgrade to its digital rights management (DRM) components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="51123-108">Владельцы содержимого могут потребовать, чтобы их защищенные файлы воспроизводились только в приложении, которое было индивидуальным.</span><span class="sxs-lookup"><span data-stu-id="51123-108">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

## <a name="event-values"></a><span data-ttu-id="51123-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="51123-109">Event values</span></span>

<span data-ttu-id="51123-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="51123-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="51123-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="51123-111">VARTYPE</span></span>              | <span data-ttu-id="51123-112">Описание</span><span class="sxs-lookup"><span data-stu-id="51123-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="51123-113">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="51123-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="51123-114">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="51123-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="51123-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51123-115">Remarks</span></span>

<span data-ttu-id="51123-116">По завершении приобретения лицензии обработчик политики вызывает событие [меиндивидуализатионкомплетед](meindividualizationcompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="51123-116">When license acquisition is completed, the policy engine raises the [MEIndividualizationCompleted](meindividualizationcompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="51123-117">Требования</span><span class="sxs-lookup"><span data-stu-id="51123-117">Requirements</span></span>



| <span data-ttu-id="51123-118">Требование</span><span class="sxs-lookup"><span data-stu-id="51123-118">Requirement</span></span> | <span data-ttu-id="51123-119">Значение</span><span class="sxs-lookup"><span data-stu-id="51123-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51123-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51123-120">Minimum supported client</span></span><br/> | <span data-ttu-id="51123-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51123-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="51123-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51123-122">Minimum supported server</span></span><br/> | <span data-ttu-id="51123-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51123-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51123-124">Header</span><span class="sxs-lookup"><span data-stu-id="51123-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="51123-125"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51123-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51123-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51123-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51123-127">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51123-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




