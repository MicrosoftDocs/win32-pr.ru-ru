---
description: ELS поддерживает функции, определенные в следующей таблице.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Расширенные функции лингвистических служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650908"
---
# <a name="extended-linguistic-services-functions"></a><span data-ttu-id="af902-103">Расширенные функции лингвистических служб</span><span class="sxs-lookup"><span data-stu-id="af902-103">Extended Linguistic Services Functions</span></span>

<span data-ttu-id="af902-104">ELS поддерживает функции, определенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="af902-104">ELS supports the functions defined in the following table.</span></span>



| <span data-ttu-id="af902-105">Функция</span><span class="sxs-lookup"><span data-stu-id="af902-105">Function</span></span>                                                 | <span data-ttu-id="af902-106">Описание</span><span class="sxs-lookup"><span data-stu-id="af902-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af902-107">**маппингкаллбаккпрок**</span><span class="sxs-lookup"><span data-stu-id="af902-107">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | <span data-ttu-id="af902-108">Определяемая приложением функция обратного вызова, которая асинхронно обрабатывает данные, созданные функцией **маппингрекогнизетекст** .</span><span class="sxs-lookup"><span data-stu-id="af902-108">An application-defined callback function that asynchronously processes data produced by the **MappingRecognizeText** function.</span></span>                 |
| [<span data-ttu-id="af902-109">**маппингдоактион**</span><span class="sxs-lookup"><span data-stu-id="af902-109">**MappingDoAction**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | <span data-ttu-id="af902-110">Заставляет службу ELS выполнить действие после распознавания текста.</span><span class="sxs-lookup"><span data-stu-id="af902-110">Causes an ELS service to perform an action after text recognition has occurred.</span></span>                                                                |
| [<span data-ttu-id="af902-111">**маппингфрипропертибаг**</span><span class="sxs-lookup"><span data-stu-id="af902-111">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | <span data-ttu-id="af902-112">Освобождает память и ресурсы, выделенные во время операции распознавания текста ELS.</span><span class="sxs-lookup"><span data-stu-id="af902-112">Frees memory and resources allocated during an ELS text recognition operation.</span></span>                                                                 |
| [<span data-ttu-id="af902-113">**маппингфрисервицес**</span><span class="sxs-lookup"><span data-stu-id="af902-113">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | <span data-ttu-id="af902-114">Освобождает память и ресурсы, выделенные для взаимодействия приложения с одной или несколькими службами ELS.</span><span class="sxs-lookup"><span data-stu-id="af902-114">Frees memory and resources allocated for the application to interact with one or more ELS services.</span></span>                                            |
| [<span data-ttu-id="af902-115">**маппингжетсервицес**</span><span class="sxs-lookup"><span data-stu-id="af902-115">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | <span data-ttu-id="af902-116">Извлекает список доступных служб, поддерживаемых платформой ELS, вместе со связанной информацией в соответствии с заданным приложением критерием.</span><span class="sxs-lookup"><span data-stu-id="af902-116">Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.</span></span> |
| [<span data-ttu-id="af902-117">**маппингрекогнизетекст**</span><span class="sxs-lookup"><span data-stu-id="af902-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | <span data-ttu-id="af902-118">Вызывает службу ELS для распознавания текста.</span><span class="sxs-lookup"><span data-stu-id="af902-118">Calls upon an ELS service to recognize text.</span></span>                                                                                                   |



 

 

 



