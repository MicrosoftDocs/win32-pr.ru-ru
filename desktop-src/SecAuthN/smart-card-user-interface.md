---
description: Пользовательский интерфейс смарт-карты — это одно общее диалоговое окно, которое позволяет пользователю указать или найти смарт-карту, которую нужно открыть (то есть подключиться и использовать в приложении).
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Пользовательский интерфейс смарт-карты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664162"
---
# <a name="smart-card-user-interface"></a><span data-ttu-id="b409c-103">Пользовательский интерфейс смарт-карты</span><span class="sxs-lookup"><span data-stu-id="b409c-103">Smart Card User Interface</span></span>

<span data-ttu-id="b409c-104">[*Пользовательский интерфейс*](../secgloss/u-gly.md) смарт-карты — это одно [*общее диалоговое окно*](../secgloss/s-gly.md) , которое позволяет пользователю указать или найти смарт-карту, которую нужно открыть (то есть подключиться и использовать в приложении).</span><span class="sxs-lookup"><span data-stu-id="b409c-104">The smart card [*user interface*](../secgloss/u-gly.md) (UI) is a single [*common dialog box*](../secgloss/s-gly.md) that lets the user specify or search for a smart card to open (that is, connect to and use in an application).</span></span>

<span data-ttu-id="b409c-105">Ниже приведены два способа использования диалогового окна общее.</span><span class="sxs-lookup"><span data-stu-id="b409c-105">Following are two ways you can use the common dialog box.</span></span> <span data-ttu-id="b409c-106">Оба варианта предполагают, что будет отображаться пользовательский интерфейс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b409c-106">Both assume that the dialog box UI will be displayed.</span></span> <span data-ttu-id="b409c-107">Дополнительные сведения см. в разделе [**опенкарднаме**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).</span><span class="sxs-lookup"><span data-stu-id="b409c-107">For more information, see [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).</span></span>

<span data-ttu-id="b409c-108">**Выбор смарт-карты для открытия**</span><span class="sxs-lookup"><span data-stu-id="b409c-108">**To select a smart card to open**</span></span>

1.  <span data-ttu-id="b409c-109">Объявите переменную типа **опенкарднаме**.</span><span class="sxs-lookup"><span data-stu-id="b409c-109">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="b409c-110">Укажите достаточно информации в общем диалоговом окне, чтобы уточнить поиск смарт-карты, которую ищет вызывающее приложение.</span><span class="sxs-lookup"><span data-stu-id="b409c-110">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="b409c-111">Это включает в себя указание **лпстрграупнамес**, **лпстркарднамес** и **рггуидинтерфацес**.</span><span class="sxs-lookup"><span data-stu-id="b409c-111">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span> <span data-ttu-id="b409c-112">Сюда также входит указание предпочтительного режима общего доступа и используемого протокола, когда общее диалоговое окно подключается к карточке с помощью членов **двшаремоде** и **двпреферредпротоколс** структуры [**опенкарднаме**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) .</span><span class="sxs-lookup"><span data-stu-id="b409c-112">This also includes specifying a preferred share mode and protocol to use when the common dialog box connects to the card by using the **dwShareMode** and **dwPreferredProtocols** members of the [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) structure.</span></span>
3.  <span data-ttu-id="b409c-113">Вызовите функцию [**жетопенкарднаме**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) , чтобы отобразить общее диалоговое окно для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b409c-113">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) function to display the common dialog box to the user.</span></span> <span data-ttu-id="b409c-114">Будет отображена простая строка справочной информации, и если одна из запрашиваемых карточек найдена, карточка будет выделена на экране.</span><span class="sxs-lookup"><span data-stu-id="b409c-114">A simple help information line will be displayed, and if one of the cards being requested is found, the card will be highlighted in the display.</span></span> <span data-ttu-id="b409c-115">При поиске нескольких имен карт будет выделено первое средство чтения, содержащее одну из предпочтительных карточек.</span><span class="sxs-lookup"><span data-stu-id="b409c-115">For multiple card name searches, the first reader that contains one of the preferred cards will be highlighted.</span></span>
4.  <span data-ttu-id="b409c-116">Затем пользователь выбирает карту, нажимает кнопку **ОК** и подключается к смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="b409c-116">The user then selects a card, clicks **OK**, and connects to the smart card.</span></span>

<span data-ttu-id="b409c-117">**Поиск конкретной карточки**</span><span class="sxs-lookup"><span data-stu-id="b409c-117">**To search for a specific card**</span></span>

1.  <span data-ttu-id="b409c-118">Объявите переменную типа **опенкарднаме**.</span><span class="sxs-lookup"><span data-stu-id="b409c-118">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="b409c-119">Укажите достаточно информации в общем диалоговом окне, чтобы уточнить поиск смарт-карты, которую ищет вызывающее приложение.</span><span class="sxs-lookup"><span data-stu-id="b409c-119">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="b409c-120">Это включает в себя указание **лпстрграупнамес**, **лпстркарднамес** и **рггуидинтерфацес**.</span><span class="sxs-lookup"><span data-stu-id="b409c-120">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span>
3.  <span data-ttu-id="b409c-121">Создайте функции обратного вызова **Connect**, **Check** и **Disconnect** , а также настройте элементы данных **лпфнконнект**, **лпфнчекк** и **лпфндисконнект** соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="b409c-121">Create the **Connect**, **Check**, and **Disconnect** callback functions, and set the **lpfnConnect**, **lpfnCheck**, and **lpfnDisconnect** data members appropriately.</span></span>
    > [!Note]  
    > <span data-ttu-id="b409c-122">Все три функции и члены должны быть доступны при использовании общего диалогового окна таким образом.</span><span class="sxs-lookup"><span data-stu-id="b409c-122">All three functions and members must be available when using the common dialog box in this way.</span></span>

     

4.  <span data-ttu-id="b409c-123">Вызов функции общего диалогового окна [**жетопенкарднаме**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) .</span><span class="sxs-lookup"><span data-stu-id="b409c-123">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) common dialog box function.</span></span>
5.  <span data-ttu-id="b409c-124">Затем общее диалоговое окно будет искать запрошенные карточки.</span><span class="sxs-lookup"><span data-stu-id="b409c-124">The common dialog box will then search for the requested cards.</span></span> <span data-ttu-id="b409c-125">Если найдено совпадающее имя карты или [*строка ATR*](../secgloss/a-gly.md) , функции обратного вызова **Connect**, **Check** и **Disconnect** будут вызываться последовательно.</span><span class="sxs-lookup"><span data-stu-id="b409c-125">If a matching card name or [*ATR string*](../secgloss/a-gly.md) is found, the **Connect**, **Check**, and **Disconnect** callback functions will be called in sequence.</span></span> <span data-ttu-id="b409c-126">Если карта передает подпрограммы **проверки** (то есть функция обратного вызова **проверки** возвращает **значение true**), эта карточка выделяется пользователю на экране.</span><span class="sxs-lookup"><span data-stu-id="b409c-126">If a card passes the **Check** routine (that is, the **Check** callback returns **TRUE**), this card is highlighted in the display to the user.</span></span>
    > [!Note]  
    > <span data-ttu-id="b409c-127">Если задано несколько имен карточек, то первый модуль чтения, который содержит одну из запрошенных карточек, и передает подпрограмму **проверки** , будет выбранной картой.</span><span class="sxs-lookup"><span data-stu-id="b409c-127">If multiple card names are given, the first reader that contains one of the requested cards and passes the **Check** routine will be the selected card.</span></span>

     

6.  <span data-ttu-id="b409c-128">Если совпадений не найдено, появится общее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b409c-128">If no matches are found, a common dialog box will appear.</span></span>

 

 
