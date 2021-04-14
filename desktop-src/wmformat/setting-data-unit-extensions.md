---
title: Настройка модулей обработки данных
description: Настройка модулей обработки данных
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Расширенный системный формат (ASF), расширения модулей данных
- ASF (Расширенный системный формат), расширения модулей данных
- расширения модулей данных, Настройка
- потоки, расширения модулей данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104533047"
---
# <a name="setting-data-unit-extensions"></a><span data-ttu-id="f2df1-107">Настройка модулей обработки данных</span><span class="sxs-lookup"><span data-stu-id="f2df1-107">Setting Data Unit Extensions</span></span>

<span data-ttu-id="f2df1-108">Некоторые потоки настроены на использование расширений модулей данных для связи дополнительных данных с отдельными примерами.</span><span class="sxs-lookup"><span data-stu-id="f2df1-108">Some streams are configured to use data unit extensions to associate supplementary data with individual samples.</span></span> <span data-ttu-id="f2df1-109">Дополнительные сведения о расширенных примерах см. в разделе [расширения модулей данных](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="f2df1-109">For more information about extended samples, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="f2df1-110">Большинству систем расширения единиц обработки данных требуется расширение для каждого примера в потоке.</span><span class="sxs-lookup"><span data-stu-id="f2df1-110">Most data unit extension systems require an extension on every sample in the stream.</span></span> <span data-ttu-id="f2df1-111">Если расширение нужного размера не будет предоставлено, модуль записи отклонит пример.</span><span class="sxs-lookup"><span data-stu-id="f2df1-111">If you do not provide an extension of the correct size, the writer will reject the sample.</span></span>

<span data-ttu-id="f2df1-112">Чтобы добавить Расширенные данные в образец, используйте метод [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="f2df1-112">To add extended data to a sample, use the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="f2df1-113">Сведения о расширениях модулей данных, настроенных в потоке, можно получить с помощью методов [**IWMStreamConfig2:: жетдатаунитекстенсионкаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) и [**IWMStreamConfig2:: жетдатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="f2df1-113">You can get information about the data unit extensions configured on a stream by using the [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) and [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2df1-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f2df1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2df1-115">**Настройка расширений модуля данных**</span><span class="sxs-lookup"><span data-stu-id="f2df1-115">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="f2df1-116">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="f2df1-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




