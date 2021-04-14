---
title: Инициализация ленты
description: Приложение должно использовать функцию CreateFile для создания маркера ленточного устройства. Этот маркер используется в последующих операциях на ленте устройства.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Резервное копирование ленты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488001"
---
# <a name="tape-initialization"></a><span data-ttu-id="6093a-105">Инициализация ленты</span><span class="sxs-lookup"><span data-stu-id="6093a-105">Tape Initialization</span></span>

<span data-ttu-id="6093a-106">Приложение должно использовать функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) для создания маркера ленточного устройства.</span><span class="sxs-lookup"><span data-stu-id="6093a-106">An application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to create a handle of a tape device.</span></span> <span data-ttu-id="6093a-107">Этот маркер используется в последующих операциях на ленте устройства.</span><span class="sxs-lookup"><span data-stu-id="6093a-107">This handle is used in subsequent operations on the tape in the device.</span></span>

<span data-ttu-id="6093a-108">Прежде чем приложение запишет на ленту, необходимо отформатировать ленту в соответствии с потребностями приложения и возможностями используемого ленточного накопителя.</span><span class="sxs-lookup"><span data-stu-id="6093a-108">Before an application writes to a tape, the tape must be formatted according to the needs of the application and the capabilities of the tape drive being used.</span></span> <span data-ttu-id="6093a-109">Функция [**креатетапепартитион**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) переформатирует ленту, создавая на ней заданное количество разделов указанного размера.</span><span class="sxs-lookup"><span data-stu-id="6093a-109">The [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) function reformats a tape, creating on it a given number of partitions of a specified size.</span></span>

<span data-ttu-id="6093a-110">Функция [**препаретапе**](/windows/desktop/api/Winbase/nf-winbase-preparetape) готовит ленту к доступу или удалению.</span><span class="sxs-lookup"><span data-stu-id="6093a-110">The [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) function prepares a tape to be accessed or removed.</span></span> <span data-ttu-id="6093a-111">Эта функция может загружать, выгружать, блокировать или разблокировать ленту.</span><span class="sxs-lookup"><span data-stu-id="6093a-111">This function can load, unload, lock, or unlock a tape.</span></span> <span data-ttu-id="6093a-112">Эта функция также может натяжение ленты путем перемещения ленты в конец ленты и обратно в начало.</span><span class="sxs-lookup"><span data-stu-id="6093a-112">This function can also tension the tape by moving the tape to the end of the tape and back to the beginning.</span></span>

<span data-ttu-id="6093a-113">Чтобы получить и задать сведения о ленточном накопителе и ленточном накопителе, приложение использует функции [**жеттапепараметерс**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**сеттапепараметерс**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)и [**жеттапестатус**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .</span><span class="sxs-lookup"><span data-stu-id="6093a-113">To retrieve and set information about a tape and tape drive, an application uses the [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters), and [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) functions.</span></span>

<span data-ttu-id="6093a-114">[**Жеттапепараметерс**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) извлекает сведения, описывающие ленту или ленточный накопитель.</span><span class="sxs-lookup"><span data-stu-id="6093a-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) retrieves information that describes a tape or a tape drive.</span></span> <span data-ttu-id="6093a-115">Сведения о ленте включают тип ленты, плотность и размер блока. Количество секций на ленте; оставшийся объем ленты; и т. д.</span><span class="sxs-lookup"><span data-stu-id="6093a-115">The tape information includes the tape's type, density, and block size; the number of partitions on the tape; the amount of tape remaining; and so on.</span></span> <span data-ttu-id="6093a-116">Сведения о ленточном накопителе включают размер блока по умолчанию диска, максимальное число разделов и поддерживаемые функции.</span><span class="sxs-lookup"><span data-stu-id="6093a-116">The tape drive information includes the drive's default block size, the maximum partition count, and the features that are supported.</span></span>

<span data-ttu-id="6093a-117">[**Сеттапепараметерс**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) либо задает размер блока ленты, либо устанавливает флаги ленточного накопителя, указывающие, поддерживает ли диск аппаратную коррекцию ошибок, сжатие данных, заполнение данных или любое сочетание трех.</span><span class="sxs-lookup"><span data-stu-id="6093a-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) either sets the tape block size or sets the tape drive flags that indicate whether the drive supports hardware error correction, data compression, data padding, or any combination of the three.</span></span>

<span data-ttu-id="6093a-118">[**Жеттапестатус**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) указывает, готов ли ленточный накопитель к обработке команд ленты.</span><span class="sxs-lookup"><span data-stu-id="6093a-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indicates whether the tape drive is ready to process tape commands.</span></span>

 

 