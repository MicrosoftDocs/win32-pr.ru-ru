---
title: Сообщения команды
description: Сообщения команды
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Сообщения команды MCI, сведения
- Сообщения команды MCI, синтаксис
- Функция МЦисендкомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533101"
---
# <a name="command-messages"></a><span data-ttu-id="5c68f-106">Сообщения команды</span><span class="sxs-lookup"><span data-stu-id="5c68f-106">Command Messages</span></span>

<span data-ttu-id="5c68f-107">Интерфейс командной строки предназначен для использования приложениями, которым требуется интерфейс языка C для управления устройствами мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5c68f-107">The command-message interface is designed to be used by applications requiring a C-language interface to control multimedia devices.</span></span> <span data-ttu-id="5c68f-108">Для взаимодействия с устройствами MCI используется парадигма передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c68f-108">It uses a message-passing paradigm to communicate with MCI devices.</span></span> <span data-ttu-id="5c68f-109">Команду можно отправить с помощью функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5c68f-109">You can send a command by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="5c68f-110">Функция **мЦисендкомманд** возвращает нуль в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="5c68f-110">The **mciSendCommand** function returns zero if successful.</span></span> <span data-ttu-id="5c68f-111">Если функция завершается ошибкой, в слове с низким порядком возвращаемого значения содержится код ошибки.</span><span class="sxs-lookup"><span data-stu-id="5c68f-111">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="5c68f-112">Этот код ошибки можно передать функции [**мЦижетеррорстринг**](/previous-versions//dd757158(v=vs.85)) , чтобы получить текстовое описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="5c68f-112">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-messages"></a><span data-ttu-id="5c68f-113">Синтаксис сообщений команды</span><span class="sxs-lookup"><span data-stu-id="5c68f-113">Syntax of Command Messages</span></span>

<span data-ttu-id="5c68f-114">Сообщения команды MCI состоят из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="5c68f-114">MCI command messages consist of the following elements:</span></span>

-   <span data-ttu-id="5c68f-115">Постоянное значение сообщения</span><span class="sxs-lookup"><span data-stu-id="5c68f-115">A constant message value</span></span>
-   <span data-ttu-id="5c68f-116">Структура, содержащая параметры для команды</span><span class="sxs-lookup"><span data-stu-id="5c68f-116">A structure containing parameters for the command</span></span>
-   <span data-ttu-id="5c68f-117">Набор флагов, задающий параметры для команды и проверки полей в блоке параметров</span><span class="sxs-lookup"><span data-stu-id="5c68f-117">A set of flags specifying options for the command and validating fields in the parameter block</span></span>

<span data-ttu-id="5c68f-118">В следующем примере функция [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) используется для отправки команды [**MCI \_ Play**](mci-play.md) устройству, идентифицируемому идентификатором устройства.</span><span class="sxs-lookup"><span data-stu-id="5c68f-118">The following example uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_ PLAY**](mci-play.md) command to the device identified by a device identifier.</span></span>


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



<span data-ttu-id="5c68f-119">Идентификатор устройства, указанный в первом параметре, извлекается при открытии устройства с помощью команды [**MCI \_ Open**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="5c68f-119">The device identifier given in the first parameter is retrieved when the device is opened using the [**MCI\_ OPEN**](mci-open.md) command.</span></span> <span data-ttu-id="5c68f-120">Последний параметр — это адрес структуры [**MCI \_ Play \_ пармс**](mci-play-parms.md) , которая может содержать сведения о начале и завершении воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5c68f-120">The last parameter is the address of an [**MCI\_ PLAY\_ PARMS**](mci-play-parms.md) structure, which might contain information about where to begin and end playback.</span></span> <span data-ttu-id="5c68f-121">Многие сообщения команды MCI используют структуру для хранения параметров этого типа.</span><span class="sxs-lookup"><span data-stu-id="5c68f-121">Many MCI command messages use a structure to contain parameters of this kind.</span></span> <span data-ttu-id="5c68f-122">Первый член каждой из этих структур определяет окно, которое получает сообщение [**\_ мЦинотифи мм**](mm-mcinotify.md) по завершении операции.</span><span class="sxs-lookup"><span data-stu-id="5c68f-122">The first member of each of these structures identifies the window that receives an [**MM\_ MCINOTIFY**](mm-mcinotify.md) message when the operation finishes.</span></span>

 

 