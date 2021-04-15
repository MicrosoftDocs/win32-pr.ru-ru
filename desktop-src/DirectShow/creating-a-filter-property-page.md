---
description: Создание страницы свойств фильтра
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Создание страницы свойств фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662025"
---
# <a name="creating-a-filter-property-page"></a><span data-ttu-id="9332e-103">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="9332e-103">Creating a Filter Property Page</span></span>

<span data-ttu-id="9332e-104">В этом разделе описывается создание страницы свойств для настраиваемого фильтра DirectShow с помощью класса [**кбасепропертипаже**](cbasepropertypage.md) .</span><span class="sxs-lookup"><span data-stu-id="9332e-104">This section describes how to create a property page for a custom DirectShow filter, using the [**CBasePropertyPage**](cbasepropertypage.md) class.</span></span> <span data-ttu-id="9332e-105">В примере кода в этом разделе показаны все шаги, необходимые для создания страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="9332e-105">The example code in this section shows all the steps needed to create a property page.</span></span> <span data-ttu-id="9332e-106">В примере показана страница свойств для гипотетического фильтра видеоэффектов, поддерживающего свойство насыщенности.</span><span class="sxs-lookup"><span data-stu-id="9332e-106">The example shows a property page for a hypothetical video effect filter that supports a saturation property.</span></span> <span data-ttu-id="9332e-107">На странице свойств имеется ползунок, который пользователь может перемещать для настройки уровня насыщенности фильтра.</span><span class="sxs-lookup"><span data-stu-id="9332e-107">The property page has a slider, which the user can move to adjust the filter's saturation level.</span></span>

<span data-ttu-id="9332e-108">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="9332e-108">This section contains the following topics:</span></span>

-   [<span data-ttu-id="9332e-109">Шаг 1. Определение механизма установки свойства</span><span class="sxs-lookup"><span data-stu-id="9332e-109">Step 1. Define a Mechanism for Setting the Property</span></span>](step-1--define-a-mechanism-for-setting-the-property.md)
-   [<span data-ttu-id="9332e-110">Шаг 2. Реализация ИспеЦифипропертипажес</span><span class="sxs-lookup"><span data-stu-id="9332e-110">Step 2. Implement ISpecifyPropertyPages</span></span>](step-2--implement-ispecifypropertypages.md)
-   [<span data-ttu-id="9332e-111">Шаг 3. Поддержка QueryInterface</span><span class="sxs-lookup"><span data-stu-id="9332e-111">Step 3. Support QueryInterface</span></span>](step-3--support-queryinterface.md)
-   [<span data-ttu-id="9332e-112">Шаг 4. Создание страницы свойств</span><span class="sxs-lookup"><span data-stu-id="9332e-112">Step 4. Create the Property Page</span></span>](step-4--create-the-property-page.md)
-   [<span data-ttu-id="9332e-113">Шаг 5. Сохранение указателя на фильтр</span><span class="sxs-lookup"><span data-stu-id="9332e-113">Step 5. Store a Pointer to the Filter</span></span>](step-5--store-a-pointer-to-the-filter.md)
-   [<span data-ttu-id="9332e-114">Шаг 6. Инициализация диалогового окна</span><span class="sxs-lookup"><span data-stu-id="9332e-114">Step 6. Initialize the Dialog</span></span>](step-6--initialize-the-dialog.md)
-   [<span data-ttu-id="9332e-115">Шаг 7. Обработку сообщений окна</span><span class="sxs-lookup"><span data-stu-id="9332e-115">Step 7. Handle Window Messages</span></span>](step-7--handle-window-messages.md)
-   [<span data-ttu-id="9332e-116">Шаг 8. Применить изменения свойств</span><span class="sxs-lookup"><span data-stu-id="9332e-116">Step 8. Apply Property Changes</span></span>](step-8--apply-property-changes.md)
-   [<span data-ttu-id="9332e-117">Шаг 9. Отключение страницы свойств</span><span class="sxs-lookup"><span data-stu-id="9332e-117">Step 9. Disconnect the Property Page</span></span>](step-9--disconnect-the-property-page.md)
-   [<span data-ttu-id="9332e-118">Шаг 10. Поддержка регистрации COM</span><span class="sxs-lookup"><span data-stu-id="9332e-118">Step 10. Support COM Registration</span></span>](step-10--support-com-registration.md)

## <a name="related-topics"></a><span data-ttu-id="9332e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="9332e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9332e-120">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="9332e-120">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



