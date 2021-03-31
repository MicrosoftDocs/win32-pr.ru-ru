---
title: Свойства окружения для элементов управления
description: Свойства окружения для элементов управления
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411071"
---
# <a name="ambient-properties-for-controls"></a><span data-ttu-id="a2330-103">Свойства окружения для элементов управления</span><span class="sxs-lookup"><span data-stu-id="a2330-103">Ambient Properties for Controls</span></span>

<span data-ttu-id="a2330-104">Если элемент управления поддерживает все свойства окружения, он должен по крайней мере учитывать значения следующих внешних свойств в условиях, указанных в следующей таблице, используя стандартные идентификаторы DISPID.</span><span class="sxs-lookup"><span data-stu-id="a2330-104">If a control supports any ambient properties at all, it must at least respect the values of the following ambient properties under the conditions stated in the following table using the standard dispids.</span></span>



| <span data-ttu-id="a2330-105">Внешнее свойство</span><span class="sxs-lookup"><span data-stu-id="a2330-105">Ambient Property</span></span>            | <span data-ttu-id="a2330-106">DISPID</span><span class="sxs-lookup"><span data-stu-id="a2330-106">Dispid</span></span>          | <span data-ttu-id="a2330-107">Комментарии и условия использования</span><span class="sxs-lookup"><span data-stu-id="a2330-107">Comment/Conditions for Use</span></span>                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2330-108">LocaleID</span><span class="sxs-lookup"><span data-stu-id="a2330-108">LocaleID</span></span><br/>         | <span data-ttu-id="a2330-109">— 705</span><span class="sxs-lookup"><span data-stu-id="a2330-109">-705</span></span><br/> | <span data-ttu-id="a2330-110">Если языковой стандарт важен для элемента управления, например для вывода текста</span><span class="sxs-lookup"><span data-stu-id="a2330-110">If Locale is significant to the control, e.g. for text output</span></span><br/>                                                                                                                                                                                                                  |
| <span data-ttu-id="a2330-111">Пользовательском</span><span class="sxs-lookup"><span data-stu-id="a2330-111">UserMode</span></span> <br/>        | <span data-ttu-id="a2330-112">— 709</span><span class="sxs-lookup"><span data-stu-id="a2330-112">-709</span></span><br/> | <span data-ttu-id="a2330-113">Если элемент управления ведет себя иначе в режиме пользователя (конструктора) и в режиме выполнения</span><span class="sxs-lookup"><span data-stu-id="a2330-113">If the control behaves differently in user (design) mode and run mode</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="a2330-114">уидеад</span><span class="sxs-lookup"><span data-stu-id="a2330-114">UIDead</span></span><br/>           | <span data-ttu-id="a2330-115">— 710</span><span class="sxs-lookup"><span data-stu-id="a2330-115">-710</span></span><br/> | <span data-ttu-id="a2330-116">Если элемент управления реагирует на события пользовательского интерфейса, он должен учитывать это внешнее свойство.</span><span class="sxs-lookup"><span data-stu-id="a2330-116">If the control reacts to UI events, then it should honor this ambient property</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="a2330-117">шовграбхандлес</span><span class="sxs-lookup"><span data-stu-id="a2330-117">ShowGrabHandles</span></span><br/>  | <span data-ttu-id="a2330-118">— 711</span><span class="sxs-lookup"><span data-stu-id="a2330-118">-711</span></span><br/> | <span data-ttu-id="a2330-119">Если элемент управления поддерживает изменение размера по месту самого себя</span><span class="sxs-lookup"><span data-stu-id="a2330-119">If the control support in-place resizing of itself</span></span><br/>                                                                                                                                                                                                                             |
| <span data-ttu-id="a2330-120">шовхатчинг</span><span class="sxs-lookup"><span data-stu-id="a2330-120">ShowHatching</span></span><br/>     | <span data-ttu-id="a2330-121">— 712</span><span class="sxs-lookup"><span data-stu-id="a2330-121">-712</span></span><br/> | <span data-ttu-id="a2330-122">Если элемент управления поддерживает активацию на месте и активацию пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a2330-122">If the control support in-place activation and UI activation</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="a2330-123">DisplayAsDefault</span><span class="sxs-lookup"><span data-stu-id="a2330-123">DisplayAsDefault</span></span><br/> | <span data-ttu-id="a2330-124">— 713</span><span class="sxs-lookup"><span data-stu-id="a2330-124">-713</span></span><br/> | <span data-ttu-id="a2330-125">Только в том случае, если элемент управления помечен как ОЛЕМИСК \_ актсликебуттон (что означает, что поддерживается поддержка назначенных клавиш клавиатуры, поэтому необходимо реализовать [**метод интерфейса IOleControl:: Жетконтролинфо**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) и [**метод интерфейса IOleControl:: OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) ).</span><span class="sxs-lookup"><span data-stu-id="a2330-125">Only if the control is marked OLEMISC\_ACTSLIKEBUTTON (which means that support for keyboard mnemonics is provided, thus [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) must be implemented).</span></span><br/> |



 

<span data-ttu-id="a2330-126">Как было сказано ранее, для использования внешних элементов требуется как минимум [**метод интерфейса IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) ( [**онамбиентпропертичанже**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) ), так и [**Иолеобжект**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (для [**сетклиентсите**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) и [**жетклиентсите**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span><span class="sxs-lookup"><span data-stu-id="a2330-126">As described previously, use of ambients requires both [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (for [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) as a minimum) as well as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (for [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) and [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span></span>

<span data-ttu-id="a2330-127">ОЛЕМИСК \_ сетклиентситефирст bit не обязательно поддерживаться контейнером.</span><span class="sxs-lookup"><span data-stu-id="a2330-127">The OLEMISC\_SETCLIENTSITEFIRST bit may not necessarily be supported by a container.</span></span> <span data-ttu-id="a2330-128">В таких случаях элемент управления должен отсортировать значения по умолчанию для требуемых внешних свойств.</span><span class="sxs-lookup"><span data-stu-id="a2330-128">In these circumstances, a control must resort to default values for the ambient properties that it requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2330-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a2330-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2330-130">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="a2330-130">Controls</span></span>](controls.md)
</dt> </dl>

 

 





