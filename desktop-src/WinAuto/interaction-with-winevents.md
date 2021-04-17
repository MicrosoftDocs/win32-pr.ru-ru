---
title: Взаимодействие с Виневентс
description: Динамическое время выполнения заметки не будет отсылать Виневентс; ответственность за отправку соответствующих событий при необходимости является обязанностью аннотации. Если необходимо отправить Виневентс, не забудьте отправить их после заметки.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aedd09a22371f91a92eca891c77f6c424583b5
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "105710225"
---
# <a name="interaction-with-winevents"></a><span data-ttu-id="c66c9-104">Взаимодействие с Виневентс</span><span class="sxs-lookup"><span data-stu-id="c66c9-104">Interaction with WinEvents</span></span>

<span data-ttu-id="c66c9-105">Динамическое время выполнения заметки не будет отсылать [виневентс](winevents-infrastructure.md); ответственность за отправку соответствующих событий при необходимости является обязанностью аннотации.</span><span class="sxs-lookup"><span data-stu-id="c66c9-105">The Dynamic Annotation run time will not send [WinEvents](winevents-infrastructure.md); it is the annotator's responsibility to send appropriate events, when necessary.</span></span> <span data-ttu-id="c66c9-106">Если необходимо отправить Виневентс, не забудьте отправить их после заметки.</span><span class="sxs-lookup"><span data-stu-id="c66c9-106">If you need to send WinEvents, be sure to send them after the annotation has taken place.</span></span>

<span data-ttu-id="c66c9-107">Например, если вы используете [**иаккпропсервицес:: сетпропвалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) , чтобы задать свойство [**Name**](name-property.md) элемента, отправьте событие [**\_ \_ NAMECHANGE объекта события**](event-constants.md) для этого объекта после того, как **сетпропвалуе** возвратит значение.</span><span class="sxs-lookup"><span data-stu-id="c66c9-107">For example, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the [**Name**](name-property.md) property of an element, send an [**EVENT\_OBJECT\_NAMECHANGE**](event-constants.md) event for that object after **SetPropValue** returns.</span></span>

<span data-ttu-id="c66c9-108">Однако при использовании [**иаккпропсервицес:: сетпропвалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) для задания ValueMap для ползунка никаких событий не требуется, так как настройка ValueMap не изменяет значение ползунка.</span><span class="sxs-lookup"><span data-stu-id="c66c9-108">However, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the ValueMap for a slider, no events are required because setting the ValueMap does not change the slider's value.</span></span>

 

 




