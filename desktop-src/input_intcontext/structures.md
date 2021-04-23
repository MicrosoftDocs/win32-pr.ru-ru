---
title: Структуры контекста взаимодействия
description: В подразделах этого раздела приведены справочные спецификации по структурам контекста взаимодействия.
ms.assetid: 38C5CE85-405B-455F-809D-19C77B8A217B
keywords:
- взаимодействие с пользователем
- input
- указатель
- Сенсорный ввод
- Мышь
- Перо
- перо
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 975b1342c681d4d154ba31d31348e13063c9fc88
ms.sourcegitcommit: 6b8d5058d02daacad4d2ed7830da63b63a509586
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/07/2020
ms.locfileid: "104412411"
---
# <a name="interaction-context-structures"></a><span data-ttu-id="06d4d-110">Структуры контекста взаимодействия</span><span class="sxs-lookup"><span data-stu-id="06d4d-110">Interaction Context Structures</span></span>

<span data-ttu-id="06d4d-111">В подразделах этого раздела приведены справочные спецификации по структурам [контекста взаимодействия](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="06d4d-111">The topics in this section provide the reference specifications for [Interaction Context](interaction-context-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="06d4d-112">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="06d4d-112">In this section</span></span>

| <span data-ttu-id="06d4d-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="06d4d-113">Topic</span></span> | <span data-ttu-id="06d4d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="06d4d-114">Description</span></span> |
|---|---|
| [<span data-ttu-id="06d4d-115">**параметр "перекрестный \_ слайд" \_**</span><span class="sxs-lookup"><span data-stu-id="06d4d-115">**CROSS\_SLIDE\_PARAMETER**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-cross_slide_parameter)<br/>                           | <span data-ttu-id="06d4d-116">Определяет порог между слайдами и его пороговое значение расстояния.</span><span class="sxs-lookup"><span data-stu-id="06d4d-116">Defines the cross-slide threshold and its distance threshold.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="06d4d-117">**аргументы взаимодействия в \_ \_ разных \_ слайдах**</span><span class="sxs-lookup"><span data-stu-id="06d4d-117">**INTERACTION\_ARGUMENTS\_CROSS\_SLIDE**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_cross_slide)<br/>  | <span data-ttu-id="06d4d-118">Определяет состояние взаимодействия между слайдами.</span><span class="sxs-lookup"><span data-stu-id="06d4d-118">Defines the state of the cross-slide interaction.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="06d4d-119">**\_Управление аргументами взаимодействия \_**</span><span class="sxs-lookup"><span data-stu-id="06d4d-119">**INTERACTION\_ARGUMENTS\_MANIPULATION**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_manipulation)<br/> | <span data-ttu-id="06d4d-120">Определяет состояние манипуляции.</span><span class="sxs-lookup"><span data-stu-id="06d4d-120">Defines the state of a manipulation.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="06d4d-121">**\_аргументы взаимодействия \_ TAP**</span><span class="sxs-lookup"><span data-stu-id="06d4d-121">**INTERACTION\_ARGUMENTS\_TAP**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_tap)<br/>                   | <span data-ttu-id="06d4d-122">Определяет состояние взаимодействия касания.</span><span class="sxs-lookup"><span data-stu-id="06d4d-122">Defines the state of the tap interaction.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="06d4d-123">**\_Конфигурация контекста \_ взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="06d4d-123">**INTERACTION\_CONTEXT\_CONFIGURATION**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_context_configuration)<br/>   | <span data-ttu-id="06d4d-124">Определяет конфигурацию объекта [контекста взаимодействия](interaction-context-portal.md) , который включает, отключает или изменяет поведение взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="06d4d-124">Defines the configuration of an [Interaction Context](interaction-context-portal.md) object that enables, disables, or modifies the behavior of an interaction.</span></span><br/> |
| [<span data-ttu-id="06d4d-125">**\_ \_ выходные данные контекста взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="06d4d-125">**INTERACTION\_CONTEXT\_OUTPUT**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_context_output)<br/>                 | <span data-ttu-id="06d4d-126">Определяет выходные данные объекта [контекста взаимодействия](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="06d4d-126">Defines the output of the [Interaction Context](interaction-context-portal.md) object.</span></span><br/>                                                                          |
| [<span data-ttu-id="06d4d-127">**Преобразование МАНИПУЛЯЦИи \_**</span><span class="sxs-lookup"><span data-stu-id="06d4d-127">**MANIPULATION\_TRANSFORM**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-manipulation_transform)<br/>                          | <span data-ttu-id="06d4d-128">Определяет данные преобразования для манипуляции.</span><span class="sxs-lookup"><span data-stu-id="06d4d-128">Defines the transformation data for a manipulation.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="06d4d-129">**скорость МАНИПУЛЯЦИи \_**</span><span class="sxs-lookup"><span data-stu-id="06d4d-129">**MANIPULATION\_VELOCITY**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-manipulation_velocity)<br/>                            | <span data-ttu-id="06d4d-130">Определяет скорость обработки данных.</span><span class="sxs-lookup"><span data-stu-id="06d4d-130">Defines the velocity data of a manipulation.</span></span><br/>                                                                                                                     |
## <a name="related-topics"></a><span data-ttu-id="06d4d-131">См. также</span><span class="sxs-lookup"><span data-stu-id="06d4d-131">Related topics</span></span>

[<span data-ttu-id="06d4d-132">Взаимодействие с пользователем</span><span class="sxs-lookup"><span data-stu-id="06d4d-132">User Interaction</span></span>](../user-interaction.md)
