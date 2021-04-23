---
description: Принудительная вставка ключевых кадров
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Принудительная вставка ключевых кадров (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496809"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a><span data-ttu-id="6f13f-103">Принудительная вставка ключевых кадров (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="6f13f-103">Forced Key Frame Insertion (Microsoft Media Foundation)</span></span>

<span data-ttu-id="6f13f-104">При настройке объекта видеокодировщика можно задать максимальный интервал для ключевых кадров в кодированном содержимом.</span><span class="sxs-lookup"><span data-stu-id="6f13f-104">When you configure a video encoder object, you can set a maximum interval for key frames in the encoded content.</span></span> <span data-ttu-id="6f13f-105">Однако кодек поместит ключевые кадры в пределах этого интервала, заменяя их содержимым. Интервал опорного кадра не является константой.</span><span class="sxs-lookup"><span data-stu-id="6f13f-105">However, the codec will place key frames within that interval as dictated by the content; the key frame interval is not constant.</span></span> <span data-ttu-id="6f13f-106">Для некоторых приложений очень важна дистанция ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="6f13f-106">For some applications, the key frame distance is very important.</span></span> <span data-ttu-id="6f13f-107">Например, приложение для редактирования видео нуждается в ключевых кадрах в расположениях, которые являются логическими для редактора, например в случае разрыва сцены и перехода на новую.</span><span class="sxs-lookup"><span data-stu-id="6f13f-107">For example, a video editing application needs key frames at locations that are logical to an editor, like at scene breaks and shot transitions.</span></span>

<span data-ttu-id="6f13f-108">Принудительная вставка ключевых кадров — это функция, которая позволяет запросить кодирование входного кадра в виде ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="6f13f-108">Forced key frame insertion is a feature that enables you to request that an input frame be encoded as a key frame.</span></span> <span data-ttu-id="6f13f-109">Кодировщик будет пытаться обработать эти запросы, но параметры буфера (скорость потока и окно буфера), настроенные для сеанса кодирования, всегда имеют приоритет.</span><span class="sxs-lookup"><span data-stu-id="6f13f-109">The encoder will try to honor these requests, but the buffer settings (bit rate and buffer window) configured for the encoding session always take precedence.</span></span>

<span data-ttu-id="6f13f-110">Объекты кодировщика видео реализуют принудительную вставку ключевых кадров в качестве ответа на расширение единицы данных, присоединенное к образцу ввода.</span><span class="sxs-lookup"><span data-stu-id="6f13f-110">The video encoder objects implement forced key frame insertion as a response to a data unit extension attached to the input sample.</span></span> <span data-ttu-id="6f13f-111">Дополнительные сведения о модулях обработки данных см. [в разделе Использование расширений модулей данных](usingdataunitextensions.md).</span><span class="sxs-lookup"><span data-stu-id="6f13f-111">For more information about data unit extensions, see [Using Data Unit Extensions](usingdataunitextensions.md).</span></span>

<span data-ttu-id="6f13f-112">Данные расширения для вставки принудительных ключевых кадров определяются следующим значением GUID: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span><span class="sxs-lookup"><span data-stu-id="6f13f-112">The extension data for forced key frame insertion is identified by the following GUID value: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span></span> <span data-ttu-id="6f13f-113">Отдельные расширения являются значениями типа **bool** .</span><span class="sxs-lookup"><span data-stu-id="6f13f-113">The individual extensions are **BOOL** values.</span></span> <span data-ttu-id="6f13f-114">Установите значение **true** , чтобы указать запрос опорного кадра.</span><span class="sxs-lookup"><span data-stu-id="6f13f-114">Set the value to **TRUE** to indicate a key frame request.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f13f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="6f13f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f13f-116">Использование модулей обработки данных</span><span class="sxs-lookup"><span data-stu-id="6f13f-116">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
</dt> <dt>

[<span data-ttu-id="6f13f-117">Работа с видео</span><span class="sxs-lookup"><span data-stu-id="6f13f-117">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



