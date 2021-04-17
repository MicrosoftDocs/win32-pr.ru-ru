---
description: Если операционная система или даже приложение настроены на использование определенного языка и языкового стандарта, затрагиваются многие параметры.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Параметры языка документа и системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9408093a8583a4b17566b5fcd118b30439c0ebda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710910"
---
# <a name="document-and-system-locale-settings"></a><span data-ttu-id="72950-103">Параметры языка документа и системы</span><span class="sxs-lookup"><span data-stu-id="72950-103">Document and System Locale Settings</span></span>

<span data-ttu-id="72950-104">Если операционная система или даже приложение настроены на использование определенного языка и языкового стандарта, затрагиваются многие параметры.</span><span class="sxs-lookup"><span data-stu-id="72950-104">When the operating system, or even an application, is set to use a particular language and locale, many settings are affected.</span></span> <span data-ttu-id="72950-105">Эти параметры включают числовой формат, формат даты, формат валюты, сопоставление верхнего и нижнего регистра, порядок сортировки словаря, разметку и другие.</span><span class="sxs-lookup"><span data-stu-id="72950-105">These settings include numeric format, date format, currency format, uppercase and lowercase mapping, dictionary sort ordering, tokenization, and others.</span></span> <span data-ttu-id="72950-106">Хотя эти параметры помогают Windows Search обеспечить отличную локализованную поддержку, непредвиденные результаты могут возникнуть при поиске документов из одного языкового стандарта с помощью системы, для которой настроен другой языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="72950-106">Although these settings help Windows Search provide excellent localized support, unexpected results can occur when documents from one locale are searched by using a system that is set to another locale.</span></span>

<span data-ttu-id="72950-107">Когда объект [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) обрабатывает свойства текста и содержимое документа, он сообщает языку этого документа с индексатором содержимого.</span><span class="sxs-lookup"><span data-stu-id="72950-107">When the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) object processes a document's text properties and content, it reports the language of that document to the content indexer.</span></span> <span data-ttu-id="72950-108">С помощью этой информации Windows Search может применить соответствующее средство разбиения по словам.</span><span class="sxs-lookup"><span data-stu-id="72950-108">Using this information, Windows Search can apply the appropriate word breaker.</span></span>

 

 
