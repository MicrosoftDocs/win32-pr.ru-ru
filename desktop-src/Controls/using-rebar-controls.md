---
title: Использование элементов управления "Главная панель"
description: В этом разделе содержатся разделы, демонстрирующие создание и использование элементов управления главной панели.
ms.assetid: b821216f-609e-41a4-8d45-69609f3572bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9174a4ee05b966037bb30be3e796bcc2c3e00da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794029"
---
# <a name="using-rebar-controls"></a><span data-ttu-id="00d4d-103">Использование элементов управления "Главная панель"</span><span class="sxs-lookup"><span data-stu-id="00d4d-103">Using Rebar Controls</span></span>

<span data-ttu-id="00d4d-104">В этом разделе содержатся разделы, демонстрирующие создание и использование элементов управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="00d4d-104">This section contains topics that demonstrate how to create and use rebar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="00d4d-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="00d4d-105">In this section</span></span>



| <span data-ttu-id="00d4d-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="00d4d-106">Topic</span></span>                                                                | <span data-ttu-id="00d4d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="00d4d-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00d4d-108">Создание элементов управления "Главная панель"</span><span class="sxs-lookup"><span data-stu-id="00d4d-108">How to Create Rebar Controls</span></span>](create-rebar-controls.md)<br/> | <span data-ttu-id="00d4d-109">Приложение создает элемент управления главной панели путем вызова функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указывая [**ребаркласснаме**](common-control-window-classes.md) в качестве класса Window.</span><span class="sxs-lookup"><span data-stu-id="00d4d-109">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="00d4d-110">Приложение должно сначала зарегистрировать класс окна, вызвав функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , указав \_ бит замечательных классов ICC \_ в сопровождающей структуре [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="00d4d-110">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span> <br/> |



 

 

