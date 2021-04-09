---
description: Используйте следующие флаги параметров, чтобы указать, что установщик не записывает значение, указанное в поле Целевой объект таблицы CustomAction, в журнал. Чтобы задать параметр, добавьте значение в этой таблице в значение поля Тип таблицы CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Параметр скрытого целевого объекта настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080927"
---
# <a name="custom-action-hidden-target-option"></a><span data-ttu-id="86989-104">Параметр скрытого целевого объекта настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="86989-104">Custom Action Hidden Target Option</span></span>

<span data-ttu-id="86989-105">Используйте следующие флаги параметров, чтобы указать, что установщик не записывает значение, указанное в поле Целевой объект [таблицы CustomAction](customaction-table.md) , в журнал.</span><span class="sxs-lookup"><span data-stu-id="86989-105">Use the following option flags to specify that the installer not write the value entered into the Target field of the [CustomAction table](customaction-table.md) into the log.</span></span> <span data-ttu-id="86989-106">Чтобы задать параметр, добавьте значение в этой таблице в значение поля Тип таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="86989-106">To set the option add the value in this table to the value in the Type field of the CustomAction table.</span></span>



| <span data-ttu-id="86989-107">Константа</span><span class="sxs-lookup"><span data-stu-id="86989-107">Constant</span></span>                            | <span data-ttu-id="86989-108">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="86989-108">Hexadecimal</span></span> | <span data-ttu-id="86989-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="86989-109">Decimal</span></span> | <span data-ttu-id="86989-110">Описание</span><span class="sxs-lookup"><span data-stu-id="86989-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86989-111">(нет)</span><span class="sxs-lookup"><span data-stu-id="86989-111">(none)</span></span>                              | <span data-ttu-id="86989-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="86989-112">0x0000</span></span>      | <span data-ttu-id="86989-113">0</span><span class="sxs-lookup"><span data-stu-id="86989-113">0</span></span>       | <span data-ttu-id="86989-114">Установщик может записать значение в столбец Target таблицы CustomAction в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="86989-114">The installer may write the value in the Target column of the CustomAction table into the log file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="86989-115">**мсидбкустомактионтипехидетаржет**</span><span class="sxs-lookup"><span data-stu-id="86989-115">**msidbCustomActionTypeHideTarget**</span></span> | <span data-ttu-id="86989-116">0x2000</span><span class="sxs-lookup"><span data-stu-id="86989-116">0x2000</span></span>      | <span data-ttu-id="86989-117">8192</span><span class="sxs-lookup"><span data-stu-id="86989-117">8192</span></span>    | <span data-ttu-id="86989-118">Установщику не удается записать значение в целевой столбец [таблицы CustomAction](customaction-table.md) в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="86989-118">The installer is prevented from writing the value in the Target column of the [CustomAction table](customaction-table.md) into the log file.</span></span> <span data-ttu-id="86989-119">Свойство CustomActionData также не регистрируется, когда установщик выполняет пользовательское действие.</span><span class="sxs-lookup"><span data-stu-id="86989-119">The CustomActionData property is also not logged when the installer executes the custom action.</span></span><br/> <span data-ttu-id="86989-120">Поскольку установщик устанавливает значение CustomActionData из свойства с тем же именем, что и пользовательское действие, это свойство должно быть указано в свойстве [**мсихидденпропертиес**](msihiddenproperties.md) , чтобы предотвратить появление его значения в журнале.</span><span class="sxs-lookup"><span data-stu-id="86989-120">Because the installer sets the value of CustomActionData from a property with the same name as the custom action, that property must be listed in the [**MsiHiddenProperties**](msihiddenproperties.md) Property to prevent its value from appearing in the log.</span></span><br/> |



 

<span data-ttu-id="86989-121">Дополнительные сведения см. в разделе [предотвращение записи конфиденциальной информации в файл журнала](preventing-confidential-information-from-being-written-into-the-log-file.md) .</span><span class="sxs-lookup"><span data-stu-id="86989-121">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="86989-122">См. также</span><span class="sxs-lookup"><span data-stu-id="86989-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86989-123">Ссылка на настраиваемое действие</span><span class="sxs-lookup"><span data-stu-id="86989-123">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="86989-124">Сведения о настраиваемых действиях</span><span class="sxs-lookup"><span data-stu-id="86989-124">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="86989-125">Использование настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="86989-125">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 




