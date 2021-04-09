---
title: Заголовок ACF
description: Заголовок ACF содержит зависящие от платформы атрибуты, которые применяются к интерфейсу в целом. Атрибуты, применяемые к отдельным типам и функциям в теле ACF, переопределяют атрибуты в заголовке ACF. В заголовке ACF атрибуты не требуются.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070283"
---
# <a name="the-acf-header"></a><span data-ttu-id="65add-105">Заголовок ACF</span><span class="sxs-lookup"><span data-stu-id="65add-105">The ACF Header</span></span>

<span data-ttu-id="65add-106">Заголовок ACF содержит зависящие от платформы атрибуты, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="65add-106">The ACF header contains platform-specific attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="65add-107">Атрибуты, применяемые к отдельным типам и функциям в теле ACF, переопределяют атрибуты в заголовке ACF.</span><span class="sxs-lookup"><span data-stu-id="65add-107">Attributes applied to individual types and functions in the ACF body override the attributes in the ACF header.</span></span> <span data-ttu-id="65add-108">В заголовке ACF атрибуты не требуются.</span><span class="sxs-lookup"><span data-stu-id="65add-108">No attributes are required in the ACF header.</span></span>

<span data-ttu-id="65add-109">Заголовок ACF может включать один из следующих атрибутов: **\[** [**Auto \_ Handle**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**неявный \_ обработчик**](/windows/desktop/Midl/implicit-handle) **\]** или [**явный \_ обработчик**](/windows/desktop/Midl/explicit-handle) **\]** .</span><span class="sxs-lookup"><span data-stu-id="65add-109">The ACF header can include one of the following attributes: **\[**[**auto\_handle**](/windows/desktop/Midl/auto-handle)**\]**, **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]**, or [**explicit\_handle**](/windows/desktop/Midl/explicit-handle)**\]**.</span></span> <span data-ttu-id="65add-110">Если используется **\[ автоматически \_ обрабатываемый \]** или **\[ неявный \_ Handle \]** , он указывает тип маркера привязки, который будет использоваться для привязки, если Удаленная функция не имеет явного параметра обработчика привязки.</span><span class="sxs-lookup"><span data-stu-id="65add-110">If **\[auto\_handle\]** or **\[implicit\_handle\]** is used, it specifies the type of binding handle that will be used for binding when a remote function does not have an explicit binding-handle parameter.</span></span> <span data-ttu-id="65add-111">Если ACF отсутствует или не указывает автоматический, неявный или явный маркер привязки, MIDL использует **\[ автоматическую \_ обработку \]** для неявной привязки.</span><span class="sxs-lookup"><span data-stu-id="65add-111">When the ACF is not present or does not specify an automatic, implicit, or explicit binding handle, MIDL uses **\[auto\_handle\]** for implicit binding.</span></span>

<span data-ttu-id="65add-112">**\[** [](/windows/desktop/Midl/code) **\]** **\[** [](/windows/desktop/Midl/nocode) **\]** В заголовке интерфейса могут отображаться либо код, либо код "только один раз".</span><span class="sxs-lookup"><span data-stu-id="65add-112">Either **\[**[**code**](/windows/desktop/Midl/code)**\]** or **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]** can appear in the interface header, but the one you choose can appear only once.</span></span> <span data-ttu-id="65add-113">Если ни один из атрибутов не указан, компилятор по умолчанию использует **\[ код \]** .</span><span class="sxs-lookup"><span data-stu-id="65add-113">When neither attribute is present, the compiler uses **\[code\]** as a default.</span></span>

<span data-ttu-id="65add-114">Дополнительные сведения см. в разделе [атрибуты ACF](/windows/desktop/Midl/acf-attributes).</span><span class="sxs-lookup"><span data-stu-id="65add-114">For more information, see [ACF Attributes](/windows/desktop/Midl/acf-attributes).</span></span>

 

 