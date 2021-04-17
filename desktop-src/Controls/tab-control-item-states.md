---
title: Состояния элементов элемента управления Tab (Коммктрл. h)
description: Элементы управления вкладки теперь поддерживают состояние элемента для поддержки \_ сообщения TCM деселекталл. Кроме того, структура ТЦИТЕМ поддерживает значения состояния элементов.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657193"
---
# <a name="tab-control-item-states"></a><span data-ttu-id="86909-104">Состояния элементов элемента управления Tab</span><span class="sxs-lookup"><span data-stu-id="86909-104">Tab Control Item States</span></span>

<span data-ttu-id="86909-105">Элементы управления вкладки теперь поддерживают состояние элемента для поддержки сообщения [**TCM \_ деселекталл**](tcm-deselectall.md) .</span><span class="sxs-lookup"><span data-stu-id="86909-105">Tab control items now support an item state to support the [**TCM\_DESELECTALL**](tcm-deselectall.md) message.</span></span> <span data-ttu-id="86909-106">Кроме того, структура [**тЦитем**](/windows/win32/api/commctrl/ns-commctrl-tcitema) поддерживает значения состояния элементов.</span><span class="sxs-lookup"><span data-stu-id="86909-106">Additionally, the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure supports item state values.</span></span>



| <span data-ttu-id="86909-107">Константа</span><span class="sxs-lookup"><span data-stu-id="86909-107">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="86909-108">Описание</span><span class="sxs-lookup"><span data-stu-id="86909-108">Description</span></span>                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <span data-ttu-id="86909-109"><dt>**ТЦИС \_ буттонпрессед**</dt></span><span class="sxs-lookup"><span data-stu-id="86909-109"><dt>**TCIS\_BUTTONPRESSED**</dt></span></span> </dl> | <span data-ttu-id="86909-110">[Версия 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="86909-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="86909-111">Элемент управления вкладки выбран.</span><span class="sxs-lookup"><span data-stu-id="86909-111">The tab control item is selected.</span></span> <span data-ttu-id="86909-112">Это состояние имеет смысл только в том случае, если установлен флаг стиля [**TCS \_ Buttons**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="86909-112">This state is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span><br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <span data-ttu-id="86909-113"><dt>**\_выделенный тЦис**</dt></span><span class="sxs-lookup"><span data-stu-id="86909-113"><dt>**TCIS\_HIGHLIGHTED**</dt></span></span> </dl>       | <span data-ttu-id="86909-114">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="86909-114">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="86909-115">Элемент управления вкладки выделяется, а вкладка и текст рисуются с использованием текущего цвета выделения.</span><span class="sxs-lookup"><span data-stu-id="86909-115">The tab control item is highlighted, and the tab and text are drawn using the current highlight color.</span></span> <span data-ttu-id="86909-116">При использовании высокого цвета это будет истинной интерполяцией, а не с неконтрастным цветом.</span><span class="sxs-lookup"><span data-stu-id="86909-116">When using high-color, this will be a true interpolation, not a dithered color.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="86909-117">Требования</span><span class="sxs-lookup"><span data-stu-id="86909-117">Requirements</span></span>



| <span data-ttu-id="86909-118">Требование</span><span class="sxs-lookup"><span data-stu-id="86909-118">Requirement</span></span> | <span data-ttu-id="86909-119">Значение</span><span class="sxs-lookup"><span data-stu-id="86909-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86909-120">Header</span><span class="sxs-lookup"><span data-stu-id="86909-120">Header</span></span><br/> | <dl> <span data-ttu-id="86909-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="86909-121"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





