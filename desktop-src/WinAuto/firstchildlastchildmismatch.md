---
title: фирстчилдластчилдмисматч
description: фирстчилдластчилдмисматч
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411135"
---
# <a name="firstchildlastchildmismatch"></a><span data-ttu-id="a6c71-103">фирстчилдластчилдмисматч</span><span class="sxs-lookup"><span data-stu-id="a6c71-103">FirstChildLastChildMismatch</span></span>

## <a name="text"></a><span data-ttu-id="a6c71-104">Текст</span><span class="sxs-lookup"><span data-stu-id="a6c71-104">Text</span></span>

<span data-ttu-id="a6c71-105">При переходе по вызову {0} из протестированного узла и последующем многократном вызове {1} мы завершили следующий дочерний элемент: {2} .</span><span class="sxs-lookup"><span data-stu-id="a6c71-105">When navigating by calling {0} from the tested node, and then repeatedly calling {1}, we finished at the following child: {2}.</span></span> <span data-ttu-id="a6c71-106">Это не соответствует результату вызова {3} на проверенном узле, который вернул: {4} .</span><span class="sxs-lookup"><span data-stu-id="a6c71-106">This did not match the result of calling {3} on the tested node, which yielded: {4}.</span></span> <span data-ttu-id="a6c71-107">Вместо этого дочерний элемент должен сообщить как его родительский узел тестирования.</span><span class="sxs-lookup"><span data-stu-id="a6c71-107">Instead, the child should report as its parent the testing node.</span></span>

## <a name="type"></a><span data-ttu-id="a6c71-108">Тип</span><span class="sxs-lookup"><span data-stu-id="a6c71-108">Type</span></span>

<span data-ttu-id="a6c71-109">Ошибка</span><span class="sxs-lookup"><span data-stu-id="a6c71-109">Error</span></span>

## <a name="description"></a><span data-ttu-id="a6c71-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a6c71-110">Description</span></span>

<span data-ttu-id="a6c71-111">Возникла проблема при переходе между дочерними элементами элемента.</span><span class="sxs-lookup"><span data-stu-id="a6c71-111">There is a problem when navigating between element’s children.</span></span> <span data-ttu-id="a6c71-112">1.</span><span class="sxs-lookup"><span data-stu-id="a6c71-112">1.</span></span> <span data-ttu-id="a6c71-113">Неправильная или недопустимая реализация модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a6c71-113">An incorrect or invalid UI Automation implementation.</span></span>

<span data-ttu-id="a6c71-114">Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="a6c71-114">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a6c71-115">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="a6c71-115">Possible causes</span></span>

<span data-ttu-id="a6c71-116">Неправильная или недопустимая реализация модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a6c71-116">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6c71-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a6c71-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6c71-118">**Иуиаутоматионелемент:: Жеткачедпарент**</span><span class="sxs-lookup"><span data-stu-id="a6c71-118">**IUIAutomationElement::GetCachedParent**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[<span data-ttu-id="a6c71-119">**иуиаутоматионтривалкер**</span><span class="sxs-lookup"><span data-stu-id="a6c71-119">**IUIAutomationTreeWalker**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




