---
description: Управление схемами управления питанием
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Управление схемами управления питанием
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663116"
---
# <a name="power-scheme-management"></a><span data-ttu-id="69762-103">Управление схемами управления питанием</span><span class="sxs-lookup"><span data-stu-id="69762-103">Power Scheme Management</span></span>

<span data-ttu-id="69762-104">Каждая схема управления питанием уникально идентифицируется по **идентификатору GUID**.</span><span class="sxs-lookup"><span data-stu-id="69762-104">Each power scheme is uniquely identified by a **GUID**.</span></span> <span data-ttu-id="69762-105">Чтобы перечислить все доступные схемы управления питанием, используйте функцию [**поверенумерате**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) .</span><span class="sxs-lookup"><span data-stu-id="69762-105">To enumerate all available power schemes, use the [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) function.</span></span> <span data-ttu-id="69762-106">**Поверенумерате** также можно использовать для получения всех параметров управления питанием для указанной схемы.</span><span class="sxs-lookup"><span data-stu-id="69762-106">**PowerEnumerate** can also be used to retrieve all of the power settings for a specified scheme.</span></span>

<span data-ttu-id="69762-107">Схема управления питанием, используемая в данный момент в системе, называется активной схемой управления питанием или планом.</span><span class="sxs-lookup"><span data-stu-id="69762-107">The power scheme that is currently in use on the system is called the active power scheme or plan.</span></span> <span data-ttu-id="69762-108">Чтобы получить **идентификатор GUID** активного плана, вызовите функцию [**повержетактивесчеме**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="69762-108">To retrieve the **GUID** of the active plan, call the [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) function.</span></span> <span data-ttu-id="69762-109">Чтобы изменить активную схему управления питанием, вызовите функцию [**поверсетактивесчеме**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="69762-109">To change the active power plan, call the [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) function.</span></span>

<span data-ttu-id="69762-110">Чтобы создать схему управления питанием, сначала необходимо скопировать существующую схему с помощью функции [**повердупликатесчеме**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) , указав **идентификатор GUID** схемы, на основе которой вы хотите создать новую схему.</span><span class="sxs-lookup"><span data-stu-id="69762-110">To create a power scheme, you need to first duplicate an existing scheme by using the [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) function, specifying the **GUID** of the scheme you wish to base your new scheme upon.</span></span> <span data-ttu-id="69762-111">Необходимо скопировать одну из встроенных схем и изменить параметры управления питанием в отношении ваших потребностей.</span><span class="sxs-lookup"><span data-stu-id="69762-111">You should copy one of the built-in schemes and modify the power settings to your needs.</span></span> <span data-ttu-id="69762-112">Обратите внимание, что создание схемы управления питанием не приводит к автоматическому обновлению активной схемы управления питанием.</span><span class="sxs-lookup"><span data-stu-id="69762-112">Note that creating a power plan does not automatically update the active power plan.</span></span> <span data-ttu-id="69762-113">Для обновления активной схемы управления питанием необходимо всегда вызывать [**поверсетактивесчеме**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="69762-113">You must always call [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) to update the active power plan.</span></span> <span data-ttu-id="69762-114">Существующие схемы управления питанием можно изменить, а затем применить таким же образом.</span><span class="sxs-lookup"><span data-stu-id="69762-114">Existing power plans can be modified and then applied in the same manner.</span></span>

<span data-ttu-id="69762-115">Чтобы удалить схему управления питанием, вызовите функцию [**поверделетесчеме**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) .</span><span class="sxs-lookup"><span data-stu-id="69762-115">To remove a power plan, call the [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) function.</span></span>

> [!Note]  
> <span data-ttu-id="69762-116">Чтобы получить дополнительные сведения о состоянии энергопотребления системы, вызовите функцию [**каллнтповеринформатион**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) .</span><span class="sxs-lookup"><span data-stu-id="69762-116">To retrieve additional information about the system power state, call the [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="69762-117">См. также</span><span class="sxs-lookup"><span data-stu-id="69762-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69762-118">Схемы управления питанием</span><span class="sxs-lookup"><span data-stu-id="69762-118">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 



