---
title: EC_WMT_INDEX_EVENT (пакет SDK для формата Windows Media 11)
description: '\_ \_ событие индекса EC \_ ВМТ'
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- Пакет SDK Windows Media Format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Расширенный формат систем (ASF), EC_WMT_INDEX_EVENT
- ASF (Расширенный системный формат), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070951"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a><span data-ttu-id="52d26-108">EC_WMT_INDEX_EVENT (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="52d26-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="52d26-109">Отправляется пакетом SDK Windows Media Format, когда приложение использует модуль записи ASF для индексирования видеофайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="52d26-109">Sent by the Windows Media Format SDK when an application uses the ASF Writer to index Windows Media Video files.</span></span>

<span data-ttu-id="52d26-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="52d26-110">Parameters</span></span>

<span data-ttu-id="52d26-111">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="52d26-111">*lParam1*</span></span>

<span data-ttu-id="52d26-112">Может быть одним из следующих сообщений **\_ о состоянии ВМТ** .</span><span class="sxs-lookup"><span data-stu-id="52d26-112">Can be any one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="52d26-113">Сообщение</span><span class="sxs-lookup"><span data-stu-id="52d26-113">Message</span></span>              | <span data-ttu-id="52d26-114">Описание</span><span class="sxs-lookup"><span data-stu-id="52d26-114">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="52d26-115">ВМТ \_ запущен</span><span class="sxs-lookup"><span data-stu-id="52d26-115">WMT\_STARTED</span></span>         | <span data-ttu-id="52d26-116">Индексирование начато.</span><span class="sxs-lookup"><span data-stu-id="52d26-116">Indexing has begun.</span></span> <span data-ttu-id="52d26-117">*lParam2* имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="52d26-117">*lParam2* is zero.</span></span>          |
| <span data-ttu-id="52d26-118">ВМТ \_ закрыт</span><span class="sxs-lookup"><span data-stu-id="52d26-118">WMT\_CLOSED</span></span>          | <span data-ttu-id="52d26-119">Индексирование завершено.</span><span class="sxs-lookup"><span data-stu-id="52d26-119">Indexing has been completed.</span></span> <span data-ttu-id="52d26-120">*lParam2* имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="52d26-120">*lParam2* is zero.</span></span> |
| <span data-ttu-id="52d26-121">\_ \_ ход выполнения индекса ВМТ</span><span class="sxs-lookup"><span data-stu-id="52d26-121">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="52d26-122">Выполняется индексирование.</span><span class="sxs-lookup"><span data-stu-id="52d26-122">Indexing is in progress.</span></span>                        |



 

<span data-ttu-id="52d26-123">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="52d26-123">*lParam2*</span></span>

<span data-ttu-id="52d26-124">Если *LPARAM1* ВМТ \_ Closed или ВМТ \_ Started, то *lParam2* равен нулю.</span><span class="sxs-lookup"><span data-stu-id="52d26-124">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="52d26-125">Если *lParam1* является ВМТ \_ \_ ходом выполнения индекса, то *lParam2* представляет собой **DWORD** , который выражает объем работ в процентах от общего размера загрузки.</span><span class="sxs-lookup"><span data-stu-id="52d26-125">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that expresses the amount of progress as a percentage of the total download size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52d26-126">См. также</span><span class="sxs-lookup"><span data-stu-id="52d26-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52d26-127">**Справочник по КАСФ DirectShow**</span><span class="sxs-lookup"><span data-stu-id="52d26-127">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 




