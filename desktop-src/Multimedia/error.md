---
title: Error
description: Error
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- Функции обратного вызова Авикап, сообщения об ошибках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f418f16ae2af15902e96927990d79a4ecac08b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068393"
---
# <a name="error"></a><span data-ttu-id="79124-104">Ошибка</span><span class="sxs-lookup"><span data-stu-id="79124-104">Error</span></span>

<span data-ttu-id="79124-105">В окне отслеживания используются сообщения об ошибках для уведомления приложения об ошибках Авикап, таких как нехваткой места на диске, попытка записи в файл только для чтения, сбой доступа к оборудованию или удаление слишком большого количества кадров.</span><span class="sxs-lookup"><span data-stu-id="79124-105">A capture window uses error notification messages to notify your application of AVICap errors, such as running out of disk space, attempting to write to a read-only file, failing to access hardware, or dropping too many frames.</span></span> <span data-ttu-id="79124-106">Содержимое уведомления об ошибке содержит идентификатор сообщения и форматированную текстовую строку, готовую для просмотра.</span><span class="sxs-lookup"><span data-stu-id="79124-106">The content of an error notification includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="79124-107">Приложение может использовать идентификатор сообщения для фильтрации уведомлений и ограничения сообщений, которые должны быть представлены пользователю.</span><span class="sxs-lookup"><span data-stu-id="79124-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="79124-108">Нулевой идентификатор сообщения означает, что новая операция запускается, а функция обратного вызова должна очистить любое отображаемое сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="79124-108">A message identifier of zero indicates a new operation is starting and the callback function should clear any displayed error message.</span></span>

 

 




