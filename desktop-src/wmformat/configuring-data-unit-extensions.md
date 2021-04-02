---
title: Настройка расширений модуля данных
description: Настройка расширений модуля данных
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- потоки, Настройка расширений модулей данных
- потоки, расширения модулей данных
- расширения модулей данных, Настройка
- профили, расширения модулей данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789181"
---
# <a name="configuring-data-unit-extensions"></a><span data-ttu-id="a4ae2-107">Настройка расширений модуля данных</span><span class="sxs-lookup"><span data-stu-id="a4ae2-107">Configuring Data Unit Extensions</span></span>

<span data-ttu-id="a4ae2-108">Примеры, записанные в файлы ASF, могут содержать дополнительные сведения, помимо самих примеров носителей.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-108">Samples written to ASF files can contain additional information apart from the media samples themselves.</span></span> <span data-ttu-id="a4ae2-109">Эти сведения включаются с помощью модулей обработки данных.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-109">This information is included using data unit extensions.</span></span> <span data-ttu-id="a4ae2-110">Дополнительные сведения о расширениях модулей данных см. в разделе [модули данных](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a4ae2-110">For more information about data unit extensions, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="a4ae2-111">Чтобы использовать расширения единиц данных, необходимо настроить поток в профиле, чтобы принять их.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-111">To use data unit extensions, you must configure the stream in the profile to accept them.</span></span> <span data-ttu-id="a4ae2-112">Чтобы настроить расширение единицы обработки данных для потока, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-112">To configure a data unit extension for a stream, perform the following steps.</span></span>

1.  <span data-ttu-id="a4ae2-113">Получите указатель на интерфейс [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) , вызвав метод **QueryInterface** [**ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="a4ae2-113">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface by calling the **QueryInterface** method of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span>
2.  <span data-ttu-id="a4ae2-114">Вызовите метод [**IWMStreamConfig2:: адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) , чтобы зарегистрировать тип расширения единицы данных для потока.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-114">Call [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) to register a type of data unit extension for the stream.</span></span>

<span data-ttu-id="a4ae2-115">Вы можете изучить все типы расширений единиц данных, зарегистрированные для потока, вызвав [**IWMStreamConfig2:: жетдатаунитекстенсионкаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) , чтобы получить количество зарегистрированных типов модулей данных.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-115">You can examine all of the data unit extension types currently registered for a stream by calling [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) to retrieve the number of registered data unit extension types.</span></span> <span data-ttu-id="a4ae2-116">Затем можно выполнить цикл по всем типам, используя вызовы [**IWMStreamConfig2:: жетдатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-116">Then you can loop through all of the types using calls to [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) for each.</span></span>

<span data-ttu-id="a4ae2-117">Расширениям модулей данных назначается размер при настройке потока.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-117">Data unit extensions are assigned a size when configured for a stream.</span></span> <span data-ttu-id="a4ae2-118">Многие системы расширений модулей данных используют данные, которые имеют постоянный размер (обычно это структура).</span><span class="sxs-lookup"><span data-stu-id="a4ae2-118">Many data unit extension systems use data that is a constant size (usually a structure).</span></span> <span data-ttu-id="a4ae2-119">Тем не менее можно также настроить для модулей обработки данных размер переменного размера, задав для параметра Размер значение 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-119">However, you can also configure your data unit extensions to be of variable size by setting the size to 0xFFFF.</span></span> <span data-ttu-id="a4ae2-120">Каждое расширение единицы данных, назначенное во время кодирования, может иметь любой размер от 1 до 65534 байт.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-120">Each data unit extension assigned at encoding time can then be of any size between 1 byte and 65534 bytes.</span></span> <span data-ttu-id="a4ae2-121">Вариаблиные расширения единиц обработки данных также называются динамическими модулями данных.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-121">Variably sized data unit extensions are also called dynamic data unit extensions.</span></span>

<span data-ttu-id="a4ae2-122">Преимущество использования динамических модулей обработки данных заключается в том, что при необходимости можно присоединить данные расширения.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-122">The advantage of using dynamic data unit extensions is that you can attach extension data as needed.</span></span> <span data-ttu-id="a4ae2-123">Если вы определили расширение единицы данных с заданным размером, каждый пример для потока должен содержать данные расширения этого размера, даже если для некоторых образцов нет данных.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-123">If you define a data unit extension with a set size, every sample for the stream must contain extension data of that size, even if you have no data for some samples.</span></span> <span data-ttu-id="a4ae2-124">С помощью динамических модулей обработки данных можно опустить расширения модулей данных из некоторых примеров, что экономит пространство и сокращает требования к пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-124">With dynamic data unit extensions, you can omit data unit extensions from some samples, which saves space and reduces bandwidth requirements.</span></span> <span data-ttu-id="a4ae2-125">Однако если расширения модулей данных имеют переменный размер, объект чтения не может проверить полученные данные расширения на статический размер.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-125">However, if data unit extensions are of variable size, the reading object cannot verify the received extension data against a static size.</span></span> <span data-ttu-id="a4ae2-126">Необходимо убедиться, что получаемые данные расширения являются допустимыми, а не вредоносное искажение потока битов.</span><span class="sxs-lookup"><span data-stu-id="a4ae2-126">You must verify that the extension data that you receive is valid, and not malicious distortion of the bit stream.</span></span>

<span data-ttu-id="a4ae2-127">Отдельные расширения модулей данных должны быть установлены для выборок с помощью метода [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="a4ae2-127">Individual data unit extensions must be set on samples by using the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="a4ae2-128">Дополнительные сведения см. в разделе [Задание модулей обработки данных](setting-data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a4ae2-128">For more information, see [Setting Data Unit Extensions](setting-data-unit-extensions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4ae2-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a4ae2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4ae2-130">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="a4ae2-130">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




