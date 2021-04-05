---
title: Архитектура обработчика
description: Архитектура обработчика
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068076"
---
# <a name="handler-architecture"></a><span data-ttu-id="c3fa5-103">Архитектура обработчика</span><span class="sxs-lookup"><span data-stu-id="c3fa5-103">Handler Architecture</span></span>

<span data-ttu-id="c3fa5-104">Внутренняя функция файла или обработчика потока определяется самим обработчиком.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-104">The internal function of a file or stream handler is defined by the handler itself.</span></span> <span data-ttu-id="c3fa5-105">Для приложения обработчик файлов обычно отображается как модуль для чтения и записи AVI-файлов.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-105">To an application, a file handler typically appears as a module to read and write AVI files.</span></span> <span data-ttu-id="c3fa5-106">Аналогичным образом обработчик потока отображается как модуль для чтения и записи определенного типа потока данных.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-106">Similarly, a stream handler appears as a module to read and write a specific type of data stream.</span></span> <span data-ttu-id="c3fa5-107">Последовательный интерфейс потока делает источник и назначение потока неважными для приложения, использующего обработчик.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-107">The consistent stream interface makes the source and destination of the stream unimportant to the application that uses the handler.</span></span>

<span data-ttu-id="c3fa5-108">Обработчик файлов предоставляет доступ к источнику данных, состоящему из одного или нескольких потоков данных.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-108">A file handler provides access to a data source consisting of one or more data streams.</span></span> <span data-ttu-id="c3fa5-109">Обработчики файлов обычно предоставляют доступ к файлам на диске, содержащим один или несколько потоков данных, а внутренние функции обработчика файлов считывают и записывают данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-109">File handlers typically provide access to disk files containing one or more data streams, and the internal functions of the file handler read and write the multimedia data.</span></span> <span data-ttu-id="c3fa5-110">Однако обработчики файлов могут работать с любыми источниками данных, например с цифровым каналом передачи, содержащим несколько потоков данных запутанной.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-110">However, file handlers can work with any data source, such as a digital transmission channel containing several intermingled data streams.</span></span>

<span data-ttu-id="c3fa5-111">В отличие от этого обработчик потока обрабатывает один тип данных и появляется в виде потока данных для приложения.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-111">In contrast, a stream handler processes one type of data and appears as a data stream to an application.</span></span> <span data-ttu-id="c3fa5-112">Обработчик потока может предоставлять данные, которые он создает, или может получать данные из файла или из внешнего источника.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-112">A stream handler can provide data that it manufactures, or it can retrieve data from a file or an external source.</span></span> <span data-ttu-id="c3fa5-113">Он предоставляет свои данные в формате, который может использовать приложение.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-113">It supplies its data in a format that your application can use.</span></span>

 

 




