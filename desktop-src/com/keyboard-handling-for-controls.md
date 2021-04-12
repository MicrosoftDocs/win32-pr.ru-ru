---
title: Обработка клавиатуры для элементов управления
description: Элемент управления реагирует на сочетания клавиш, чтобы конечный пользователь мог инициировать действия, выполняемые элементом управления.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332496"
---
# <a name="keyboard-handling-for-controls"></a><span data-ttu-id="5cf24-103">Обработка клавиатуры для элементов управления</span><span class="sxs-lookup"><span data-stu-id="5cf24-103">Keyboard Handling for Controls</span></span>

<span data-ttu-id="5cf24-104">Элемент управления реагирует на сочетания клавиш, чтобы конечный пользователь мог инициировать действия, выполняемые элементом управления.</span><span class="sxs-lookup"><span data-stu-id="5cf24-104">A control responds to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="5cf24-105">Контейнер управляет работой клавиатуры для всех его внедренных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="5cf24-105">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="5cf24-106">При работе с составными документами сочетания клавиш применяются только к текущему активному объекту.</span><span class="sxs-lookup"><span data-stu-id="5cf24-106">With compound documents, keyboard accelerators apply only to the currently active object.</span></span> <span data-ttu-id="5cf24-107">С помощью элементов управления был добавлен механизм, позволяющий элементу управления реагировать на назначенные ему сочетания клавиш, даже если он не активен в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="5cf24-107">With controls, a mechanism has been added so that a control can respond to its keyboard mnemonics even if it is not currently UI-active.</span></span>

<span data-ttu-id="5cf24-108">Методы [**метод интерфейса IOleControl:: жетконтролинфо**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) и [**метод интерфейса IOleControl:: OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) , а также метод [**IOleControlSite:: онконтролинфочанжед**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) обрабатывали назначенные клавиши клавиатуры элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5cf24-108">The [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) methods and the [**IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) method handle a control's keyboard mnemonics.</span></span> <span data-ttu-id="5cf24-109">Структура [**контролинфо**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) описывает назначенные сочетания клавиш для элемента управления, а флаги, передаваемые обратно с помощью метода **жетконтролинфо** , описывают поведение элементов управления с помощью клавиш Enter и ESC.</span><span class="sxs-lookup"><span data-stu-id="5cf24-109">A [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) structure describes a control's mnemonic accelerators, and the flags passed back with it through the **GetControlInfo** method describe the controls behavior with the Enter and Esc keys.</span></span> <span data-ttu-id="5cf24-110">Когда элемент управления изменяет свои назначенные клавиши, он вызывает **онконтролинфочанжед** , чтобы контейнер мог перезагрузить структуру при необходимости.</span><span class="sxs-lookup"><span data-stu-id="5cf24-110">When a control changes its mnemonics, it calls **OnControlInfoChanged** so the container can reload the structure if necessary.</span></span>

<span data-ttu-id="5cf24-111">Если элемент управления активен в пользовательском интерфейсе, он также является элементом управления с фокусом.</span><span class="sxs-lookup"><span data-stu-id="5cf24-111">When a control is UI active, it is also the control with the focus.</span></span> <span data-ttu-id="5cf24-112">По мере активации и деактивации элементов управления между активными и активными состояниями пользовательского интерфейса элемент управления вызывает [**IOleControlSite:: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) , чтобы сообщить контейнеру об этих изменениях.</span><span class="sxs-lookup"><span data-stu-id="5cf24-112">As controls are activated and deactivated between the in-place active and the UI active states, the control calls [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) to tell the container of such changes.</span></span>

<span data-ttu-id="5cf24-113">Кроме того, если элемент управления активен в пользовательском интерфейсе, он получит первый шанс обработать все нажатия клавиш.</span><span class="sxs-lookup"><span data-stu-id="5cf24-113">In addition, when a control is UI active, it will have first chance to process any keystrokes.</span></span> <span data-ttu-id="5cf24-114">Чтобы предоставить контейнеру возможность обработать нажатие клавиши до элемента управления, элемент управления вызывает [**IOleControlSite:: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span><span class="sxs-lookup"><span data-stu-id="5cf24-114">To give a container the opportunity to process the keystroke before the control, the control calls [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span></span> <span data-ttu-id="5cf24-115">Если контейнер не обрабатывает нажатие клавиш, элемент управления обрабатывает его.</span><span class="sxs-lookup"><span data-stu-id="5cf24-115">If the container does not handle the keystroke, the control then processes it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cf24-116">См. также</span><span class="sxs-lookup"><span data-stu-id="5cf24-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cf24-117">Элементы управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="5cf24-117">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




