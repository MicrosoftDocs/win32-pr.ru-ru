---
title: Повторное использование конфигураций потоков
description: Повторное использование конфигураций потоков
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- потоки, повторное использование конфигураций
- профили, повторное использование конфигураций потоков
- повторное использование конфигураций потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af10fd026904ccef33aba28d28e0e6a4975d3fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105681580"
---
# <a name="reusing-stream-configurations"></a><span data-ttu-id="980cf-106">Повторное использование конфигураций потоков</span><span class="sxs-lookup"><span data-stu-id="980cf-106">Reusing Stream Configurations</span></span>

<span data-ttu-id="980cf-107">Часто бывают случаи, когда необходимо повторно использовать объект конфигурации потока из существующего профиля.</span><span class="sxs-lookup"><span data-stu-id="980cf-107">There are often times when you want to reuse a stream configuration object from an existing profile.</span></span> <span data-ttu-id="980cf-108">Возможно, у вас есть старые профили, которые нуждаются в обновлении, или в системном профиле может потребоваться поток, идентичный одному.</span><span class="sxs-lookup"><span data-stu-id="980cf-108">You may have old profiles that need updating or you may need a stream identical to one in a system profile.</span></span> <span data-ttu-id="980cf-109">Гораздо проще использовать конфигурации потоков, чем создавать новые, и часто можно изменить несколько параметров в конфигурации в соответствии с вашими потребностями, а не создавать совершенно новые.</span><span class="sxs-lookup"><span data-stu-id="980cf-109">It is easier to reuse stream configurations than to create new ones, and you can often change a few settings in a configuration to meet your needs rather than creating an entirely new one.</span></span>

<span data-ttu-id="980cf-110">Имейте в виду, что существуют ограничения на изменение конфигурации потока.</span><span class="sxs-lookup"><span data-stu-id="980cf-110">Be aware that there are limitations to how you can change stream configurations.</span></span> <span data-ttu-id="980cf-111">При неправильном изменении параметров профиль может не принять объект конфигурации потока.</span><span class="sxs-lookup"><span data-stu-id="980cf-111">If you change settings in the wrong way, your profile may not accept the stream configuration object.</span></span> <span data-ttu-id="980cf-112">Неправильные конфигурации потока часто принимаются профилем, но вызывают отклонения профиля объектом модуля записи.</span><span class="sxs-lookup"><span data-stu-id="980cf-112">Incorrect stream configurations are frequently accepted by the profile but cause the writer object to reject the profile.</span></span> <span data-ttu-id="980cf-113">При использовании и изменении существующих конфигураций потоков учитывайте следующие ограничения и проблемы.</span><span class="sxs-lookup"><span data-stu-id="980cf-113">Be aware of the following limitations and issues when using and modifying existing stream configurations.</span></span>

-   <span data-ttu-id="980cf-114">Никогда не изменяйте содержимое файла пркс для изменения параметров потока.</span><span class="sxs-lookup"><span data-stu-id="980cf-114">Never alter the contents of a .prx file to change stream settings.</span></span> <span data-ttu-id="980cf-115">Когда профили сохраняются в XML-строки и записываются в файл. пркс, они могут быть считаны любым текстовым редактором.</span><span class="sxs-lookup"><span data-stu-id="980cf-115">When profiles are saved to XML strings and written to a .prx file they can be read with any text editor.</span></span> <span data-ttu-id="980cf-116">Просмотр сохраненного профиля поможет понять, как работают профили.</span><span class="sxs-lookup"><span data-stu-id="980cf-116">Looking at a saved profile can help you understand how profiles work.</span></span> <span data-ttu-id="980cf-117">Тем не менее, не следует изменять файл пркс каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="980cf-117">However, you should never alter a .prx file in any way.</span></span> <span data-ttu-id="980cf-118">Даже кажется, что тривиальные изменения могут сделать профиль недействительным.</span><span class="sxs-lookup"><span data-stu-id="980cf-118">Even seemingly trivial changes can invalidate the profile.</span></span>
-   <span data-ttu-id="980cf-119">Несколько версий аудиокодека Windows Media используют одни и те же конфигурации потока.</span><span class="sxs-lookup"><span data-stu-id="980cf-119">Several versions of the Windows Media Audio codec use the same stream configurations.</span></span> <span data-ttu-id="980cf-120">При наличии объекта конфигурации потока, настроенного как подтип ВММЕДИАСУБТИПЕ \_ WMAudioV2, вммедиасубтипе \_ WMAUDIOV7 или вммедиасубтипе \_ WMAudioV8, полученный поток будет сжат с использованием последнего аудиокодека Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="980cf-120">If you have a stream configuration object that is configured as subtype WMMEDIASUBTYPE\_WMAudioV2, WMMEDIASUBTYPE\_WMAudioV7, or WMMEDIASUBTYPE\_WMAudioV8, the resulting stream will be compressed with the latest Windows Media Audio codec.</span></span> <span data-ttu-id="980cf-121">Тем не менее следует оценить потребности перед использованием существующего аудиокодека.</span><span class="sxs-lookup"><span data-stu-id="980cf-121">However, you should evaluate your needs before using an existing audio codec.</span></span> <span data-ttu-id="980cf-122">Многие типы файлов можно улучшить путем обновления до последней версии кодека Windows Media Audio Professional или кодека Windows Media Audio без него.</span><span class="sxs-lookup"><span data-stu-id="980cf-122">Many types of files can be improved by upgrading to the latest version of the Windows Media Audio Professional codec, or the Windows Media Audio Lossless codec.</span></span>
-   <span data-ttu-id="980cf-123">Никогда не изменяйте подтип потока для обновления до нового кодека.</span><span class="sxs-lookup"><span data-stu-id="980cf-123">Never change the subtype of a stream to upgrade to a new codec.</span></span> <span data-ttu-id="980cf-124">При использовании методов [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) для получения конфигурации потока кодек присоединяет к нему некоторые данные, определяющие формат потока битов.</span><span class="sxs-lookup"><span data-stu-id="980cf-124">When you use the methods of [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) to obtain a stream configuration, the codec attaches some data to it that identifies the bit stream format.</span></span> <span data-ttu-id="980cf-125">При изменении подтипа существующего объекта конфигурации потока подтип не будет соответствовать данным кодека.</span><span class="sxs-lookup"><span data-stu-id="980cf-125">If you change the subtype of an existing stream configuration object, the subtype will not match the codec data.</span></span> <span data-ttu-id="980cf-126">Объект модуля записи не будет принимать профиль с такой конфигурацией потока.</span><span class="sxs-lookup"><span data-stu-id="980cf-126">A profile with such a stream configuration will not be accepted by the writer object.</span></span>
-   <span data-ttu-id="980cf-127">Не изменяйте параметры сжатых конфигураций аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="980cf-127">Do not alter the settings of compressed audio stream configurations.</span></span> <span data-ttu-id="980cf-128">Если параметры звукового потока не соответствуют вашим потребностям, получите новую конфигурацию потока из кодека, используя методы **IWMCodecInfo3**.</span><span class="sxs-lookup"><span data-stu-id="980cf-128">If the settings of an audio stream do not suit your needs, obtain a new stream configuration from the codec using the methods of **IWMCodecInfo3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="980cf-129">См. также</span><span class="sxs-lookup"><span data-stu-id="980cf-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="980cf-130">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="980cf-130">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="980cf-131">**Получение сведений о конфигурации потока из кодеков**</span><span class="sxs-lookup"><span data-stu-id="980cf-131">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




