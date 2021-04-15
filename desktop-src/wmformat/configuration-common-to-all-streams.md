---
title: Общая конфигурация для всех потоков
description: Общая конфигурация для всех потоков
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- профили, конфигурации, общие для всех потоков
- потоки, общие конфигурации
- потоки, имена
- потоки, имена соединений
- потоки, числа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104412723"
---
# <a name="configuration-common-to-all-streams"></a><span data-ttu-id="98a09-108">Общая конфигурация для всех потоков</span><span class="sxs-lookup"><span data-stu-id="98a09-108">Configuration Common to All Streams</span></span>

<span data-ttu-id="98a09-109">Всем потокам, независимо от типа, следует назначить имя потока, имя соединения и номер потока.</span><span class="sxs-lookup"><span data-stu-id="98a09-109">All streams, regardless of type, should be assigned a stream name, a connection name, and a stream number.</span></span>

<span data-ttu-id="98a09-110">Имя потока — это просто описательное имя, присваиваемое потоку.</span><span class="sxs-lookup"><span data-stu-id="98a09-110">The stream name is simply a descriptive name you assign to the stream.</span></span> <span data-ttu-id="98a09-111">Поток не обязательно должен иметь имя потока, но он помогает опознать поток при изменении профиля позже.</span><span class="sxs-lookup"><span data-stu-id="98a09-111">A stream does not need to have a stream name, but it helps you to identify the stream when editing the profile at a later time.</span></span> <span data-ttu-id="98a09-112">Вы можете задать имя для потока, вызвав [**ивмстреамконфиг:: сетстреамнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span><span class="sxs-lookup"><span data-stu-id="98a09-112">You can set a name for the stream by calling [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span></span>

<span data-ttu-id="98a09-113">Каждый поток должен иметь имя соединения, которое также называется входным именем.</span><span class="sxs-lookup"><span data-stu-id="98a09-113">Every stream should have a connection name, also called an input name.</span></span> <span data-ttu-id="98a09-114">При настройке профиля в объекте модуля записи для записи файла модуль записи связывает имя каждого подключения с входными данными.</span><span class="sxs-lookup"><span data-stu-id="98a09-114">When you set the profile in the writer object to write a file, the writer will associate each connection name with an input.</span></span> <span data-ttu-id="98a09-115">Для определения входных данных необходимо вызвать метод [**ивминпутмедиапропс:: жетконнектионнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) , чтобы получить имя соединения.</span><span class="sxs-lookup"><span data-stu-id="98a09-115">To identify the inputs, you must call [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) to retrieve the connection name.</span></span> <span data-ttu-id="98a09-116">Типичные имена соединений являются простыми описаниями содержимого, например "Audio".</span><span class="sxs-lookup"><span data-stu-id="98a09-116">Typical connection names are simple descriptions of the content, such as "audio".</span></span> <span data-ttu-id="98a09-117">Если профиль содержит потоки, которые являются взаимоисключающими по скорости потока, то каждый из взаимоисключающих потоков должен иметь одинаковое имя соединения.</span><span class="sxs-lookup"><span data-stu-id="98a09-117">If your profile contains streams that are mutually exclusive by bit rate, each of the mutually exclusive streams must have the same connection name.</span></span> <span data-ttu-id="98a09-118">Если это не так, профиль является недопустимым и будет отклонен модулем записи.</span><span class="sxs-lookup"><span data-stu-id="98a09-118">If they do not, the profile is invalid and will be rejected by the writer.</span></span> <span data-ttu-id="98a09-119">Имя соединения можно задать, вызвав [**ивмстреамконфиг:: сетконнектионнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span><span class="sxs-lookup"><span data-stu-id="98a09-119">You can set a connection name by calling [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span></span>

<span data-ttu-id="98a09-120">Номер потока определяет поток внутри файла.</span><span class="sxs-lookup"><span data-stu-id="98a09-120">The stream number identifies the stream within the file.</span></span> <span data-ttu-id="98a09-121">В отличие от входных и выходных номеров, Номера потоков начинаются с 1, а не 0.</span><span class="sxs-lookup"><span data-stu-id="98a09-121">Unlike input numbers and output numbers, stream numbers start at 1, not 0.</span></span> <span data-ttu-id="98a09-122">Номер потока отличается от индекса потока, который используется при получении потоков в профиле с помощью [**ивмпрофиле::-Stream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="98a09-122">A stream number is different than a stream index, which you use when getting streams in a profile by using [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span> <span data-ttu-id="98a09-123">Индекс потока — это число, присвоенное потоку объектом Profile.</span><span class="sxs-lookup"><span data-stu-id="98a09-123">The stream index is a number assigned to the stream by the profile object.</span></span> <span data-ttu-id="98a09-124">Индексы потоков находятся в диапазоне от 0 до числа потоков, полученных с помощью [**ивмпрофиле:: жетстреамкаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span><span class="sxs-lookup"><span data-stu-id="98a09-124">Stream indexes range between 0 and one less than the number of streams retrieved by [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span></span> <span data-ttu-id="98a09-125">Номера потоков не должны быть последовательными, хотя обычно они и могут находиться в диапазоне от 1 до 63.</span><span class="sxs-lookup"><span data-stu-id="98a09-125">Stream numbers need not be sequential, though they usually are, and can range from 1 to 63.</span></span> <span data-ttu-id="98a09-126">Вы можете задать номер потока, вызвав [**ивмстреамконфиг:: сетстреамнумбер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span><span class="sxs-lookup"><span data-stu-id="98a09-126">You can set a stream number by calling [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span></span>

## <a name="related-topics"></a><span data-ttu-id="98a09-127">См. также</span><span class="sxs-lookup"><span data-stu-id="98a09-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98a09-128">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="98a09-128">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="98a09-129">**Входы, потоки и выходные данные**</span><span class="sxs-lookup"><span data-stu-id="98a09-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




