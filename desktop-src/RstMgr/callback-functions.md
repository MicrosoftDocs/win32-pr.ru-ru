---
title: Функции обратного вызова диспетчера перезапуска
description: API диспетчера перезапуска использует функции обратного вызова, приведенные в следующей таблице.
ms.assetid: abb78aa5-0487-4e99-85b6-adc38b600c09
keywords:
- Диспетчер перезапуска, Справка, функции обратного вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c850dd805aeff664e3e09292825e342a6c5603
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793327"
---
# <a name="restart-manager-callback-functions"></a><span data-ttu-id="5a757-104">Функции обратного вызова диспетчера перезапуска</span><span class="sxs-lookup"><span data-stu-id="5a757-104">Restart Manager Callback Functions</span></span>

<span data-ttu-id="5a757-105">API диспетчера перезапуска использует функции обратного вызова, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5a757-105">The Restart Manager API uses the callback functions in the following table.</span></span>



| <span data-ttu-id="5a757-106">Функция Callback</span><span class="sxs-lookup"><span data-stu-id="5a757-106">Callback Function</span></span>                                               | <span data-ttu-id="5a757-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5a757-107">Description</span></span>                                                                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a757-108">**\_ \_ обратный вызов состояния записи RM \_**</span><span class="sxs-lookup"><span data-stu-id="5a757-108">**RM\_WRITE\_STATUS\_CALLBACK**</span></span>](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) | <span data-ttu-id="5a757-109">Приложение, запустившего сеанс диспетчера перезапуска, может передать указатель на эту функцию в функции диспетчера перезапуска, чтобы получить процент полноты.</span><span class="sxs-lookup"><span data-stu-id="5a757-109">The application that started the Restart Manager session can pass a pointer to this function to the Restart Manager functions to receive a percentage of completeness.</span></span> |



 

 

 