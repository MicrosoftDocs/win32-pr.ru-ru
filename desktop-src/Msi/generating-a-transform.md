---
description: Следующая процедура описывает сценарий создания преобразования, которое окончательно скрывает функцию.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Создание преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081069"
---
# <a name="generating-a-transform"></a><span data-ttu-id="d57b7-103">Создание преобразования</span><span class="sxs-lookup"><span data-stu-id="d57b7-103">Generating a Transform</span></span>

<span data-ttu-id="d57b7-104">Следующая процедура описывает сценарий создания преобразования, которое окончательно скрывает функцию.</span><span class="sxs-lookup"><span data-stu-id="d57b7-104">The following procedure describes a scenario to generate a transform that permanently hides a feature.</span></span>

<span data-ttu-id="d57b7-105">**Постоянное скрытие функции продукта**</span><span class="sxs-lookup"><span data-stu-id="d57b7-105">**To permanently hide a product feature**</span></span>

1.  <span data-ttu-id="d57b7-106">Скопируйте исходный установочный пакет.</span><span class="sxs-lookup"><span data-stu-id="d57b7-106">Copy the original installation package.</span></span>
2.  <span data-ttu-id="d57b7-107">Измените копию, установив значение столбца отобразить в [таблице Features](feature-table.md) равным нулю.</span><span class="sxs-lookup"><span data-stu-id="d57b7-107">Alter the copy by setting the value of the Display column in the [Feature table](feature-table.md) to zero.</span></span> <span data-ttu-id="d57b7-108">Это позволяет скрыть функцию.</span><span class="sxs-lookup"><span data-stu-id="d57b7-108">This specifies hiding the feature.</span></span>
3.  <span data-ttu-id="d57b7-109">Создайте преобразование из исходного пакета установки в новые пакеты установки, вызвав [**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span><span class="sxs-lookup"><span data-stu-id="d57b7-109">Create a transform from the original installation package to the new installation packages by calling [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span></span>
4.  <span data-ttu-id="d57b7-110">Создайте сводные данные в преобразовании, вызвав [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="d57b7-110">Create the summary information in the transform by calling [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

<span data-ttu-id="d57b7-111">Преобразование затем Готово к применению во время установки.</span><span class="sxs-lookup"><span data-stu-id="d57b7-111">The transform is then ready to be applied during installation.</span></span> <span data-ttu-id="d57b7-112">Дополнительные сведения см. в разделе [применение преобразований](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="d57b7-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



