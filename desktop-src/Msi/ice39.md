---
description: ICE39 проверяет информационный поток сводки базы данных.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650928"
---
# <a name="ice39"></a><span data-ttu-id="c27ee-103">ICE39</span><span class="sxs-lookup"><span data-stu-id="c27ee-103">ICE39</span></span>

<span data-ttu-id="c27ee-104">ICE39 проверяет [информационный поток сводки](summary-information-stream.md) базы данных.</span><span class="sxs-lookup"><span data-stu-id="c27ee-104">ICE39 validates the [Summary Information Stream](summary-information-stream.md) of the database.</span></span>

<span data-ttu-id="c27ee-105">ICE39 проверяет формат следующих свойств:</span><span class="sxs-lookup"><span data-stu-id="c27ee-105">ICE39 checks the format of the following properties:</span></span>

-   [<span data-ttu-id="c27ee-106">**Сводка по количеству слов**</span><span class="sxs-lookup"><span data-stu-id="c27ee-106">**Word Count Summary**</span></span>](word-count-summary.md)
-   [<span data-ttu-id="c27ee-107">**Сводка по количеству страниц**</span><span class="sxs-lookup"><span data-stu-id="c27ee-107">**Page Count Summary**</span></span>](page-count-summary.md)
-   [<span data-ttu-id="c27ee-108">**Сводка по шаблону**</span><span class="sxs-lookup"><span data-stu-id="c27ee-108">**Template Summary**</span></span>](template-summary.md)
-   [<span data-ttu-id="c27ee-109">**Сводка по номеру редакции**</span><span class="sxs-lookup"><span data-stu-id="c27ee-109">**Revision Number Summary**</span></span>](revision-number-summary.md)
-   [<span data-ttu-id="c27ee-110">**Создать сводку по времени и дате**</span><span class="sxs-lookup"><span data-stu-id="c27ee-110">**Create Time/Date Summary**</span></span>](create-time-date-summary.md)
-   [<span data-ttu-id="c27ee-111">**Сводка по дате и времени последнего сохранения**</span><span class="sxs-lookup"><span data-stu-id="c27ee-111">**Last Saved Time/Date Summary**</span></span>](last-saved-time-date-summary.md)
-   [<span data-ttu-id="c27ee-112">**Последняя выводимая сводка**</span><span class="sxs-lookup"><span data-stu-id="c27ee-112">**Last Printed Summary**</span></span>](last-printed-summary.md)

<span data-ttu-id="c27ee-113">Если в свойстве " [**Сводка слов**](word-count-summary.md) " указано, что источник сжат, ICE39 отправляет предупреждение, если какие-либо файлы также помечены как сжатые в столбце Attributes [таблицы File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="c27ee-113">If the [**Word Count Summary**](word-count-summary.md) Property specifies that the source is compressed, ICE39 posts a warning if any files are also marked as compressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="c27ee-114">См. раздел [Использование ящиков и сжатых источников](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="c27ee-114">See [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="c27ee-115">ICE39 отправляет предупреждение, если в свойстве " [**Сводка слов**](word-count-summary.md) " указано, что пакет является совместимым с UAC, а [Таблица мсипаккажецертификате](msipackagecertificate-table.md) не пуста.</span><span class="sxs-lookup"><span data-stu-id="c27ee-115">ICE39 posts a warning if the [**Word Count Summary**](word-count-summary.md) Property specifies that the package is UAC compliant and the [MsiPackageCertificate Table](msipackagecertificate-table.md) is not empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c27ee-116">См. также</span><span class="sxs-lookup"><span data-stu-id="c27ee-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c27ee-117">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c27ee-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



