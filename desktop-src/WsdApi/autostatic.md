---
description: Указывает, должна ли Всдкодежен попытаться автоматически помечать определенные созданные поля как статические.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: элемент "автостатический"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994931"
---
# <a name="autostatic-element"></a><span data-ttu-id="86bd6-103">элемент "автостатический"</span><span class="sxs-lookup"><span data-stu-id="86bd6-103">autoStatic element</span></span>

<span data-ttu-id="86bd6-104">Указывает, должна ли Всдкодежен попытаться автоматически помечать определенные созданные поля как статические.</span><span class="sxs-lookup"><span data-stu-id="86bd6-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="86bd6-105">Это поведение включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86bd6-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="86bd6-106">Использование</span><span class="sxs-lookup"><span data-stu-id="86bd6-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="86bd6-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="86bd6-107">Attributes</span></span>

<span data-ttu-id="86bd6-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="86bd6-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="86bd6-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="86bd6-109">Child elements</span></span>

<span data-ttu-id="86bd6-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="86bd6-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="86bd6-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="86bd6-111">Parent elements</span></span>



| <span data-ttu-id="86bd6-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="86bd6-112">Element</span></span>                                     | <span data-ttu-id="86bd6-113">Описание</span><span class="sxs-lookup"><span data-stu-id="86bd6-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="86bd6-114">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="86bd6-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="86bd6-115">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="86bd6-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="86bd6-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="86bd6-116">Remarks</span></span>

<span data-ttu-id="86bd6-117">Элемент " **автостатический** " не является обязательным и может быть опущен в XML-файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="86bd6-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="86bd6-118">Элемент можно использовать для отключения пометки созданных полей как статических или для явного принудительного включения пометки некоторых созданных полей в статические.</span><span class="sxs-lookup"><span data-stu-id="86bd6-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="86bd6-119">Возможные значения: 1 (включено, по умолчанию) и 0 (отключено).</span><span class="sxs-lookup"><span data-stu-id="86bd6-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="86bd6-120">Включение функции **автостатического** выполнения может вызвать проблемы компиляции в зависимости от того, как генератор кода направляется на выходные данные.</span><span class="sxs-lookup"><span data-stu-id="86bd6-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="86bd6-121">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="86bd6-121">Element information</span></span>



| <span data-ttu-id="86bd6-122">Метка</span><span class="sxs-lookup"><span data-stu-id="86bd6-122">Label</span></span> | <span data-ttu-id="86bd6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="86bd6-123">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="86bd6-124">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="86bd6-124">Minimum supported system</span></span><br/> | <span data-ttu-id="86bd6-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86bd6-125">Windows Vista</span></span> |
| <span data-ttu-id="86bd6-126">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="86bd6-126">Can be empty</span></span>                        | <span data-ttu-id="86bd6-127">Да</span><span class="sxs-lookup"><span data-stu-id="86bd6-127">Yes</span></span>           |



 

 




