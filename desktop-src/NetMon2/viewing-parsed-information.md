---
description: Средство просмотра кадров сетевой монитор отображает проанализированные данные на трех панелях.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Просмотр проанализированных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551131"
---
# <a name="viewing-parsed-information"></a><span data-ttu-id="82e4d-103">Просмотр проанализированных данных</span><span class="sxs-lookup"><span data-stu-id="82e4d-103">Viewing Parsed Information</span></span>

<span data-ttu-id="82e4d-104">Средство просмотра кадров сетевой монитор отображает проанализированные данные на трех панелях.</span><span class="sxs-lookup"><span data-stu-id="82e4d-104">The Network Monitor frame viewer displays parsed data in three panes.</span></span> <span data-ttu-id="82e4d-105">В верхней области отображается сводка по кадру, включающему идентифицированный протокол.</span><span class="sxs-lookup"><span data-stu-id="82e4d-105">The upper pane displays a summary of the frame that includes the identified protocol.</span></span> <span data-ttu-id="82e4d-106">В средней области отображаются свойства форматированных данных, которые могут быть организованы иерархически в виде части отображения средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="82e4d-106">The middle pane displays the formatted data properties that can be organized hierarchically as part of the parser display.</span></span> <span data-ttu-id="82e4d-107">На нижней панели отображаются выделенные необработанные данные, выбранные из средней области.</span><span class="sxs-lookup"><span data-stu-id="82e4d-107">The lower pane displays highlighted raw data that is selected from the middle pane.</span></span>

<span data-ttu-id="82e4d-108">Можно указать способ отображения информации в средстве просмотра при разработке собственного средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="82e4d-108">You can specify how the information in the viewer is displayed when you develop your own parser.</span></span> <span data-ttu-id="82e4d-109">На следующем рисунке показано, как можно отобразить сведения в средстве просмотра кадров сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="82e4d-109">The following illustration shows how information can be displayed in the Network Monitor frame viewer.</span></span>

![средство просмотра кадров сетевого монитора](images/parseui.png)

> [!Note]  
> <span data-ttu-id="82e4d-111">Средства синтаксического анализа не отображают кадры.</span><span class="sxs-lookup"><span data-stu-id="82e4d-111">Parsers do not display frames.</span></span> <span data-ttu-id="82e4d-112">Средства синтаксического анализа распознают поля в предоставленных сведениях, а затем уведомляют сетевой монитор, чтобы отобразить кадр.</span><span class="sxs-lookup"><span data-stu-id="82e4d-112">Parsers recognize fields in the information provided, and then notify Network Monitor to display the frame.</span></span> <span data-ttu-id="82e4d-113">Фильтрация — это операция более высокого уровня, которая позволяет фильтровать запросы на охват средств синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="82e4d-113">Filtering is a higher level operation that allows filter queries to span parsers.</span></span>

 

<span data-ttu-id="82e4d-114">В средстве синтаксического анализа используйте только функции, которые могут выполняться в приложениях Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="82e4d-114">In your parser, use only functions that can run on Microsoft Win32 applications.</span></span> <span data-ttu-id="82e4d-115">Перед присоединением свойств к необработанным данным средство синтаксического анализа должно сначала зарегистрировать все возможные свойства с помощью ядра сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="82e4d-115">Before attaching properties to the raw data, a parser must first register all possible properties with the Network Monitor kernel.</span></span> <span data-ttu-id="82e4d-116">Средство синтаксического анализа отправляет в ядро сообщение для создания базы данных свойств, а затем заполняет базу данных свойств любым возможным свойством для его протокола.</span><span class="sxs-lookup"><span data-stu-id="82e4d-116">The parser sends a message to the kernel to create a property database, and then fills the property database with every possible property for its protocol.</span></span> <span data-ttu-id="82e4d-117">Каждое свойство в базе данных свойств содержит такие сведения, как текстовое описание, тип данных и квалификатор, которые используются для форматирования необработанных данных, и подпрограммы форматирования, используемые для вывода данных.</span><span class="sxs-lookup"><span data-stu-id="82e4d-117">Each property in the property database contains information such as a textual description, a data type and qualifier that are used to format the raw data, and a formatting routine that is used to display the data.</span></span>

 

 



