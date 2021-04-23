---
title: Шифрование и импорт примеров мультимедиа
description: Шифрование и импорт примеров мультимедиа
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows Media Format SDK, импорт DRM
- Windows Media Format SDK, импорт
- Windows Media Format SDK, примеры шифрования носителей
- Управление цифровыми правами (DRM), импорт
- DRM (Управление цифровыми правами), импорт
- Управление цифровыми правами (DRM), примеры шифрования носителей
- DRM (Управление цифровыми правами), шифрование образцов мультимедиа
- Расширенные API клиента DRM, импорт
- Расширенные API клиента, импорт
- Расширенные API клиента DRM, шифрование образцов мультимедиа
- Расширенные API клиента, шифрование образцов мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412504"
---
# <a name="encrypting-and-importing-media-samples"></a><span data-ttu-id="432ce-114">Шифрование и импорт примеров мультимедиа</span><span class="sxs-lookup"><span data-stu-id="432ce-114">Encrypting and Importing Media Samples</span></span>

<span data-ttu-id="432ce-115">Для каждого примера носителя, зашифрованного с помощью Windows Media DRM, необходимо создать расширяющее значение, которое должно быть строго больше предыдущего (монотонно возрастает).</span><span class="sxs-lookup"><span data-stu-id="432ce-115">For each media sample that you encrypt using Windows Media DRM, you must generate a salt value that is strictly bigger than the previous one (monotonically increasing).</span></span> <span data-ttu-id="432ce-116">Используйте новое расширяющее значение, чтобы создать транзитный ключ шифрования, применяя алгоритм шифрования SHA-1 к вектору инициализации, сцепленному с расширяющим значением.</span><span class="sxs-lookup"><span data-stu-id="432ce-116">Use the new salt value to create a transitory encryption key by applying the SHA-1 encryption algorithm to the initialization vector concatenated with the salt value.</span></span>

<span data-ttu-id="432ce-117">Затем зашифровать пример в соответствии с алгоритмом RC4, используя созданный транзитный ключ.</span><span class="sxs-lookup"><span data-stu-id="432ce-117">Next, encrypt the sample according to the RC4 algorithm using the generated transitory key.</span></span> <span data-ttu-id="432ce-118">Перед передачей образца в пакет SDK приложение должно связать значение соли с примером, задав атрибут расширения.</span><span class="sxs-lookup"><span data-stu-id="432ce-118">Before the sample is passed to the SDK, your application must associate the salt value with the sample by setting an extension attribute.</span></span>

<span data-ttu-id="432ce-119">Ниже приведены шаги для шифрования примеров носителей.</span><span class="sxs-lookup"><span data-stu-id="432ce-119">Here are the steps for encrypting media samples:</span></span>

1.  <span data-ttu-id="432ce-120">Вызовите метод **QueryInterface** образца объекта, чтобы получить интерфейс [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="432ce-120">Call the **QueryInterface** method of the sample object to get the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface.</span></span>
2.  <span data-ttu-id="432ce-121">Увеличение расширяющего значения.</span><span class="sxs-lookup"><span data-stu-id="432ce-121">Increment the salt value.</span></span>
3.  <span data-ttu-id="432ce-122">Зашифровать пример с помощью алгоритма шифрования RC1.</span><span class="sxs-lookup"><span data-stu-id="432ce-122">Encrypt the sample using an RC1 encryption algorithm.</span></span> <span data-ttu-id="432ce-123">Для шифрования создается ключ путем сцепления вектора инициализации и расширяющего значения.</span><span class="sxs-lookup"><span data-stu-id="432ce-123">For the encryption you create a key by concatenating the initialization vector and the salt value.</span></span>
4.  <span data-ttu-id="432ce-124">Укажите значение соли для пакета SDK, вызвав метод [**инссбуффер:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="432ce-124">Provide the salt value to the SDK by calling [**INSSBuffer::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="432ce-125">См. также</span><span class="sxs-lookup"><span data-stu-id="432ce-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="432ce-126">**Импорт DRM**</span><span class="sxs-lookup"><span data-stu-id="432ce-126">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="432ce-127">**Пример шифрования мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="432ce-127">**Media Sample Encryption Example**</span></span>](media-sample-encryption-example.md)
</dt> </dl>

 

 




