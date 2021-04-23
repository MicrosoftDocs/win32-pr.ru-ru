---
title: Активное свойство
description: Активное свойство
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253267"
---
# <a name="active-property"></a><span data-ttu-id="ff3a8-103">Активное свойство</span><span class="sxs-lookup"><span data-stu-id="ff3a8-103">Active Property</span></span>

<span data-ttu-id="ff3a8-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ff3a8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ff3a8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="ff3a8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ff3a8-106">Возвращает значение, указывающее, является ли приложение активным клиентом символа и является ли он верхним.</span><span class="sxs-lookup"><span data-stu-id="ff3a8-106">Returns whether your application is the active client of the character and whether the character is topmost.</span></span>

</dd> <dt>

<span data-ttu-id="ff3a8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="ff3a8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ff3a8-108">\*агент. ***Символы \* \* \* \* ("*** чарактерид \* \* *"). Активное* \*  \[  =  *состояние*\]</span><span class="sxs-lookup"><span data-stu-id="ff3a8-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Active** \[ = *State*\]</span></span>



| <span data-ttu-id="ff3a8-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="ff3a8-109">Part</span></span>    | <span data-ttu-id="ff3a8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3a8-110">Description</span></span>                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3a8-111">*state*</span><span class="sxs-lookup"><span data-stu-id="ff3a8-111">*state*</span></span> | <span data-ttu-id="ff3a8-112">Целочисленное выражение, указывающее состояние клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ff3a8-112">An integer expression specifying the state of your client application.</span></span> <span data-ttu-id="ff3a8-113">0 — не активный клиент.</span><span class="sxs-lookup"><span data-stu-id="ff3a8-113">0 Not the active client.</span></span><br/> <span data-ttu-id="ff3a8-114">1 активный клиент.</span><span class="sxs-lookup"><span data-stu-id="ff3a8-114">1 The active client.</span></span> <br/> <span data-ttu-id="ff3a8-115">2. Клиент ввода-активного.</span><span class="sxs-lookup"><span data-stu-id="ff3a8-115">2 The input-active client.</span></span> <span data-ttu-id="ff3a8-116">(Самый верхний символ.)</span><span class="sxs-lookup"><span data-stu-id="ff3a8-116">(The topmost character.)</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff3a8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff3a8-117">Remarks</span></span>

<span data-ttu-id="ff3a8-118">Если несколько клиентских приложений совместно используют один и тот же символ, то активный клиент символа получает ввод с помощью мыши (например, элемент управления агента Microsoft Agent [**Click**](click-event.md) или [драгстарт](dragstart-event.md) Events).</span><span class="sxs-lookup"><span data-stu-id="ff3a8-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control [**Click**](click-event.md) or [DragStart](dragstart-event.md) events).</span></span> <span data-ttu-id="ff3a8-119">Аналогично, когда отображается несколько символов, активный клиент самого верхнего символа (также известный как клиент ввода) получает события команды.</span><span class="sxs-lookup"><span data-stu-id="ff3a8-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives Command events.</span></span>

<span data-ttu-id="ff3a8-120">Можно использовать метод [**Activate**](activate-method.md), чтобы задать, является ли приложение активным клиентом символа, или сделать так, чтобы приложение использовало входной активный клиент (что также делает символ самым верхним).</span><span class="sxs-lookup"><span data-stu-id="ff3a8-120">You can use the [**Activate**](activate-method.md)method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="ff3a8-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="ff3a8-121">See Also</span></span>

[<span data-ttu-id="ff3a8-122">Активировать \* \* метод \* \*</span><span class="sxs-lookup"><span data-stu-id="ff3a8-122">\*\*\*\*Activate\*\* method\*\*</span></span>](activate-method.md)


 

 





