---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fada27e903c465f9b5e0342fca481e5161b699c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674048"
---
# <a name="t-windows-installer"></a><span data-ttu-id="71aa2-103">T (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="71aa2-103">T (Windows Installer)</span></span>

<span data-ttu-id="71aa2-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р [. J K](i-gly.md) L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="71aa2-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="71aa2-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**обработка транзакций**</span><span class="sxs-lookup"><span data-stu-id="71aa2-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**transaction processing**</span></span>
</dt> <dd>

<span data-ttu-id="71aa2-106">Одна или несколько операций обрабатывались в виде одного неделимого целого числа, называемого транзакцией.</span><span class="sxs-lookup"><span data-stu-id="71aa2-106">One or more operations processed together as a single indivisible whole called a transaction.</span></span> <span data-ttu-id="71aa2-107">Все составляющие операции должны быть выполнены, чтобы транзакция была выполнена, в противном случае выполняется откат всех операций в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="71aa2-107">All the constituent operations must succeed for the transaction to succeed, otherwise all the operations are rolled back to the original state.</span></span>

</dd> <dt>

<span data-ttu-id="71aa2-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Преобразует**</span><span class="sxs-lookup"><span data-stu-id="71aa2-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="71aa2-109">Шаблон различий между двумя [*базами данных установщика*](i-gly.md) , которые можно применить для получения аналогичных изменений в других базах данных.</span><span class="sxs-lookup"><span data-stu-id="71aa2-109">Template of the differences between two [*installer databases*](i-gly.md) that can be applied to produce similar changes in other databases.</span></span> <span data-ttu-id="71aa2-110">Например, преобразование локализации можно использовать для изменения языка приложения.</span><span class="sxs-lookup"><span data-stu-id="71aa2-110">For example, a localization transform can be used to change the language of an application.</span></span> <span data-ttu-id="71aa2-111">Дополнительные сведения см. в разделе [слияния и преобразования](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="71aa2-111">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

</dd> <dt>

<span data-ttu-id="71aa2-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**флаги состояния ошибки преобразования**</span><span class="sxs-lookup"><span data-stu-id="71aa2-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transform error condition flags**</span></span>
</dt> <dd>

<span data-ttu-id="71aa2-113">Набор свойств, используемых для отметки условий ошибок [*преобразования*](/windows).</span><span class="sxs-lookup"><span data-stu-id="71aa2-113">Set of properties used to flag the error conditions of a [*transform*](/windows).</span></span> <span data-ttu-id="71aa2-114">Дополнительные сведения см. в разделе [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="71aa2-114">For more information, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> <dt>

<span data-ttu-id="71aa2-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**Преобразование флагов проверки**</span><span class="sxs-lookup"><span data-stu-id="71aa2-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transform validation flags**</span></span>
</dt> <dd>

<span data-ttu-id="71aa2-116">Набор свойств, используемый для проверки того, что [*Преобразование*](/windows) может быть применено к базе данных.</span><span class="sxs-lookup"><span data-stu-id="71aa2-116">Set of properties used to verify that the [*transform*](/windows) can be applied to the database.</span></span> <span data-ttu-id="71aa2-117">Список этих свойств см. в разделе [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="71aa2-117">For a list of these properties, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> </dl>

 

 
