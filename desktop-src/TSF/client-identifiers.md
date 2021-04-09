---
title: Идентификаторы клиентов
description: Идентификаторы клиентов
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Платформа текстовых служб (TSF), идентификаторы клиентов
- TSF (платформа текстовых служб), идентификаторы клиентов
- текстовые службы, идентификаторы клиентов
- Приложения с поддержкой TSF, идентификаторы клиентов
- идентификаторы клиентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de15b208d2fbc6c6ea5c2a1114eb5cb23ff12ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986293"
---
# <a name="client-identifiers"></a><span data-ttu-id="32496-108">Идентификаторы клиентов</span><span class="sxs-lookup"><span data-stu-id="32496-108">Client Identifiers</span></span>

## <a name="applications"></a><span data-ttu-id="32496-109">Приложения</span><span class="sxs-lookup"><span data-stu-id="32496-109">Applications</span></span>

<span data-ttu-id="32496-110">Приложение получает свой идентификатор клиента путем вызова [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span><span class="sxs-lookup"><span data-stu-id="32496-110">An application obtains its client identifier by calling [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span>

## <a name="text-services"></a><span data-ttu-id="32496-111">Текстовые службы</span><span class="sxs-lookup"><span data-stu-id="32496-111">Text Services</span></span>

<span data-ttu-id="32496-112">Служба текстового ввода получает свой идентификатор клиента при вызове метода [итфтекстинпутпроцессор:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) текстовой службы.</span><span class="sxs-lookup"><span data-stu-id="32496-112">A text service obtains its client identifier when the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method is called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32496-113">См. также</span><span class="sxs-lookup"><span data-stu-id="32496-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32496-114">ITfThreadMgr:: Activate</span><span class="sxs-lookup"><span data-stu-id="32496-114">ITfThreadMgr::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[<span data-ttu-id="32496-115">Итфтекстинпутпроцессор:: Activate</span><span class="sxs-lookup"><span data-stu-id="32496-115">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




