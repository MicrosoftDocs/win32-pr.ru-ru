---
title: Зачем использовать платформу текстовых служб
description: Зачем использовать платформу текстовых служб
ms.assetid: 64b3b0a1-7740-49fa-b0a6-f80040147280
keywords:
- Платформа текстовых служб (TSF), сведения
- TSF (платформа текстовых служб), сведения
- службы текстового ввода, сведения
- Приложения с поддержкой TSF, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6647981b890bd1fcdf488b18bffad587f49ed9b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681388"
---
# <a name="why-use-text-services-framework"></a><span data-ttu-id="279fd-107">Зачем использовать платформу текстовых служб?</span><span class="sxs-lookup"><span data-stu-id="279fd-107">Why Use Text Services Framework?</span></span>

<span data-ttu-id="279fd-108">Платформа текстовых служб (TSF) позволяет приложению с поддержкой TSF принимать текстовые данные из любого числа устройств или источников.</span><span class="sxs-lookup"><span data-stu-id="279fd-108">Text Services Framework (TSF) enables a TSF-enabled application to receive text input from any number of devices or sources.</span></span> <span data-ttu-id="279fd-109">Поскольку TSF является расширяемой, приложение может принимать текстовые входные данные из дополнительных текстовых источников с минимальными изменениями или без них.</span><span class="sxs-lookup"><span data-stu-id="279fd-109">Because TSF is extensible, the application can receive text input from additional text sources with little or no modification.</span></span>

<span data-ttu-id="279fd-110">Служба текстового ввода получает текст из и предоставляет текст в любое приложение с поддержкой TSF, не требуя знания о приложении.</span><span class="sxs-lookup"><span data-stu-id="279fd-110">A text service obtains text from, and provides text to, any TSF-enabled application without requiring any knowledge about the application.</span></span> <span data-ttu-id="279fd-111">Эта структура обеспечивает доступ к текстовой службе любому приложению с поддержкой TSF.</span><span class="sxs-lookup"><span data-stu-id="279fd-111">This structure enables the text service to be available to any TSF-enabled application.</span></span> <span data-ttu-id="279fd-112">Службу текстового ввода можно установить или обновить как отдельный модуль и не зависеть от конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="279fd-112">The text service can be installed or updated as a separate module and is independent of any specific application.</span></span> <span data-ttu-id="279fd-113">TSF также позволяет текстовой службе хранить метаданные с документом, фрагментом текста или объектом в документе.</span><span class="sxs-lookup"><span data-stu-id="279fd-113">TSF also enables a text service to store metadata with a document, a piece of text, or an object within the document.</span></span> <span data-ttu-id="279fd-114">Например, служба текстового ввода речи может хранить звуковые данные, связанные с блоком текста.</span><span class="sxs-lookup"><span data-stu-id="279fd-114">For example, a speech input text service can store sound information associated with a block of text.</span></span>

<span data-ttu-id="279fd-115">TSF позволяет текстовым службам обеспечить точное и полное преобразование текста с непрерывным доступом к буферу документа.</span><span class="sxs-lookup"><span data-stu-id="279fd-115">TSF enables text services to provide accurate and complete text conversion, with continuous access to the document buffer.</span></span> <span data-ttu-id="279fd-116">Текстовые службы, использующие TSF, могут не разделять свои функциональные возможности на режимы для ввода и режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="279fd-116">Text services using TSF can avoid separating their functionality into modes for input and modes for editing.</span></span> <span data-ttu-id="279fd-117">Эта архитектура ввода позволяет динамически изменять буферизованный и накопленный текстовый поток, тем самым обеспечивая более эффективный ввод с клавиатуры и редактирование текста.</span><span class="sxs-lookup"><span data-stu-id="279fd-117">This input architecture enables the buffered and accumulating text stream to change dynamically, thereby enabling more efficient keyboard input and text editing.</span></span>

<span data-ttu-id="279fd-118">TSF не зависит от устройства и включает текстовые службы для нескольких устройств ввода, включая клавиатуру, перо и микрофон.</span><span class="sxs-lookup"><span data-stu-id="279fd-118">TSF is device-independent and enables text services for multiple input devices including keyboard, pen, and microphone.</span></span>

 

 




