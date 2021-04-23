---
description: Если параметр обработки возврата Мсидбкустомактионтипеконтинуе не установлен, настраиваемое действие должно возвращать целочисленный код состояния, как показано в следующей таблице.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Возвращаемые значения настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664589"
---
# <a name="custom-action-return-values"></a><span data-ttu-id="39f30-103">Возвращаемые значения настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="39f30-103">Custom Action Return Values</span></span>

<span data-ttu-id="39f30-104">Если параметр обработки возврата **мсидбкустомактионтипеконтинуе** не установлен, настраиваемое действие должно возвращать целочисленный код состояния, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="39f30-104">If the **msidbCustomActionTypeContinue** return processing option is not set, the custom action must return an integer status code as shown in the following table.</span></span>



| <span data-ttu-id="39f30-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39f30-105">Return value</span></span>                 | <span data-ttu-id="39f30-106">Описание</span><span class="sxs-lookup"><span data-stu-id="39f30-106">Description</span></span>                           |
|------------------------------|---------------------------------------|
| <span data-ttu-id="39f30-107">\_функция ERROR \_ не \_ вызвана</span><span class="sxs-lookup"><span data-stu-id="39f30-107">ERROR\_FUNCTION\_NOT\_CALLED</span></span> | <span data-ttu-id="39f30-108">Действие не выполнено.</span><span class="sxs-lookup"><span data-stu-id="39f30-108">Action not executed.</span></span>                  |
| <span data-ttu-id="39f30-109">Ошибка при \_ успешном выполнении</span><span class="sxs-lookup"><span data-stu-id="39f30-109">ERROR\_SUCCESS</span></span>               | <span data-ttu-id="39f30-110">Успешно завершенные действия.</span><span class="sxs-lookup"><span data-stu-id="39f30-110">Completed actions successfully.</span></span>       |
| <span data-ttu-id="39f30-111">Ошибка при \_ установке \_ усерексит</span><span class="sxs-lookup"><span data-stu-id="39f30-111">ERROR\_INSTALL\_USEREXIT</span></span>     | <span data-ttu-id="39f30-112">Пользователь завершился преждевременно.</span><span class="sxs-lookup"><span data-stu-id="39f30-112">User terminated prematurely.</span></span>          |
| <span data-ttu-id="39f30-113">Ошибка \_ \_ при установке</span><span class="sxs-lookup"><span data-stu-id="39f30-113">ERROR\_INSTALL\_FAILURE</span></span>      | <span data-ttu-id="39f30-114">Произошла неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="39f30-114">Unrecoverable error occurred.</span></span>         |
| <span data-ttu-id="39f30-115">Ошибка \_ больше \_ нет \_ элементов</span><span class="sxs-lookup"><span data-stu-id="39f30-115">ERROR\_NO\_MORE\_ITEMS</span></span>       | <span data-ttu-id="39f30-116">Пропустить оставшиеся действия, а не ошибку.</span><span class="sxs-lookup"><span data-stu-id="39f30-116">Skip remaining actions, not an error.</span></span> |



 

<span data-ttu-id="39f30-117">Обратите внимание, что настраиваемые действия, являющиеся [исполняемыми файлами](executable-files.md) , должны возвращать значение 0 для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="39f30-117">Note that custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="39f30-118">Установщик интерпретирует любое другое возвращаемое значение как сбой.</span><span class="sxs-lookup"><span data-stu-id="39f30-118">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="39f30-119">Чтобы игнорировать возвращаемые значения, установите флаг битов **мсидбкустомактионтипеконтинуе** в поле Тип [таблицы CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="39f30-119">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="39f30-120">Дополнительные сведения о параметре **мсидбкустомактионтипеконтинуе** и других возможностях обработки возврата см. в разделе [Параметры обработки возвращаемых данных пользовательского действия](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="39f30-120">For more information about the **msidbCustomActionTypeContinue** option and other return processing options, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="39f30-121">Обратите внимание, что установщик Windows преобразует возвращаемые значения из всех действий при записи возвращаемого значения в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="39f30-121">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="39f30-122">Например, если возвращаемое значение действия отображается как 1 в файле журнала, это означает, что действие вернуло ошибку \_ успешно.</span><span class="sxs-lookup"><span data-stu-id="39f30-122">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="39f30-123">Дополнительные сведения об этом переводе см. в разделе [ведение журнала возвращаемых значений действий](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="39f30-123">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="39f30-124">См. также</span><span class="sxs-lookup"><span data-stu-id="39f30-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39f30-125">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="39f30-125">Error Codes</span></span>](error-codes.md)
</dt> <dt>

[<span data-ttu-id="39f30-126">Ведение журнала возвращаемых значений действий</span><span class="sxs-lookup"><span data-stu-id="39f30-126">Logging of Action Return Values</span></span>](logging-of-action-return-values.md)
</dt> </dl>

 

 



