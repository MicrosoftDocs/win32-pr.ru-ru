---
description: Указывает, должна ли Всдкодежен попытаться автоматически помечать определенные созданные поля как статические.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: элемент "автостатический"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32591c43c850af05014ff92fc4023e228b371fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711719"
---
# <a name="autostatic-element"></a><span data-ttu-id="65a9e-103">элемент "автостатический"</span><span class="sxs-lookup"><span data-stu-id="65a9e-103">autoStatic element</span></span>

<span data-ttu-id="65a9e-104">Указывает, должна ли Всдкодежен попытаться автоматически помечать определенные созданные поля как статические.</span><span class="sxs-lookup"><span data-stu-id="65a9e-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="65a9e-105">Это поведение включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="65a9e-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="65a9e-106">Использование</span><span class="sxs-lookup"><span data-stu-id="65a9e-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="65a9e-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="65a9e-107">Attributes</span></span>

<span data-ttu-id="65a9e-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="65a9e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="65a9e-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="65a9e-109">Child elements</span></span>

<span data-ttu-id="65a9e-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="65a9e-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="65a9e-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="65a9e-111">Parent elements</span></span>



| <span data-ttu-id="65a9e-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="65a9e-112">Element</span></span>                                     | <span data-ttu-id="65a9e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="65a9e-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="65a9e-114">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="65a9e-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="65a9e-115">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="65a9e-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="65a9e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65a9e-116">Remarks</span></span>

<span data-ttu-id="65a9e-117">Элемент " **автостатический** " не является обязательным и может быть опущен в XML-файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="65a9e-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="65a9e-118">Элемент можно использовать для отключения пометки созданных полей как статических или для явного принудительного включения пометки некоторых созданных полей в статические.</span><span class="sxs-lookup"><span data-stu-id="65a9e-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="65a9e-119">Возможные значения: 1 (включено, по умолчанию) и 0 (отключено).</span><span class="sxs-lookup"><span data-stu-id="65a9e-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="65a9e-120">Включение функции **автостатического** выполнения может вызвать проблемы компиляции в зависимости от того, как генератор кода направляется на выходные данные.</span><span class="sxs-lookup"><span data-stu-id="65a9e-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="65a9e-121">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="65a9e-121">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="65a9e-122">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="65a9e-122">Minimum supported system</span></span><br/> | <span data-ttu-id="65a9e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65a9e-123">Windows Vista</span></span> |
| <span data-ttu-id="65a9e-124">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="65a9e-124">Can be empty</span></span>                        | <span data-ttu-id="65a9e-125">Да</span><span class="sxs-lookup"><span data-stu-id="65a9e-125">Yes</span></span>           |



 

 




