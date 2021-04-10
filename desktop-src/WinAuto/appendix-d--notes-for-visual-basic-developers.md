---
title: Приложение г, заметки для Visual Basic разработчиков
description: В этом разделе содержатся сведения о Microsoft Active Accessibility для разработчиков Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986420"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a><span data-ttu-id="3091c-103">Приложение г. примечания для Visual Basic разработчиков</span><span class="sxs-lookup"><span data-stu-id="3091c-103">Appendix D: Notes for Visual Basic Developers</span></span>

<span data-ttu-id="3091c-104">В этом разделе содержатся сведения о Microsoft Active Accessibility для разработчиков Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3091c-104">This section provides information about Microsoft Active Accessibility for Microsoft Visual Basic developers.</span></span>

<span data-ttu-id="3091c-105">Приложения, написанные на Visual Basic, являются клиентами Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="3091c-105">Applications written in Visual Basic are Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="3091c-106">Они не предоставляют сведения о своих настраиваемых элементах пользовательского интерфейса, так как они не реализуют [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) или какой-либо другой интерфейс модели COM.</span><span class="sxs-lookup"><span data-stu-id="3091c-106">They do not provide information about their custom user interface elements because they do not implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or any other Component Object Model (COM) interface.</span></span>

<span data-ttu-id="3091c-107">В этой документации используются имена C/C++ для свойств [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ; Однако имена Visual Basic похожи.</span><span class="sxs-lookup"><span data-stu-id="3091c-107">This documentation uses the C/C++ names for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties; however, the Visual Basic names are similar.</span></span> <span data-ttu-id="3091c-108">Например, свойство [**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) будет называться **аккнаме** в приложении Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3091c-108">For example, the [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) property would be called **accName** in a Visual Basic application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3091c-109">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="3091c-109">In this section</span></span>

-   [<span data-ttu-id="3091c-110">Примечания к методу Visual Basic: Аккнаме</span><span class="sxs-lookup"><span data-stu-id="3091c-110">Visual Basic Method Notes: accName</span></span>](visual-basic-method-notes--accname.md)
-   [<span data-ttu-id="3091c-111">Примечания к методу Visual Basic: Акквалуе</span><span class="sxs-lookup"><span data-stu-id="3091c-111">Visual Basic Method Notes: accValue</span></span>](visual-basic-method-notes--accvalue.md)
-   [<span data-ttu-id="3091c-112">Visual Basic примеров программ</span><span class="sxs-lookup"><span data-stu-id="3091c-112">Visual Basic Sample Programs</span></span>](visual-basic-sample-programs.md)

 

 




