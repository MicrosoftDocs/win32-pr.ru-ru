---
description: .
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Совместимость с DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb542331d218ed4c493efde091be3e5efae6aee
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713271"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="7daf8-103">Совместимость с DEP/NX</span><span class="sxs-lookup"><span data-stu-id="7daf8-103">DEP/NX compatibility</span></span>

<span data-ttu-id="7daf8-104">По умолчанию в Windows Internet Explorer 7 функция DEP/NX отключена в целях совместимости.</span><span class="sxs-lookup"><span data-stu-id="7daf8-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="7daf8-105">Некоторые популярные надстройки несовместимы с DEP/NX и не работают, если Windows Internet Explorer загружает их с включенной функцией DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7daf8-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="7daf8-106">Как правило, эти надстройки создаются с помощью более старой версии платформы ATL.</span><span class="sxs-lookup"><span data-stu-id="7daf8-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="7daf8-107">ATL 7,1 и более ранние версии не разработаны с функцией безопасности DEP.</span><span class="sxs-lookup"><span data-stu-id="7daf8-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="7daf8-108">К счастью, новые версии пакетов обновления Microsoft Windows имеют новые API-интерфейсы DEP/NX, позволяющие использовать DEP/NX и хранить совместимость с более старыми версиями ATL.</span><span class="sxs-lookup"><span data-stu-id="7daf8-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="7daf8-109">Эти новые API позволяют Internet Explorer отказаться от DEP/NX, не вызывая сбой надстроек, созданных с помощью более старых версий ATL.</span><span class="sxs-lookup"><span data-stu-id="7daf8-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="7daf8-110">Если надстройка не совместима с DEP/NX и не использует устаревшую библиотеку ATL, можно использовать параметр групповая политика, чтобы отказаться от DEP/NX для Internet Explorer до тех пор, пока не будет развернута обновленная версия неработающего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="7daf8-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="7daf8-111">Локальные администраторы могут управлять DEP/NX, запуская Internet Explorer от имени администратора и сняв флажок **включить защиту памяти** на панели **Дополнительно** **диалогового окна Свойства обозревателя**.</span><span class="sxs-lookup"><span data-stu-id="7daf8-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7daf8-112">См. также</span><span class="sxs-lookup"><span data-stu-id="7daf8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7daf8-113">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="7daf8-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
