---
title: Перечисление приемников
description: Перечисление приемников
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Расширенный формат систем (ASF), перечисление приемников
- ASF (Расширенный системный формат), перечисление приемников
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- приемники, перечисление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789169"
---
# <a name="enumerating-sinks"></a><span data-ttu-id="935d7-108">Перечисление приемников</span><span class="sxs-lookup"><span data-stu-id="935d7-108">Enumerating Sinks</span></span>

<span data-ttu-id="935d7-109">С модулем записи может быть связано несколько приемников.</span><span class="sxs-lookup"><span data-stu-id="935d7-109">The writer can have many sinks associated with it.</span></span> <span data-ttu-id="935d7-110">Можно перечислить приемники, добавленные в модуль записи, с помощью [**ивмвритерадванцед:: жетсинккаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) и [**Ивмвритерадванцед:: Sink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span><span class="sxs-lookup"><span data-stu-id="935d7-110">You can enumerate the sinks that have been added to the writer by using [**IWMWriterAdvanced::GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) and [**IWMWriterAdvanced::GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span></span>

<span data-ttu-id="935d7-111">В примере кода в [сообщениях об ошибках из приемника](getting-error-messages-from-a-sink.md) демонстрируется перечисление приемника.</span><span class="sxs-lookup"><span data-stu-id="935d7-111">The example code in the [Getting Error Messages from a Sink](getting-error-messages-from-a-sink.md) demonstrates sink enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="935d7-112">При перечислении приемников файл по умолчанию, созданный в ответ на вызов [**ивмвритер:: сетаутпутфиленаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) , будет перечислен вместе с другими добавленными приемниками.</span><span class="sxs-lookup"><span data-stu-id="935d7-112">When enumerating sinks, the default file sink created in response to a call to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) will be enumerated along with any other sinks you have added.</span></span> <span data-ttu-id="935d7-113">Если вы используете только приемник файлов по умолчанию, вы можете получить к нему доступ, вызвав метод **sink** для индекса приемника 0.</span><span class="sxs-lookup"><span data-stu-id="935d7-113">If you are using only the default file sink, you can access it by calling **GetSink** for sink index 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="935d7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="935d7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="935d7-115">**Интерфейс Ивмвритерадванцед**</span><span class="sxs-lookup"><span data-stu-id="935d7-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="935d7-116">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="935d7-116">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




