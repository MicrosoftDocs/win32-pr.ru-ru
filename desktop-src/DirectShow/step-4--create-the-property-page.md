---
description: Реализуйте страницу свойств как часть создания страницы свойств фильтра для настраиваемого фильтра DirectShow.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Шаг 4. Создание страницы свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32cd9eacc98af5f273897a3837390ab5cc75f7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406857"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="dfebb-104">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="dfebb-104">Step 4.</span></span> <span data-ttu-id="dfebb-105">Создание страницы свойств</span><span class="sxs-lookup"><span data-stu-id="dfebb-105">Create the Property Page</span></span>

<span data-ttu-id="dfebb-106">На этом этапе фильтр поддерживает все, что требуется для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="dfebb-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="dfebb-107">Следующим шагом является реализация самой страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="dfebb-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="dfebb-108">Начните с создания производного класса от **кбасепропертипаже**.</span><span class="sxs-lookup"><span data-stu-id="dfebb-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="dfebb-109">В следующем примере показана часть объявления, включающая некоторые переменные закрытых членов, которые будут использоваться далее в примере:</span><span class="sxs-lookup"><span data-stu-id="dfebb-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


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



<span data-ttu-id="dfebb-110">Затем создайте ресурс диалогового окна в редакторе ресурсов, а также строковый ресурс для заголовка диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="dfebb-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="dfebb-111">Строка будет отображаться на вкладке страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="dfebb-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="dfebb-112">Эти два идентификатора ресурсов являются аргументами для конструктора **кбасепропертипаже** :</span><span class="sxs-lookup"><span data-stu-id="dfebb-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="dfebb-113">На следующем рисунке показан ресурс диалогового окна для страницы «пример свойства».</span><span class="sxs-lookup"><span data-stu-id="dfebb-113">The following illustration shows the dialog resource for the example property page.</span></span>

![диалоговое окно страницы свойств](images/proppage.png)

<span data-ttu-id="dfebb-115">Теперь все готово для реализации страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="dfebb-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="dfebb-116">Ниже приведены методы переопределения **кбасепропертипаже** .</span><span class="sxs-lookup"><span data-stu-id="dfebb-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="dfebb-117">**OnConnect** вызывается, когда клиент создает страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="dfebb-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="dfebb-118">Он задает для фильтра указатель **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="dfebb-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="dfebb-119">**OnActivate** вызывается при создании диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="dfebb-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="dfebb-120">**Онрецеивемессаже** вызывается, когда диалоговое окно получает сообщение окна.</span><span class="sxs-lookup"><span data-stu-id="dfebb-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="dfebb-121">**Онаппличанжес** вызывается, когда пользователь фиксирует изменения свойства, нажав кнопку **ОК** или **Применить** .</span><span class="sxs-lookup"><span data-stu-id="dfebb-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="dfebb-122">**Ondisconnectие** вызывается, когда пользователь закрывает страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="dfebb-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="dfebb-123">В оставшейся части этого руководства описывается каждый из этих методов.</span><span class="sxs-lookup"><span data-stu-id="dfebb-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="dfebb-124">Далее. [Шаг 5. Сохранить указатель на фильтр](step-5--store-a-pointer-to-the-filter.md).</span><span class="sxs-lookup"><span data-stu-id="dfebb-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfebb-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="dfebb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfebb-126">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="dfebb-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



