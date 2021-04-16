---
description: Произвольный целочисленный тип семантического типа является одним из типов целочисленного формата.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Произвольный целочисленный тип
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156339"
---
# <a name="arbitrary-integer-type"></a><span data-ttu-id="ecfb4-103">Произвольный целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="ecfb4-103">Arbitrary Integer Type</span></span>

<span data-ttu-id="ecfb4-104">Произвольный целочисленный тип [семантического типа](semantic-types.md) является одним из [типов целочисленного формата](integer-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="ecfb4-104">The Arbitrary Integer Type of [semantic type](semantic-types.md) is one of the [Integer Format Types](integer-format-types.md).</span></span> <span data-ttu-id="ecfb4-105">Этот тип настраиваемого элемента является целым числом, предоставленным пользователем.</span><span class="sxs-lookup"><span data-stu-id="ecfb4-105">This type of configurable item is an integer provided by the user.</span></span> <span data-ttu-id="ecfb4-106">Средство слияния заменяет это целое число на шаблоны, указанные в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="ecfb4-106">The merge tool substitutes this integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="ecfb4-107">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя текстовой строки в столбец Name, ввести "2" в столбец Format и оставить пустыми столбцы Type и Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="ecfb4-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "2" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="ecfb4-108">Столбцы Type и Контекстдата зарезервированы и должны иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="ecfb4-108">The Type and ContextData columns are reserved and must be null.</span></span>

 

 



