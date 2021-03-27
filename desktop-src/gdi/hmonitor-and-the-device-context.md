---
description: Каждый физический дисплей представлен обработчиком монитора типа ХМОНИТОР.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: ХМОНИТОР и контекст устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997358"
---
# <a name="hmonitor-and-the-device-context"></a><span data-ttu-id="d5618-103">ХМОНИТОР и контекст устройства</span><span class="sxs-lookup"><span data-stu-id="d5618-103">HMONITOR and the Device Context</span></span>

<span data-ttu-id="d5618-104">Каждый физический дисплей представлен обработчиком монитора типа **хмонитор**.</span><span class="sxs-lookup"><span data-stu-id="d5618-104">Each physical display is represented by a monitor handle of type **HMONITOR**.</span></span> <span data-ttu-id="d5618-105">Допустимый **хмонитор** гарантированно не равен null.</span><span class="sxs-lookup"><span data-stu-id="d5618-105">A valid **HMONITOR** is guaranteed to be non-NULL.</span></span> <span data-ttu-id="d5618-106">Физический дисплей имеет тот же **хмонитор** , если он является частью рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="d5618-106">A physical display has the same **HMONITOR** as long as it is part of the desktop.</span></span> <span data-ttu-id="d5618-107">При отправке сообщения **WM \_ дисплайчанже** любой монитор может быть удален с рабочего стола, поэтому его **хмонитор** становится недопустимым или изменяется его параметры.</span><span class="sxs-lookup"><span data-stu-id="d5618-107">When a **WM\_DISPLAYCHANGE** message is sent, any monitor may be removed from the desktop and thus its **HMONITOR** becomes invalid or has its settings changed.</span></span> <span data-ttu-id="d5618-108">Поэтому приложение должно проверить, являются ли все **хмониторс** допустимыми при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5618-108">Therefore, an application should check whether all **HMONITORS** are valid when this message is sent.</span></span>

<span data-ttu-id="d5618-109">Любая функция, возвращающая контекст отображаемого устройства (DC), обычно возвращает контроллер домена для основного монитора.</span><span class="sxs-lookup"><span data-stu-id="d5618-109">Any function that returns a display device context (DC) normally returns a DC for the primary monitor.</span></span> <span data-ttu-id="d5618-110">Чтобы получить контроллер домена для другого монитора, используйте функцию [**енумдисплаймониторс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="d5618-110">To obtain the DC for another monitor, use the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span> <span data-ttu-id="d5618-111">Чтобы создать контроллер домена с [**креатедк**](/windows/desktop/api/Wingdi/nf-wingdi-createdca), можно использовать имя устройства из функции [**жетмониторинфо**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d5618-111">Or, you can use the device name from the [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) function to create a DC with [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="d5618-112">Однако если функция, например [**жетвиндовдк**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) или [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), получает контроллер домена для окна, охватывающего несколько дисплеев, контроллер домена также будет охватывать два отображения.</span><span class="sxs-lookup"><span data-stu-id="d5618-112">However, if the function, such as [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), gets a DC for a window that spans more than one display, the DC will also span the two displays.</span></span>

 

 



