---
description: Хотя&\# 160; контекст распознавателя&\# 160; недоступен в двух потоках одновременно платформой Tablet PC, функция адвисеинкчанже может быть вызвана в любое время в любом потоке.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Рекомендации по потокам распознавателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702681"
---
# <a name="recognizer-threading-considerations"></a><span data-ttu-id="8edc3-103">Рекомендации по потокам распознавателя</span><span class="sxs-lookup"><span data-stu-id="8edc3-103">Recognizer Threading Considerations</span></span>

<span data-ttu-id="8edc3-104">Несмотря на то, что доступ к [контексту распознавателя](hrecocontext-handle.md) невозможен в двух потоках одновременно платформой Tablet PC, функция [**адвисеинкчанже**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) может быть вызвана в любое время в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="8edc3-104">Although a [recognizer context](hrecocontext-handle.md) cannot be accessed on two threads simultaneously by the Tablet PC platform, the [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) function can be called at any time on any thread.</span></span> <span data-ttu-id="8edc3-105">Поскольку платформа Tablet PC не гарантирует, что в каждый момент времени существует только один контекст распознавателя, два отдельных контекста распознавателя в отдельных потоках могут одновременно попытаться получить доступ к [распознавателю](hrecognizer-handle.md).</span><span class="sxs-lookup"><span data-stu-id="8edc3-105">Because the Tablet PC platform does not ensure that there is only one recognizer context at a time, two separate recognizer contexts in separate threads may simultaneously attempt to access your [recognizer](hrecognizer-handle.md).</span></span> <span data-ttu-id="8edc3-106">Таким образом, глобальные переменные в подсистеме распознавания должны быть потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="8edc3-106">Therefore, global variables in your recognition engine must be thread-safe.</span></span>

<span data-ttu-id="8edc3-107">Списки слов являются необязательными реализациями, используемыми для повышения точности.</span><span class="sxs-lookup"><span data-stu-id="8edc3-107">Word lists are an optional implementation used to increase accuracy.</span></span> <span data-ttu-id="8edc3-108">Если распознаватель реализует списки слов, он должен быть потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="8edc3-108">If your recognizer implements word lists, it must be thread-safe.</span></span> <span data-ttu-id="8edc3-109">Дополнительные сведения об использовании списков Word см. [в разделе Использование словарей приложений](using-application-dictionaries.md).</span><span class="sxs-lookup"><span data-stu-id="8edc3-109">For more information about using word lists, see [Using Application Dictionaries](using-application-dictionaries.md).</span></span>

<span data-ttu-id="8edc3-110">Дополнительные сведения о других вопросах, связанных с потоками, см. в статье [вопросы многопоточной обработки в планшетных ПК](tablet-pc-threading-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="8edc3-110">For details about other threading considerations, see [Tablet PC Threading Considerations](tablet-pc-threading-considerations.md).</span></span>

 

 



