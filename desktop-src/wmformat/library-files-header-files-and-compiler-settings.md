---
title: Файлы библиотек, файлы заголовков и параметры компилятора
description: Файлы библиотек, файлы заголовков и параметры компилятора
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- Windows Media Format SDK, файлы библиотек DRM
- Windows Media Format SDK, файлы библиотек
- Windows Media Format SDK, файлы заголовков DRM
- Windows Media Format SDK, файлы заголовков
- Windows Media Format SDK, параметры компилятора DRM
- Пакет SDK для формата Windows Media, параметры компилятора
- Управление цифровыми правами (DRM), файлы библиотек
- DRM (Управление цифровыми правами), файлы библиотек
- Управление цифровыми правами (DRM), файлы заголовков
- DRM (Управление цифровыми правами), файлы заголовков
- Управление цифровыми правами (DRM), параметры компилятора
- DRM (Управление цифровыми правами), параметры компилятора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132971"
---
# <a name="library-files-header-files-and-compiler-settings"></a><span data-ttu-id="c94c5-115">Файлы библиотек, файлы заголовков и параметры компилятора</span><span class="sxs-lookup"><span data-stu-id="c94c5-115">Library Files, Header Files, and Compiler Settings</span></span>

<span data-ttu-id="c94c5-116">Программные компоненты расширенных API клиента DRM Windows Media определяются в файле заголовка вмдрмсдк. h и реализуются в библиотеках вмдрмсдк. lib и мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="c94c5-116">The programming components of the Windows Media DRM Client Extended APIs are defined in the wmdrmsdk.h header file, and implemented in the wmdrmsdk.lib and mfuuid.lib libraries.</span></span>

<span data-ttu-id="c94c5-117">Некоторые функции расширенных API клиента DRM Windows Media требуют получения защищенной библиотеки от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c94c5-117">Some of the functionality of the Windows Media DRM Client Extended APIs requires that you obtain a protected library from Microsoft.</span></span> <span data-ttu-id="c94c5-118">Эта библиотека, называемая библиотекой заглушек в этой документации, относится к получателю и указывает уровень безопасности приложения для приложений.</span><span class="sxs-lookup"><span data-stu-id="c94c5-118">This library, called the stub library in this documentation, is specific to the recipient and specifies the application security level for your applications.</span></span> <span data-ttu-id="c94c5-119">Библиотека-заглушка заменяет вмдрмсдк. lib; никогда не следует ссылаться на оба.</span><span class="sxs-lookup"><span data-stu-id="c94c5-119">The stub library replaces wmdrmsdk.lib; you should never link to both.</span></span>

<span data-ttu-id="c94c5-120">**Примечание** . Библиотека заглушек DRM отличается от библиотеки-заглушки, используемой остальной частью пакета SDK Windows Media Format, но лицензируется с помощью того же метода.</span><span class="sxs-lookup"><span data-stu-id="c94c5-120">**Note** The DRM stub library is separate from the stub library used by the rest of the Windows Media Format SDK but is licensed using the same method.</span></span>

<span data-ttu-id="c94c5-121">**Примечание** . Библиотека заглушки DRM должна быть связана с приложением после файла библиотеки MSVCRT. lib, чтобы избежать ошибок компоновщика.</span><span class="sxs-lookup"><span data-stu-id="c94c5-121">**Note** The DRM stub library must be linked into your application after the library file msvcrt.lib to avoid linker errors.</span></span>

<span data-ttu-id="c94c5-122">Библиотека заглушек содержит внедренный сертификат, который может быть отозван корпорацией Майкрософт, если не соблюдены условия лицензионного соглашения.</span><span class="sxs-lookup"><span data-stu-id="c94c5-122">The stub library contains an embedded certificate which can be revoked by Microsoft if you fail to comply with the terms and conditions of the license agreement.</span></span>

<span data-ttu-id="c94c5-123">Конкретные методы, для которых требуется библиотека-заглушка, помечаются в документации.</span><span class="sxs-lookup"><span data-stu-id="c94c5-123">Specific methods that require the stub library are labeled in the documentation.</span></span> <span data-ttu-id="c94c5-124">Если вы попытаетесь использовать такой метод без привязки к библиотеке-заглушке, он возвратит ошибку NS \_ E \_ DRM \_ стублиб \_ Required.</span><span class="sxs-lookup"><span data-stu-id="c94c5-124">If you try to use such a method without linking to the stub library, it will return an NS\_E\_DRM\_STUBLIB\_REQUIRED error.</span></span>

<span data-ttu-id="c94c5-125">Подсистему DRM нельзя использовать в отладочной сборке.</span><span class="sxs-lookup"><span data-stu-id="c94c5-125">The DRM subsystem can not be used in a debug build.</span></span> <span data-ttu-id="c94c5-126">При последующей попыток методы API будут возвращать ошибку "ошибка при \_ \_ отладке DRM в NS" \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c94c5-126">If this is attempted, methods of the API will return the NS\_E\_DRM\_DEBUGGING\_NOT\_ALLOWED error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c94c5-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c94c5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c94c5-128">**Приступая к работе**</span><span class="sxs-lookup"><span data-stu-id="c94c5-128">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="c94c5-129">**Файлы библиотек и параметры компилятора**</span><span class="sxs-lookup"><span data-stu-id="c94c5-129">**Library Files and Compiler Settings**</span></span>](library-files-and-compiler-settings.md)
</dt> <dt>

[<span data-ttu-id="c94c5-130">**Получение требуемой библиотеки DRM**</span><span class="sxs-lookup"><span data-stu-id="c94c5-130">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




