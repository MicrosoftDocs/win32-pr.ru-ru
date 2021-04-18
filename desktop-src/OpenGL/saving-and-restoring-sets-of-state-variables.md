---
title: Сохранение и восстановление наборов переменных состояния
description: Можно сохранить и восстановить значения коллекции переменных состояния в стеке атрибутов с помощью функций Глпушаттриб и Глпопаттриб.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Переменные состояния OpenGL
- сохранение переменных состояния OpenGL
- восстановление переменных состояния OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661593"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a><span data-ttu-id="a1a84-106">Сохранение и восстановление наборов переменных состояния</span><span class="sxs-lookup"><span data-stu-id="a1a84-106">Saving and Restoring Sets of State Variables</span></span>

<span data-ttu-id="a1a84-107">Можно сохранить и восстановить значения коллекции переменных состояния в стеке атрибутов с помощью функций [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="a1a84-107">You can save and restore the values of a collection of state variables on an attribute stack with the [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) functions.</span></span> <span data-ttu-id="a1a84-108">Стек атрибутов имеет глубину не менее 16.</span><span class="sxs-lookup"><span data-stu-id="a1a84-108">The attribute stack has a depth of at least 16.</span></span> <span data-ttu-id="a1a84-109">Чтобы получить реальную глубину, используйте \_ параметр GL "максимальная \_ \_ глубина стека" \_ с [**глжетинтежерв**](glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="a1a84-109">To obtain the actual depth, use GL\_MAX\_ATTRIB\_STACK\_DEPTH with [**glGetIntegerv**](glgetintegerv.md).</span></span> <span data-ttu-id="a1a84-110">При принудительной отправке полного стека или извлечении пустого элемента возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a1a84-110">Pushing a full stack or popping an empty one generates an error.</span></span>

<span data-ttu-id="a1a84-111">Обычно быстрее использовать **глпушаттриб** и **глпопаттриб** , чем получать и восстанавливать значения самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="a1a84-111">It is generally faster to use **glPushAttrib** and **glPopAttrib** than to get and restore the values yourself.</span></span> <span data-ttu-id="a1a84-112">Некоторые значения могут быть отправлены и извлечены на оборудовании, а сохранение и восстановление ресурсов могут быть ресурсоемкими.</span><span class="sxs-lookup"><span data-stu-id="a1a84-112">Some values might be pushed and popped in the hardware, and saving and restoring them can be resource-intensive.</span></span> <span data-ttu-id="a1a84-113">Кроме того, если вы работаете на удаленном клиенте, все данные атрибутов должны передаваться по сетевому подключению и обратно по мере их сохранения и восстановления.</span><span class="sxs-lookup"><span data-stu-id="a1a84-113">Also, if you're operating on a remote client, all of the attribute data must be transferred across the network connection and back as it is saved and restored.</span></span> <span data-ttu-id="a1a84-114">Однако реализация OpenGL сохраняет стек атрибутов на сервере, избегая ненужных сетевых задержек.</span><span class="sxs-lookup"><span data-stu-id="a1a84-114">However, your OpenGL implementation keeps the attribute stack on the server, avoiding unnecessary network delays.</span></span>

<span data-ttu-id="a1a84-115">Прототип **глпушаттриб** :</span><span class="sxs-lookup"><span data-stu-id="a1a84-115">The prototype of **glPushAttrib** is:</span></span>

<span data-ttu-id="a1a84-116">**void** **глпушаттриб**( *Маска* глбитфиелд);</span><span class="sxs-lookup"><span data-stu-id="a1a84-116">**void** **glPushAttrib**(**GLbitfield** *mask* );</span></span>

<span data-ttu-id="a1a84-117">Использование [**глпушаттриб**](glpushattrib.md) сохраняет все атрибуты, обозначенные битами в *маске* , помещая их в стек атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a1a84-117">Using [**glPushAttrib**](glpushattrib.md) saves all the attributes indicated by bits in *mask* by pushing them onto the attribute stack.</span></span> <span data-ttu-id="a1a84-118">Список возможных бит маски, которые можно логически или объединить для сохранения любых сочетаний атрибутов, см. в разделе [группы атрибутов](attribute-groups.md).</span><span class="sxs-lookup"><span data-stu-id="a1a84-118">For a list of the possible mask bits you can logically OR together to save any combination of attributes, see [Attribute Groups](attribute-groups.md).</span></span> <span data-ttu-id="a1a84-119">Каждый бит соответствует коллекции отдельных переменных состояния.</span><span class="sxs-lookup"><span data-stu-id="a1a84-119">Each bit corresponds to a collection of individual state variables.</span></span> <span data-ttu-id="a1a84-120">Например, \_ бит освещения GL \_ относится ко всем переменным состояния, связанным с освещением, в том числе к текущему цвету материала, внешнему, диффузию, отражению и порожденному освещению; список включенных огней, а также направления прожекторов.</span><span class="sxs-lookup"><span data-stu-id="a1a84-120">For example, GL\_LIGHTING\_BIT refers to all the state variables related to lighting, which include the current material color; the ambient, diffuse, specular, and emitted light; a list of the lights that are enabled; and the directions of the spotlights.</span></span> <span data-ttu-id="a1a84-121">При вызове [**глпопаттриб**](glpopattrib.md)восстанавливаются все эти переменные.</span><span class="sxs-lookup"><span data-stu-id="a1a84-121">When you call [**glPopAttrib**](glpopattrib.md), all those variables are restored.</span></span> <span data-ttu-id="a1a84-122">Сведения о том, какие атрибуты сохраняются для определенных значений маски, см. в разделе [переменные состояния OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="a1a84-122">To find out exactly which attributes are saved for particular mask values, see [OpenGL State Variables](opengl-state-variables.md).</span></span>

 

 




