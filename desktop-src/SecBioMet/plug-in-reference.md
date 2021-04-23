---
title: Справочник по подключаемым модулям
description: 'Функции адаптера, функции-оболочки и структуры для создания пользовательских подключаемых адаптеров трех типов: подсистемы, датчика и хранилища.'
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API биометрическая платформа Windows API биометрическая платформа Windows, Справочник по подключаемым модулям
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487013"
---
# <a name="plug-in-reference"></a><span data-ttu-id="6e2e7-104">Справочник по подключаемым модулям</span><span class="sxs-lookup"><span data-stu-id="6e2e7-104">Plug-in Reference</span></span>

<span data-ttu-id="6e2e7-105">Биометрические устройства изготовлены в широком спектре типов и конфигураций.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-105">Biometric devices are manufactured in a wide variety of types and configurations.</span></span> <span data-ttu-id="6e2e7-106">Биометрическая платформа Windows включает расширяемую архитектуру, позволяющую работать с этими множеством, создавая пользовательские подключаемые модули. В центре этой архитектуры находится программный объект, называемый биометрической единицей.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-106">The Windows Biometric Framework incorporates an extensible architecture that enables you to deal with this variety by creating custom plug-ins. At the center of this architecture is a software object called a biometric unit.</span></span> <span data-ttu-id="6e2e7-107">Биометрическую единицу можно представить как абстракцию, которая представляет собой биометрический устройство для платформы.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-107">You can think of a biometric unit as an abstraction that represents a biometric device to the Framework.</span></span> <span data-ttu-id="6e2e7-108">Программные компоненты подключаемых модулей, называемые адаптерами, соединяют биометрическую единицу с соответствующим оборудованием.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-108">Plug-in software components called adapters connect the biometric unit to the associated hardware.</span></span> <span data-ttu-id="6e2e7-109">Существует три типа адаптеров, которые можно создать.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-109">There are three types of adapters that you can create.</span></span> <span data-ttu-id="6e2e7-110">Адаптер подсистемы создает Биометрические шаблоны из захваченных примеров, сопоставляет примеры с существующими шаблонами и шаблоны индексов.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-110">An engine adapter generates biometric templates from captured samples, matches samples to existing templates, and indexes templates.</span></span> <span data-ttu-id="6e2e7-111">Адаптер датчика создает оболочку для биометрического устройства и предоставляет стандартный интерфейс для настройки датчика, отслеживания образцов и управления передачей биометрических данных механизму обработки.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-111">A sensor adapter wraps a biometric device and provides a standard interface for configuring the sensor, capturing samples, and controlling the flow of biometric data to the processing engine.</span></span> <span data-ttu-id="6e2e7-112">Адаптер хранилища управляет шаблонами баз данных.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-112">A storage adapter manages template databases.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6e2e7-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="6e2e7-113">In this section</span></span>



| <span data-ttu-id="6e2e7-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="6e2e7-114">Topic</span></span>                                                                 | <span data-ttu-id="6e2e7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6e2e7-115">Description</span></span>                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e2e7-116">Функции подключаемых модулей</span><span class="sxs-lookup"><span data-stu-id="6e2e7-116">Plug-in Functions</span></span>](plug-in-functions.md)<br/>                 | <span data-ttu-id="6e2e7-117">Функции, которые можно использовать для создания подключаемых модулей адаптера, составляющих биометрическую единицу.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-117">Functions you can use to create the adapter plug-ins that make up a biometric unit.</span></span><br/>                                                                     |
| [<span data-ttu-id="6e2e7-118">Структуры подключаемых модулей</span><span class="sxs-lookup"><span data-stu-id="6e2e7-118">Plug-in Structures</span></span>](plug-in-structures.md)<br/>               | <span data-ttu-id="6e2e7-119">Структуры для разработки клиентских приложений с помощью API биометрическая платформа Windows.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-119">Structures for client application development by the Windows Biometric Framework API.</span></span><br/>                                                                   |
| [<span data-ttu-id="6e2e7-120">Функции-оболочки подключаемых модулей</span><span class="sxs-lookup"><span data-stu-id="6e2e7-120">Plug-in Wrapper Functions</span></span>](plug-in-wrapper-functions.md)<br/> | <span data-ttu-id="6e2e7-121">Функции-оболочки, позволяющие вызывать открытую функцию для любого адаптера, подключенного к конвейеру, без необходимости вручную получать указатель на адаптер.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-121">Wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span><br/> |



 

 

 





