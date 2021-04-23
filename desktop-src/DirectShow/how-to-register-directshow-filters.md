---
description: Как зарегистрировать фильтры DirectShow
ms.assetid: 2b6304c0-4b67-4723-94a0-7b1fff534f91
title: Как зарегистрировать фильтры DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301f26884115526e25e8875867f7cc2bdc628698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416656"
---
# <a name="how-to-register-directshow-filters"></a><span data-ttu-id="5ad78-103">Как зарегистрировать фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="5ad78-103">How to Register DirectShow Filters</span></span>

<span data-ttu-id="5ad78-104">В этой статье описывается, как выполнить самостоятельную регистрацию фильтра Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5ad78-104">This article describes how to make a Microsoft DirectShow filter self-registering.</span></span> <span data-ttu-id="5ad78-105">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="5ad78-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="5ad78-106">Структура разделов реестра</span><span class="sxs-lookup"><span data-stu-id="5ad78-106">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
-   [<span data-ttu-id="5ad78-107">Объявление сведений о фильтре</span><span class="sxs-lookup"><span data-stu-id="5ad78-107">Declaring Filter Information</span></span>](declaring-filter-information.md)
-   [<span data-ttu-id="5ad78-108">Объявление шаблона фабрики</span><span class="sxs-lookup"><span data-stu-id="5ad78-108">Declaring the Factory Template</span></span>](declaring-the-factory-template.md)
-   [<span data-ttu-id="5ad78-109">Реализация DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="5ad78-109">Implementing DllRegisterServer</span></span>](implementing-dllregisterserver.md)
-   [<span data-ttu-id="5ad78-110">Рекомендации по регистрации фильтров</span><span class="sxs-lookup"><span data-stu-id="5ad78-110">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
-   [<span data-ttu-id="5ad78-111">Отмена регистрации фильтра</span><span class="sxs-lookup"><span data-stu-id="5ad78-111">Unregistering a Filter</span></span>](unregistering-a-filter.md)

<span data-ttu-id="5ad78-112">В этой статье не описывается создание библиотеки DLL для фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5ad78-112">This article does not describe how to create a DLL for a DirectShow filter.</span></span> <span data-ttu-id="5ad78-113">Сведения о создании библиотек DLL см. в разделе [Создание библиотеки DLL фильтра DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="5ad78-113">For information on creating DLLs, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ad78-114">См. также</span><span class="sxs-lookup"><span data-stu-id="5ad78-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ad78-115">DirectShow и COM</span><span class="sxs-lookup"><span data-stu-id="5ad78-115">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



