---
description: Информационный поток сводки содержит сведения о пакете, который можно просмотреть с помощью проводника Microsoft Windows.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Сведения о потоке сводных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156355"
---
# <a name="about-the-summary-information-stream"></a><span data-ttu-id="84d59-103">Сведения о потоке сводных данных</span><span class="sxs-lookup"><span data-stu-id="84d59-103">About the Summary Information Stream</span></span>

<span data-ttu-id="84d59-104">Информационный поток сводки содержит сведения о пакете, который можно просмотреть с помощью проводника Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="84d59-104">The summary information stream contains information about the package that can be viewed through Microsoft Windows Explorer.</span></span> <span data-ttu-id="84d59-105">Эти сведения доступны через интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="84d59-105">This information is accessible through the **IStream** interface.</span></span> <span data-ttu-id="84d59-106">Автор должен предоставить значения для каждого из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="84d59-106">It is up to the author to provide the values for each of these properties.</span></span>

<span data-ttu-id="84d59-107">Информационный поток сводки использует COM для создания структурированного хранилища баз данных.</span><span class="sxs-lookup"><span data-stu-id="84d59-107">The summary information stream uses COM to provide structured storage of databases.</span></span> <span data-ttu-id="84d59-108">Модель COM поддерживает понятие структурированного хранилища, доступного через интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="84d59-108">COM supports the concept of structured storage accessible through the **IStream** interface.</span></span> <span data-ttu-id="84d59-109">Структурированное хранилище, в свою очередь, поддерживает концепцию наборов свойств в качестве гибкого метода сериализации практически любой информации.</span><span class="sxs-lookup"><span data-stu-id="84d59-109">Structured storage, in turn, supports the concept of property sets as a flexible method for serializing almost any information.</span></span> <span data-ttu-id="84d59-110">Спецификация COM определяет один стандартный набор свойств, сводную информацию, которая используется для заполнения страниц свойств, видимых в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="84d59-110">The COM specification defines a single standard property set, summary information, which is used to populate property sheets viewable from Windows Explorer.</span></span> <span data-ttu-id="84d59-111">Таким образом, данные, хранящиеся в потоке сводных данных, могут быть просмотрены пользователями, когда они правой кнопкой мыши щелкнули базу данных установщика или преобразовывают и выбрали пункт [Свойства](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="84d59-111">So, information stored in the summary information stream can be viewed by users when they right-click an installer database or transform and select [Properties](about-properties.md).</span></span>

<span data-ttu-id="84d59-112">Список набора свойств сводки см. в разделе [набор свойств потока сводных данных](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="84d59-112">For a list of the summary property set see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="84d59-113">Краткие описания свойств сводных данных, используемых в базах, преобразованиях и исправлениях, см. в разделе [описания свойств сводки](summary-property-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="84d59-113">For brief descriptions of the Summary Information properties used with databases, transforms, and patches, see [Summary Property Descriptions](summary-property-descriptions.md).</span></span>

 

 



