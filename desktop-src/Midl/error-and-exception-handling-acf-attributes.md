---
title: Атрибуты ACF обработки ошибок и исключений
description: Используйте следующие атрибуты для обработки ошибок.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- ACF MIDL, атрибуты, обработка ошибок и исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681614"
---
# <a name="error-and-exception-handling-acf-attributes"></a><span data-ttu-id="5d7ce-104">Атрибуты ACF обработки ошибок и исключений</span><span class="sxs-lookup"><span data-stu-id="5d7ce-104">Error and Exception Handling ACF Attributes</span></span>

<span data-ttu-id="5d7ce-105">Используйте следующие атрибуты для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="5d7ce-105">Use the following attributes for error handling.</span></span>



| <span data-ttu-id="5d7ce-106">attribute</span><span class="sxs-lookup"><span data-stu-id="5d7ce-106">Attribute</span></span>                                                                | <span data-ttu-id="5d7ce-107">Использование</span><span class="sxs-lookup"><span data-stu-id="5d7ce-107">Usage</span></span>                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7ce-108">[**\_**](comm-status.md)[**\_ состояние ошибки** состояния связи](fault-status.md)</span><span class="sxs-lookup"><span data-stu-id="5d7ce-108">[**comm\_status**](comm-status.md)[**fault\_status**](fault-status.md)</span></span> | <span data-ttu-id="5d7ce-109">Позволить клиентскому приложению корректно обрабатывать исключения, вызывая возвращение клиенту ошибок связи и сервера в качестве значений параметров.</span><span class="sxs-lookup"><span data-stu-id="5d7ce-109">Let your client application handle exceptions gracefully by causing communication and server errors to be returned to the client as parameter values.</span></span> <span data-ttu-id="5d7ce-110">Затем клиентское приложение может вызвать функцию времени выполнения RPC [**дцеерроринктекст**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) для ретрансляции сообщения об ошибке пользователю.</span><span class="sxs-lookup"><span data-stu-id="5d7ce-110">The client application can then call the RPC run-time function [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) to relay an error message to the user.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5d7ce-111">См. также</span><span class="sxs-lookup"><span data-stu-id="5d7ce-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d7ce-112">Импорт файлов и библиотек типов</span><span class="sxs-lookup"><span data-stu-id="5d7ce-112">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> </dl>

 

 