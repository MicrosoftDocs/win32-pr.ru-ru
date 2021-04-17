---
description: Атрибуты сеанса мультимедиа
ms.assetid: 7f9cef1c-b419-485f-ac01-afb9f42e5bd6
title: Атрибуты сеанса мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a58c0ac1f6ccd3132bb83324a4abec333a079d7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713284"
---
# <a name="media-session-attributes"></a><span data-ttu-id="93f3b-103">Атрибуты сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="93f3b-103">Media Session Attributes</span></span>

<span data-ttu-id="93f3b-104">Для настройки сеанса мультимедиа используются следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="93f3b-104">The following attributes are used to configure the Media Session.</span></span>



| <span data-ttu-id="93f3b-105">attribute</span><span class="sxs-lookup"><span data-stu-id="93f3b-105">Attribute</span></span>                                                                                            | <span data-ttu-id="93f3b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="93f3b-106">Description</span></span>                                                                                                 |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93f3b-107">**\_ \_ \_ диспетчер защиты содержимого сеанса \_ MF**</span><span class="sxs-lookup"><span data-stu-id="93f3b-107">**MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER**</span></span>](mf-session-content-protection-manager-attribute.md) | <span data-ttu-id="93f3b-108">Предоставляет интерфейс обратного вызова для приложения, получающего объект включения содержимого из сеанса PMP.</span><span class="sxs-lookup"><span data-stu-id="93f3b-108">Provides a callback interface for the application to receive a content enabler object from the PMP session.</span></span> |
| [<span data-ttu-id="93f3b-109">**\_ \_ глобальное время сеанса \_ MF**</span><span class="sxs-lookup"><span data-stu-id="93f3b-109">**MF\_SESSION\_GLOBAL\_TIME**</span></span>](mf-session-global-time-attribute.md)                                | <span data-ttu-id="93f3b-110">Указывает, будут ли топологии иметь глобальное время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="93f3b-110">Specifies whether topologies will have a global start and stop time.</span></span>                                        |
| [<span data-ttu-id="93f3b-111">**\_ \_ Диспетчер качества сеансов \_ MF**</span><span class="sxs-lookup"><span data-stu-id="93f3b-111">**MF\_SESSION\_QUALITY\_MANAGER**</span></span>](mf-session-quality-manager-attribute.md)                        | <span data-ttu-id="93f3b-112">Содержит идентификатор CLSID диспетчера качества для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="93f3b-112">Contains the CLSID of a quality manager for the Media Session.</span></span>                                              |
| [<span data-ttu-id="93f3b-113">**\_ \_ Удаленный \_ исходный режим сеанса \_ MF**</span><span class="sxs-lookup"><span data-stu-id="93f3b-113">**MF\_SESSION\_REMOTE\_SOURCE\_MODE**</span></span>](mf-session-remote-source-mode-attribute.md)                 | <span data-ttu-id="93f3b-114">Указывает, что источник мультимедиа выполняется в удаленном процессе.</span><span class="sxs-lookup"><span data-stu-id="93f3b-114">Specifies that the media source is running in a remote process.</span></span>                                             |
| [<span data-ttu-id="93f3b-115">**\_ \_ контекст сервера сеансов \_ MF**</span><span class="sxs-lookup"><span data-stu-id="93f3b-115">**MF\_SESSION\_SERVER\_CONTEXT**</span></span>](mf-session-server-context-attribute.md)                          | <span data-ttu-id="93f3b-116">Позволяет двум экземплярам сеанса мультимедиа совместно использовать один и тот же процесс PMP.</span><span class="sxs-lookup"><span data-stu-id="93f3b-116">Enables two instances of the Media Session to share the same PMP process.</span></span>                                   |
| [<span data-ttu-id="93f3b-117">**\_тополоадер сеанс \_ MF**</span><span class="sxs-lookup"><span data-stu-id="93f3b-117">**MF\_SESSION\_TOPOLOADER**</span></span>](mf-session-topoloader-attribute.md)                                   | <span data-ttu-id="93f3b-118">Содержит идентификатор CLSID для загрузчика топологии для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="93f3b-118">Contains the CLSID of a topology loader for the Media Session.</span></span>                                              |



 

## <a name="related-topics"></a><span data-ttu-id="93f3b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="93f3b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93f3b-120">**имфмедиасессион**</span><span class="sxs-lookup"><span data-stu-id="93f3b-120">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[<span data-ttu-id="93f3b-121">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="93f3b-121">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



