---
description: Выдача необработанных команд AV/C
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Выдача необработанных команд AV/C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416596"
---
# <a name="issuing-raw-avc-commands"></a><span data-ttu-id="08fa6-103">Выдача необработанных команд AV/C</span><span class="sxs-lookup"><span data-stu-id="08fa6-103">Issuing Raw AV/C Commands</span></span>

<span data-ttu-id="08fa6-104">Интерфейсы [**иамекстдевице**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**иамексттранспорт**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)и [**иамтимекодереадер**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) работают путем перевода вызовов метода в команды для драйвера, интерпретации ответа драйвера и его возврата через **HRESULT** или выходной параметр.</span><span class="sxs-lookup"><span data-stu-id="08fa6-104">The [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport), and [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) interfaces work by translating the method calls into commands for the driver, then interpreting the driver's response and returning it through an **HRESULT** or an output parameter.</span></span> <span data-ttu-id="08fa6-105">Однако некоторые функции устройства могут быть недоступны через эти методы.</span><span class="sxs-lookup"><span data-stu-id="08fa6-105">However, some device functions may not be accessible through these methods.</span></span> <span data-ttu-id="08fa6-106">Таким образом, МСДВ поддерживает отправку необработанных команд AV/C на устройство.</span><span class="sxs-lookup"><span data-stu-id="08fa6-106">Therefore, MSDV supports sending raw AV/C commands to the device.</span></span>

<span data-ttu-id="08fa6-107">При использовании этой функции следует учитывать следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="08fa6-107">You should keep the following points in mind when using this feature:</span></span>

-   <span data-ttu-id="08fa6-108">Команда передается непосредственно на устройство без проверки ошибок или параметров.</span><span class="sxs-lookup"><span data-stu-id="08fa6-108">The command is passed directly to the device, with no error checking or parameter validation.</span></span> <span data-ttu-id="08fa6-109">По этой причине следует выдавать необработанные команды AV/C, только если интерфейсы DirectShow не реализуют нужные вам функции.</span><span class="sxs-lookup"><span data-stu-id="08fa6-109">For this reason, you should issue raw AV/C commands only when the DirectShow interfaces do not implement the functionality you need.</span></span>
-   <span data-ttu-id="08fa6-110">Все необработанные команды AV/C являются синхронными.</span><span class="sxs-lookup"><span data-stu-id="08fa6-110">All raw AV/C commands are synchronous.</span></span> <span data-ttu-id="08fa6-111">Поток, выдающий команду, блокируется до тех пор, пока команда не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="08fa6-111">The thread issuing the command blocks until the command returns.</span></span>
-   <span data-ttu-id="08fa6-112">В каждый момент времени может быть предоставлена только одна команда.</span><span class="sxs-lookup"><span data-stu-id="08fa6-112">Only one command can be given at a time.</span></span> <span data-ttu-id="08fa6-113">Во время обработки команды устройство будет отклонять любые дополнительные команды.</span><span class="sxs-lookup"><span data-stu-id="08fa6-113">While the command is being processed, the device will reject any additional commands.</span></span>
-   <span data-ttu-id="08fa6-114">Драйвер УВК не поддерживает необработанные команды AV/C.</span><span class="sxs-lookup"><span data-stu-id="08fa6-114">The UVC driver does not support raw AV/C commands.</span></span>

<span data-ttu-id="08fa6-115">Чтобы отправить команду AV/C, отформатируйте команду в виде массива байтов.</span><span class="sxs-lookup"><span data-stu-id="08fa6-115">To send an AV/C command, format the command as an array of bytes.</span></span> <span data-ttu-id="08fa6-116">Затем вызовите [**иамексттранспорт:: жеттранспортбасикпараметерс**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span><span class="sxs-lookup"><span data-stu-id="08fa6-116">Then call [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span></span> <span data-ttu-id="08fa6-117">Передайте флаг "ED \_ RAW \_ ext cmd" \_ \_ , размер массива и массив.</span><span class="sxs-lookup"><span data-stu-id="08fa6-117">Pass in the ED\_RAW\_EXT\_DEV\_CMD flag, the array size, and the array.</span></span> <span data-ttu-id="08fa6-118">Необходимо привести адрес массива к типу \**лполестр \** _, так как первоначальное назначение этого параметра было бы возвращать строковое значение.</span><span class="sxs-lookup"><span data-stu-id="08fa6-118">You must cast the array address to an \**LPOLESTR\** _ type, because the original purpose of this parameter was to return a string value.</span></span>


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



<span data-ttu-id="08fa6-119">Содержимое массива передается непосредственно на устройство, поэтому необходимо соблюдать осторожность при правильном форматировании.</span><span class="sxs-lookup"><span data-stu-id="08fa6-119">The contents of the array are passed directly to the device, so you must be careful to format it correctly.</span></span> <span data-ttu-id="08fa6-120">Команда может ориентироваться на единицу (видеокамера) или подединицу (ленту или камеру).</span><span class="sxs-lookup"><span data-stu-id="08fa6-120">A command can target the unit (camcorder) or a subunit (tape or camera).</span></span> <span data-ttu-id="08fa6-121">Соответствующие стандарты доступны на [веб-сайте торговой связи 1394](https://1394ta.org).</span><span class="sxs-lookup"><span data-stu-id="08fa6-121">The relevant standards are available from the [1394 Trade Association Web site](https://1394ta.org).</span></span>

-   <span data-ttu-id="08fa6-122">Общая спецификация набора команд для цифрового интерфейса AV/C</span><span class="sxs-lookup"><span data-stu-id="08fa6-122">AV/C Digital Interface Command Set General Specification</span></span>
-   <span data-ttu-id="08fa6-123">Спецификация подразделений для записи или воспроизведения на ленте AV/C</span><span class="sxs-lookup"><span data-stu-id="08fa6-123">AV/C Tape Recorder/Player Subunit Specification</span></span>

<span data-ttu-id="08fa6-124">В предыдущем описан способ форматирования команд AV/C и перечислены команды единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="08fa6-124">The former describes how to format AV/C commands and lists the unit commands.</span></span> <span data-ttu-id="08fa6-125">В последней спецификации перечислены команды подединицы.</span><span class="sxs-lookup"><span data-stu-id="08fa6-125">The latter specification lists the subunit commands.</span></span>

<span data-ttu-id="08fa6-126">Метод **жеттранспортбасикпараметерс** может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="08fa6-126">The **GetTransportBasicParameters** method may return one of the following error codes:</span></span>



| <span data-ttu-id="08fa6-127">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="08fa6-127">Error Code</span></span>              | <span data-ttu-id="08fa6-128">Описание</span><span class="sxs-lookup"><span data-stu-id="08fa6-128">Description</span></span>                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="08fa6-129">\_время ожидания ошибки</span><span class="sxs-lookup"><span data-stu-id="08fa6-129">ERROR\_TIMEOUT</span></span>          | <span data-ttu-id="08fa6-130">Время ожидания команды истекло.</span><span class="sxs-lookup"><span data-stu-id="08fa6-130">The command timed out.</span></span>                                                           |
| <span data-ttu-id="08fa6-131">Ошибка \_ req \_ не \_ акцеп</span><span class="sxs-lookup"><span data-stu-id="08fa6-131">ERROR\_REQ\_NOT\_ACCEP</span></span>  | <span data-ttu-id="08fa6-132">Устройство не приняло команду.</span><span class="sxs-lookup"><span data-stu-id="08fa6-132">The device did not accept the command.</span></span>                                           |
| <span data-ttu-id="08fa6-133">Ошибка \_ не \_ поддерживается</span><span class="sxs-lookup"><span data-stu-id="08fa6-133">ERROR\_NOT\_SUPPORTED</span></span>   | <span data-ttu-id="08fa6-134">Устройство не поддерживает команду.</span><span class="sxs-lookup"><span data-stu-id="08fa6-134">The device does not support the command.</span></span>                                         |
| <span data-ttu-id="08fa6-135">запрос на ошибку \_ \_ прерван</span><span class="sxs-lookup"><span data-stu-id="08fa6-135">ERROR\_REQUEST\_ABORTED</span></span> | <span data-ttu-id="08fa6-136">Команда была прервана.</span><span class="sxs-lookup"><span data-stu-id="08fa6-136">The command was aborted.</span></span> <span data-ttu-id="08fa6-137">Поссбли устройство удалено или произошла сброс шины.</span><span class="sxs-lookup"><span data-stu-id="08fa6-137">Possbly the device was removed or a bus reset occurred.</span></span> |



 

> [!Note]  
> <span data-ttu-id="08fa6-138">Эти ошибки возвращаются в виде кодов ошибок Win32, а не значений HRESULT, поэтому следует проверить эти значения напрямую, вместо того чтобы использовать макросы с **успехом** и **сбоем** .</span><span class="sxs-lookup"><span data-stu-id="08fa6-138">These errors are returned as Win32 error codes, not HRESULTs, so you should test for these values directly, rather than using the **SUCCEEDED** and **FAILED** macros.</span></span>

 

<span data-ttu-id="08fa6-139">Если метод возвращает значение S \_ , ответ от устройства копируется в массив.</span><span class="sxs-lookup"><span data-stu-id="08fa6-139">If the method returns S\_OK, the response from the device is copied into the array.</span></span> <span data-ttu-id="08fa6-140">Полезные данные ответа могут быть больше, чем команда, поэтому необходимо выделить буфер, достаточно большой для его хранения.</span><span class="sxs-lookup"><span data-stu-id="08fa6-140">The response payload might be larger than the command, so you must allocate a buffer large enough to hold it.</span></span> <span data-ttu-id="08fa6-141">Максимальный размер полезных данных — 512 байт.</span><span class="sxs-lookup"><span data-stu-id="08fa6-141">The maximum payload size is 512 bytes.</span></span> <span data-ttu-id="08fa6-142">Обратите внимание, что возвращаемое значение S \_ OK не всегда означает, что устройство успешно выполнило команду.</span><span class="sxs-lookup"><span data-stu-id="08fa6-142">Note that a return value of S\_OK does not always mean the device successfully carried out the command.</span></span> <span data-ttu-id="08fa6-143">Чтобы определить состояние, приложение должно проверить полезные данные ответа.</span><span class="sxs-lookup"><span data-stu-id="08fa6-143">The application must examine the response payload to determine the status.</span></span>

<span data-ttu-id="08fa6-144">В следующем примере показана команда для поиска абсолютного номера записи.</span><span class="sxs-lookup"><span data-stu-id="08fa6-144">The following example shows the command to search for an absolute track number search:</span></span>


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a><span data-ttu-id="08fa6-145">См. также</span><span class="sxs-lookup"><span data-stu-id="08fa6-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08fa6-146">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="08fa6-146">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



