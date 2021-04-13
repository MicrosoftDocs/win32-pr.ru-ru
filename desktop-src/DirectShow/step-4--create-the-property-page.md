---
description: Шаг 4.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Шаг 4. Создание страницы свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273127"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="7cf3c-104">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-104">Step 4.</span></span> <span data-ttu-id="7cf3c-105">Создание страницы свойств</span><span class="sxs-lookup"><span data-stu-id="7cf3c-105">Create the Property Page</span></span>

<span data-ttu-id="7cf3c-106">На этом этапе фильтр поддерживает все, что требуется для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="7cf3c-107">Следующим шагом является реализация самой страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="7cf3c-108">Начните с создания производного класса от **кбасепропертипаже**.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="7cf3c-109">В следующем примере показана часть объявления, включающая некоторые переменные закрытых членов, которые будут использоваться далее в примере:</span><span class="sxs-lookup"><span data-stu-id="7cf3c-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



<span data-ttu-id="7cf3c-110">Затем создайте ресурс диалогового окна в редакторе ресурсов, а также строковый ресурс для заголовка диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="7cf3c-111">Строка будет отображаться на вкладке страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="7cf3c-112">Эти два идентификатора ресурсов являются аргументами для конструктора **кбасепропертипаже** :</span><span class="sxs-lookup"><span data-stu-id="7cf3c-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="7cf3c-113">На следующем рисунке показан ресурс диалогового окна для страницы «пример свойства».</span><span class="sxs-lookup"><span data-stu-id="7cf3c-113">The following illustration shows the dialog resource for the example property page.</span></span>

![диалоговое окно страницы свойств](images/proppage.png)

<span data-ttu-id="7cf3c-115">Теперь все готово для реализации страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="7cf3c-116">Ниже приведены методы переопределения **кбасепропертипаже** .</span><span class="sxs-lookup"><span data-stu-id="7cf3c-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="7cf3c-117">**OnConnect** вызывается, когда клиент создает страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="7cf3c-118">Он задает для фильтра указатель **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="7cf3c-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="7cf3c-119">**OnActivate** вызывается при создании диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="7cf3c-120">**Онрецеивемессаже** вызывается, когда диалоговое окно получает сообщение окна.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="7cf3c-121">**Онаппличанжес** вызывается, когда пользователь фиксирует изменения свойства, нажав кнопку **ОК** или **Применить** .</span><span class="sxs-lookup"><span data-stu-id="7cf3c-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="7cf3c-122">**Ondisconnectие** вызывается, когда пользователь закрывает страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="7cf3c-123">В оставшейся части этого руководства описывается каждый из этих методов.</span><span class="sxs-lookup"><span data-stu-id="7cf3c-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="7cf3c-124">Далее. [Шаг 5. Сохранить указатель на фильтр](step-5--store-a-pointer-to-the-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7cf3c-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cf3c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7cf3c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cf3c-126">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="7cf3c-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



