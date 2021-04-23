---
description: В этом разделе содержатся сведения о вопросах безопасности, связанных с GDI. В этом разделе не приводятся все, что необходимо знать о проблемах безопасности. Вместо этого используйте его в качестве отправной точки и ссылки для этой области технологий.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Вопросы безопасности: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998955"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="d0b6d-105">Вопросы безопасности: GDI</span><span class="sxs-lookup"><span data-stu-id="d0b6d-105">Security Considerations: GDI</span></span>

<span data-ttu-id="d0b6d-106">В этом разделе содержатся сведения о вопросах безопасности, связанных с GDI.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-106">This topic provides information about security considerations related to GDI.</span></span> <span data-ttu-id="d0b6d-107">В этом разделе не приводятся все, что необходимо знать о проблемах безопасности.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-107">This topic does not provide all you need to know about security issues.</span></span> <span data-ttu-id="d0b6d-108">Вместо этого используйте его в качестве отправной точки и ссылки для этой области технологий.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-108">Instead, use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="d0b6d-109">GDI, как правило, имеет несколько проблем безопасности, так как работает с отображением, а не с входными данными.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-109">GDI generally has few security concerns because it deals with display rather than input.</span></span> <span data-ttu-id="d0b6d-110">Однако ниже приведены некоторые проблемы, которые следует учитывать.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-110">However, here are a few issues that you should consider.</span></span>

<span data-ttu-id="d0b6d-111">Точечные рисунки, метафайлы и шрифты являются сложными структурами, которые могут быть повреждены.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-111">Bitmaps, metafiles, and fonts are complex structures that could become corrupted.</span></span> <span data-ttu-id="d0b6d-112">Рекомендуется проверить, что эти элементы не повреждены и из надежного источника.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-112">It is good practice to try to ensure that these items are uncorrupted and from a trustworthy source.</span></span>

<span data-ttu-id="d0b6d-113">Приложение может указать дескриптор безопасности для некоторых API печати и буферизации.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-113">An application can specify the security descriptor for some of the printing and spooling APIs.</span></span> <span data-ttu-id="d0b6d-114">При задании дескриптора безопасности следует соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-114">You should take care when setting the security descriptor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0b6d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d0b6d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0b6d-116">Центр безопасности Майкрософт</span><span class="sxs-lookup"><span data-stu-id="d0b6d-116">Microsoft Security Central</span></span>](https://www.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="d0b6d-117">Центр разработчиков безопасности</span><span class="sxs-lookup"><span data-stu-id="d0b6d-117">Security Developer Center</span></span>](https://technet.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="d0b6d-118">Технический центр безопасности</span><span class="sxs-lookup"><span data-stu-id="d0b6d-118">Security TechCenter</span></span>](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



