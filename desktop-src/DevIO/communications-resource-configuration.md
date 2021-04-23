---
description: Структура КОММКОНФИГ определяет конфигурацию ресурса связи, последовательного или иным образом.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Конфигурация ресурса связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141519"
---
# <a name="communications-resource-configuration"></a><span data-ttu-id="8e93e-103">Конфигурация ресурса связи</span><span class="sxs-lookup"><span data-stu-id="8e93e-103">Communications Resource Configuration</span></span>

<span data-ttu-id="8e93e-104">Структура [**коммконфиг**](/windows/desktop/api/Winbase/ns-winbase-commconfig) определяет конфигурацию ресурса связи, последовательного или иным образом.</span><span class="sxs-lookup"><span data-stu-id="8e93e-104">The [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure defines the configuration of a communications resource, serial or otherwise.</span></span> <span data-ttu-id="8e93e-105">Формат структуры зависит от типа ресурса связи (подтип поставщика).</span><span class="sxs-lookup"><span data-stu-id="8e93e-105">The format of the structure varies depending on the type of communications resource (the provider subtype).</span></span> <span data-ttu-id="8e93e-106">Первые несколько элементов структуры являются общими для всех коммуникационных ресурсов; дополнительные члены определяются для конкретных подтипов поставщика.</span><span class="sxs-lookup"><span data-stu-id="8e93e-106">The first few structure members are common to all communications resources; additional members are defined for specific provider subtypes.</span></span> <span data-ttu-id="8e93e-107">Определенные поставщики услуг также могут расширить структуру **коммконфиг** .</span><span class="sxs-lookup"><span data-stu-id="8e93e-107">Specific service providers may extend the **COMMCONFIG** structure as well.</span></span>

<span data-ttu-id="8e93e-108">Приложение может получить и настроить конфигурацию ресурса связи с помощью функций [**жеткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) и [**сеткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) .</span><span class="sxs-lookup"><span data-stu-id="8e93e-108">An application can get and set the configuration of a communications resource by using the [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) and [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) functions.</span></span> <span data-ttu-id="8e93e-109">При открытии ресурс связи инициализируется с использованием конфигурации по умолчанию для подтипа поставщика.</span><span class="sxs-lookup"><span data-stu-id="8e93e-109">When opened, a communications resource is initialized using the default configuration for its provider subtype.</span></span> <span data-ttu-id="8e93e-110">Чтобы получить и задать конфигурацию по умолчанию для подтипа поставщика, используйте функции [**жетдефаулткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) и [**сетдефаулткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .</span><span class="sxs-lookup"><span data-stu-id="8e93e-110">To get and set the default configuration for a provider subtype, use the [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) and [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) functions.</span></span>

<span data-ttu-id="8e93e-111">Чтобы запросить у пользователя сведения о конфигурации, используйте функцию [**коммконфигдиалог**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) .</span><span class="sxs-lookup"><span data-stu-id="8e93e-111">To prompt the user for configuration information, use the [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) function.</span></span> <span data-ttu-id="8e93e-112">Эта функция отображает диалоговое окно, определенное поставщиком услуг, и заполняет структуру [**коммконфиг**](/windows/desktop/api/Winbase/ns-winbase-commconfig) на основе введенных пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="8e93e-112">This function displays a dialog box defined by the service provider and fills in a [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure based on user input.</span></span>

 

 



